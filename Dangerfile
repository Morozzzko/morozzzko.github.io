# frozen_string_literal: true

modified_files = (git.added_files + git.modified_files)

files_for_proselint = modified_files.select do |file_path|
  file_path.end_with?('md') &&
    file_path.start_with?('_posts', '_drafts', '_slides')
end

prose.lint_files(
  files_for_proselint
)
prose.check_spelling(
  files_for_proselint
)
