# Github Actions Docs

Github Actions own documentation.

| Action | Steps to perform the action |
| ------------- | ------------- |
| Upload release to Github | 1) In the `.github/workflows/<FILE_NAME>.yml` file add the following (between the `name` and `jobs` keys): <br> ![on push tags](on-push-tags.png?raw=true "on push tags")<br> Full example: <br> ![publish release](publish-release.png?raw=true "publish release") <br>2) Create the tag with this command (replace the X with any version): `git tag vX.X.X.X`.<br> 3) Commit all changes to be included in the tag. <br> 4) Upload the created tag with the following command: `git push --tags`. <br> The action of the .yml file will be executed once the tag is created and uploaded to the repository (steps 2, 3 and 4). |