test-gh

- name: SCP files to production system uses: appleboy/scp-action@master with:
  host: ${{ secrets.DEPLOY_DOCS_HOST }} username: ${{ secrets.DEPLOY_DOCS_USERNAME }} key: ${{ secrets.DEPLOY_KEY }} source: ${{ steps.rendering.outputs.renderedPath }} rm: false tar_tmp_path: ${{
  secrets.TMP_TARGET_PATH }} target: ${{ secrets.TARGET_PATH }}/type_short/vendor/name/target_branch_directory/
