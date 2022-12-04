---

database-plugin: basic

---

%% dbfolder:yaml
name: Blind 75
description: Coding Practice Repetiton Check
columns:
  __file__:
    key: __file__
    input: markdown
    label: File
    accessorKey: __file__
    isMetadata: true
    skipPersist: false
    isDragDisabled: false
    csvCandidate: true
    position: 1
    width: 80
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
  Difficulty:
    input: select
    accessorKey: Difficulty
    key: Difficulty
    label: Difficulty
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "medium", backgroundColor: "hsl(358, 95%, 90%)"}
      - { label: "easy", backgroundColor: "hsl(3, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
  Repeat:
    input: text
    accessorKey: Repeat
    key: Repeat
    label: Repeat
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
  Topics:
    input: select
    key: Topics
    accessorKey: Topics
    label: Topics
    position: 2
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "9", backgroundColor: "hsl(204, 95%, 90%)"}
      - { label: "array", backgroundColor: "hsl(232, 95%, 90%)"}
      - { label: "binary", backgroundColor: "hsl(260, 95%, 90%)"}
      - { label: "dp", backgroundColor: "hsl(250, 95%, 90%)"}
      - { label: "graph", backgroundColor: "hsl(326, 95%, 90%)"}
      - { label: "interval", backgroundColor: "hsl(62, 95%, 90%)"}
      - { label: "linkedlist", backgroundColor: "hsl(186, 95%, 90%)"}
      - { label: "math", backgroundColor: "hsl(116, 95%, 90%)"}
      - { label: "stack", backgroundColor: "hsl(28, 95%, 90%)"}
      - { label: "string", backgroundColor: "hsl(241, 95%, 90%)"}
      - { label: "tree", backgroundColor: "hsl(295, 95%, 90%)"}
    config:
      enable_media_view: true
      media_width: 100
      media_height: 100
      isInline: false
config:
  remove_field_when_delete_column: false
  cell_size: compact
  sticky_first_column: false
  group_folder_column: 
  show_metadata_created: false
  show_metadata_modified: false
  show_metadata_tasks: false
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  source_data: current_folder
  source_form_result: root
  source_destination_path: /
  frontmatter_quote_wrap: false
  row_templates_folder: /
  current_row_template: 
  pagination_size: 200
  formula_folder_path: /
  inline_default: false
  inline_new_position: top
  date_format: yyyy-MM-dd
  datetime_format: "yyyy-MM-dd HH:mm:ss"
filters:
  enabled: true
  conditions:
%%