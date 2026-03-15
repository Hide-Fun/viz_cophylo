```yaml
schema: viz_cophylo.recipe.v1
mode: llm_only
human_readability_required: false
generated_on: 2026-03-05
root: /Users/hidefungi2/Github/viz_cophylo

source_scan:
  include:
    - "*.qmd"
    - "*.yml"
    - "*.bib"
    - "*.scss"
  excluded_generated:
    - "_book/**"
    - ".quarto/**"

book_contract:
  config_path: _quarto.yml
  project_type: book
  title: Visualise cophylogenetic signals
  subtitle: Phylogeny x Bipartite Network Workflows
  bibliography: references.bib
  chapters_in_order:
    - index.qmd
    - ggbipartite-visualization-ja.qmd
    - ggbipartite-publishable-ja.qmd
    - ggbipartite-sciname-tree-ja.qmd
    - session-info.qmd
  html:
    theme_chain: [litera, styles-modern.scss]
    toc: true
    toc_depth: 3
    number_sections: false
    code_copy: true
    code_overflow: wrap
    smooth_scroll: true
    anchor_sections: true
    link_external_newwindow: true
    embed_resources: true
    grid:
      sidebar_width: 320px
      body_width: 980px
      margin_width: 240px

r_dependencies_union:
  - RPANDA
  - ape
  - cowplot
  - dplyr
  - ggbipartite
  - ggplot2
  - ggtree
  - marquee
  - patchwork
  - tibble
  - tidyr
  - tidyverse

doc_index:
  - path: _quarto.yml
    kind: config
    loc: 40
    sha256: 91443ff669cdd0ce953e016fbd64cbf0cf01b12a0f8e4ea3a89ce99c74c0d633
  - path: index.qmd
    kind: preface
    in_book: true
    order: 1
    loc: 15
    sha256: bbf26f2d5c4837fb804ab80cdd88ab42329c22a014187fc05648ad9bc318d073
    chapter_count_declared: 4
    chunks:
      - unnamed_chunk_package_version_check
    chunk_body_signals:
      - packageVersion("ggbipartite")
  - path: ggbipartite-visualization-ja.qmd
    kind: chapter
    in_book: true
    order: 2
    chapter_id: ch1_bipartite_visualization_basics
    loc: 826
    sha256: 0ab3d2662c6031c92171b59b3bf0382266c80612f7a73c90d0cf16191264d52f
    frontmatter:
      execute: {echo: true, warning: false, message: false, fig_dpi: 350}
      embed_resources: true
      vignette_engine: quarto::html
    libs:
      - ggplot2
      - dplyr
      - tidyr
      - tibble
      - ape
      - ggtree
      - ggbipartite
      - patchwork
    chunk_labels:
      - setup
      - tree-overview
      - matrix-alignment
      - to-long
      - abundance-basic
      - metadata-coloring
      - metadata-coloring-point
      - abundance-layout-tuning
      - binary-plot
      - label-annotation
      - tree-link-setup
      - tree-link-display
      - tree-link-align-setup
      - tree-link-align-display
      - tree-scale-preserve-setup
      - tree-scale-preserve-display
    section_flow:
      - prep
      - tree_overview
      - matrix_order_alignment
      - matrix_to_long_transform
      - abundance_plot
      - metadata_coloring
      - layout_tuning
      - binary_plot
      - bn_coord_annotation
      - tree_network_link
      - scale_preserved_composite
      - troubleshooting
      - summary
    core_functions:
      - rtree
      - ggtree
      - get_tip_order
      - to_longer
      - construct_bn_coordination
      - geom_bipnet_box
      - geom_bipnet_interaction
      - geom_bipnet_point
      - create_link
      - adjust_tree
      - get_yrange
      - compute_box_label_coords
      - scale_x_reverse
      - coord_equal
  - path: ggbipartite-publishable-ja.qmd
    kind: chapter
    in_book: true
    order: 3
    chapter_id: ch2_publishable_cophylo_figure
    loc: 697
    sha256: 2407a1077c018ad48ddf66aca71d16f301e941d972d94d32ab001ae457ad11a8
    frontmatter:
      execute: {echo: true, warning: false, message: false, fig_dpi: 350}
      embed_resources: true
      vignette_engine: quarto::html
    libs:
      - tidyverse
      - cowplot
      - ape
      - ggtree
      - marquee
      - RPANDA
      - ggbipartite
    chunk_labels:
      - setup
      - make-data
      - publishable-tree-annotation
      - abundance-publishable-figure
      - binary-publishable-figure
      - binary-rpanda-nodepoint
      - export-template-recommended
    section_flow:
      - prep
      - synthetic_data_and_phylo
      - tree_annotation
      - tip_node_label_unification
      - abundance_publishable_figure
      - binary_publishable_figure
      - binary_with_rpanda_signal_overlay
      - export_notes
    core_functions:
      - construct_bn_coordination
      - adjust_tree
      - geom_tiplab
      - geom_treescale
      - geom_nodelab
      - geom_marquee
      - geom_nodepoint
      - create_link
      - get_yrange
      - phylosignal_sub_network
      - ggsave
  - path: ggbipartite-sciname-tree-ja.qmd
    kind: chapter
    in_book: true
    order: 4
    chapter_id: ch3_sciname_labeling
    loc: 398
    sha256: 12de49ea4adaaf7e49465fa07021825a078221cf4336005157970457a7dd006c
    frontmatter:
      execute: {echo: true, warning: false, message: false, fig_dpi: 350}
      embed_resources: true
      vignette_engine: quarto::html
    libs:
      - tidyverse
      - ape
      - ggtree
      - marquee
      - ggbipartite
    chunk_labels:
      - setup
      - make-dummy-tree
      - style-labels
      - practical-label-workflow
      - unaligned-labels
      - aligned-labels
      - avoid-tip-label-clipping
      - reversed-tree
      - example-format-node-support
      - example-style-tree-label
      - example-style-sciname
    section_flow:
      - prep
      - dummy_tree_generation
      - sciname_and_support_formatting
      - practical_label_pipeline
      - tiplab_unaligned
      - tiplab_aligned
      - clipping_control
      - reverse_axis_layout
      - api_spec_notes
      - practical_memo
    core_functions:
      - style_tree_label
      - format_node_support
      - style_sciname
      - root
      - geom_marquee
      - geom_nodelab
      - scale_x_continuous
      - scale_x_reverse
      - tiplab_marquee_data
      - tiplab_marquee_data_unaligned
      - tiplab_segment_data
  - path: session-info.qmd
    kind: chapter
    in_book: true
    order: 5
    chapter_id: ch4_session_info
    loc: 10
    sha256: a876889b7022ce190b5f223d8949e3dc2147b355310f208e018f6350040bc068
    chunks:
      - session-info
    chunk_body_signals:
      - sessionInfo()
  - path: references.bib
    kind: bibliography
    loc: 19
    sha256: 828a0efe860cbc4578136cce01a918f4bc28e58e14a93de0ebc812ad39f2af67
    entries:
      - key: knuth84
        type: article
        doi: 10.1093/comjnl/27.2.97
  - path: styles-modern.scss
    kind: theme_override
    loc: 106
    sha256: 40340ac8a62d48b1fd4fd1eb6a764f16a1868b421779b01f71923d061ff63061
    font_stack_sans:
      - Inter
      - Noto Sans JP
      - Hiragino Kaku Gothic ProN
      - Yu Gothic UI
      - Yu Gothic
      - Meiryo
      - sans-serif
    font_stack_mono:
      - JetBrains Mono
      - SFMono-Regular
      - Menlo
      - Consolas
      - monospace
    palette:
      primary: "#0e6670"
      secondary: "#a35a32"
      body_bg: "#f7f9fc"
      body_color: "#1f2937"
      heading_color: "#162235"
      link_color: "#0f5ea6"
      code_color: "#113a61"
    readability_tuning:
      - higher_text_contrast
      - light_background_gradients
      - stronger_link_visibility
      - code_block_soft_border
      - active_sidebar_item_highlight
  - path: intro.qmd
    kind: legacy_orphan_doc
    in_book: false
    loc: 9
    sha256: 407c7e49e7a404320402578c10176bcb982158027468241bdc427ab4226e44bb
  - path: summary.qmd
    kind: legacy_orphan_doc
    in_book: false
    loc: 7
    sha256: 5eda7cbb6237431fd5b857a1e23679a2cb3ed4dbb74c1b54c8387e20d1782263
  - path: references.qmd
    kind: legacy_orphan_doc
    in_book: false
    loc: 4
    sha256: 716ef649ca7fb29cac3cba133f157c33c0049cff6ac9c2eaf922886e45c7c077

semantic_graph:
  node_types: [config, chapter, bibliography, style]
  edges:
    - from: _quarto.yml
      to: index.qmd
      type: chapter_order
      ord: 1
    - from: _quarto.yml
      to: ggbipartite-visualization-ja.qmd
      type: chapter_order
      ord: 2
    - from: _quarto.yml
      to: ggbipartite-publishable-ja.qmd
      type: chapter_order
      ord: 3
    - from: _quarto.yml
      to: ggbipartite-sciname-tree-ja.qmd
      type: chapter_order
      ord: 4
    - from: _quarto.yml
      to: session-info.qmd
      type: chapter_order
      ord: 5
    - from: _quarto.yml
      to: references.bib
      type: bibliography_ref
    - from: _quarto.yml
      to: styles-modern.scss
      type: html_theme_ref
    - from: index.qmd
      to: ggbipartite
      type: runtime_version_probe
    - from: session-info.qmd
      to: R_session
      type: runtime_environment_capture

pipeline_dsl:
  book_render: "quarto_render => _book/index.html + chapter_html"
  ch1: "phylo(seed)->tip_order->matrix_align->to_long(row,column,count)->abundance_plot->metadata_color->binary_plot->tree_link->scale_preserved_layout"
  ch2: "synthetic_data->annotated_trees->abundance_publishable->binary_publishable->rpanda_signal_overlay->export_template"
  ch3: "dummy_tree->label_formatting(style_tree_label,format_node_support)->aligned_or_unaligned_tip_labels->clip_control->reverse_layout"
  ch4: "sessionInfo()"

llm_operational_notes:
  - Treat ggbipartite-visualization-ja.qmd as foundational API usage.
  - Treat ggbipartite-publishable-ja.qmd as production-grade composition/template.
  - Treat ggbipartite-sciname-tree-ja.qmd as labeling/annotation utility reference.
  - session-info.qmd is reproducibility metadata endpoint.
  - intro.qmd/summary.qmd/references.qmd exist but are not currently in chapter graph.

autonomy_profile:
  objective: semi_autonomous_plot_generation
  control_mode: user_goal + llm_execution
  expected_operator_intervention_points:
    - goal_confirmation
    - final_artifact_approval

io_contract:
  required_inputs:
    - plot_goal
    - target_chapter_id
    - data_mode
    - output_basename
  optional_inputs:
    - dataset_paths
    - palette_override
    - width_height
    - seed
  input_enums:
    target_chapter_id:
      - ch1_bipartite_visualization_basics
      - ch2_publishable_cophylo_figure
      - ch3_sciname_labeling
    data_mode:
      - synthetic
      - provided
  required_outputs:
    - rendered_html_or_figure_file
    - execution_log
    - reproducibility_block
  reproducibility_block_fields:
    - chapter_id
    - chunk_labels_used
    - package_versions
    - seed
    - output_paths

task_router:
  by_goal_keywords:
    basic_or_exploratory_network:
      chapter_id: ch1_bipartite_visualization_basics
      prefer_chunks:
        - abundance-basic
        - metadata-coloring
        - binary-plot
        - tree-link-display
    publication_ready_composite:
      chapter_id: ch2_publishable_cophylo_figure
      prefer_chunks:
        - publishable-tree-annotation
        - abundance-publishable-figure
        - binary-publishable-figure
        - binary-rpanda-nodepoint
    label_or_taxonomy_cleanup:
      chapter_id: ch3_sciname_labeling
      prefer_chunks:
        - style-labels
        - aligned-labels
        - avoid-tip-label-clipping
        - reversed-tree

execution_protocol:
  preflight:
    - validate_paths_exist
    - resolve_target_chapter_from_router_or_input
    - set_seed_if_missing: 20260305
    - verify_required_r_packages
  compose:
    - choose_minimal_chunk_subset_for_goal
    - preserve_original_factor_ordering_for_row_column
    - enforce_theme_from_book_contract
  run:
    - render_target: quarto_render_selected_qmd_or_book
    - collect_stdout_stderr
    - emit_artifact_manifest
  postcheck:
    - ensure_output_exists
    - check_no_runtime_error
    - include_session_info_reference
    - assert_visual_readability_constraints

visual_constraints:
  - keep_sans_font_stack_from_styles_modern_scss
  - maintain_high_contrast_text_on_light_background
  - avoid_overlapping_tip_labels
  - preserve_tree_network_alignment_when_links_enabled
  - keep_binary_and_abundance_variants_distinct_when_requested

failure_recovery:
  strategies:
    - on_missing_package: install_or_report_blocker
    - on_font_or_device_issue: fallback_to_html_render_path
    - on_label_overlap: increase_expand_or_switch_align_true
    - on_scale_mismatch: apply_get_yrange_and_coord_sync
  stop_conditions:
    - unresolved_missing_input_after_prompt
    - repeated_runtime_failure_over_2_attempts

success_criteria:
  - artifacts_generated: true
  - logs_captured: true
  - reproducibility_block_present: true
  - selected_chapter_protocol_followed: true
```
