## Welcome
Welcome to the CloudBees examples repository. This repository is a place for storing tutorials, examples, and other learning materials. Of note:

* It is owned and managed by the docs team. Please contact a docs team member or manager for assistance in adding files.
* This repo contains assets that complement mentions in product documentation.  As such, it is not standalone.
* Top-level folders are named to reflect their contents and must contain the CloudBees product name according to this convention: `<productName>-<shortDescription>`. Keep names narrow in scope.
* A given folder should contain related assets as indicated by the folder name. Create other folders as needed.
* Consider providing a local Readme.md file in the asset folder.

## Managing asset links
* When providing a link in product documentation to a repo asset, consider using the raw link where appropriate. This gives the reader a cut/paste-ready version of the asset.
* Choose prudent filenames to minimize future renames. Simply moving a file to a new name breaks exiting links out in the wild. It is recommended to leverage symbolic links to effect "redirects". The following shows how to rename `origfile.yaml` and then create a hard link to this original name. As a result, links to the old name will automatically "redirect" to the new name.

  ```shell
  // move old file to new name
  git mv origfile.yaml newfile.yaml
  git commit -m "commit message"
  git push
  
  // create symlink to old file
  ln -s newfile.yaml origfile.yaml
  
  // add, commit, and push the symlink
  git add origfile.yaml
  git commit -m "created symlink to origfile.yaml"
  git push
  ```

## Examples summary
The following table is a brief summary of each of the example projects.

|Directory|Description  |
|:---|:-|
|pipeline-template-examples|This repository includes a sample Pipeline Template Catalog. The demos folder includes examples of how to customize a template.yaml file.  |
|helm-custom-value-file-examples|Custom Property Value Files for the CloudBees Core for Modern Platforms Helm installation.|
|flow-on-kubernetes|Sample property value files for CloudBees Flow on Kubernetes Helm installation.|
