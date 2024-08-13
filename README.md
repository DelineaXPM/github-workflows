# github-workflow

> **_Warning_**

This is a collection of github workflow automation for managing workflows for this GitHub organization.
This is not a published marketplace set of actions for external use, and customized for workflows on public repos managed here.

These are subject to breaking changes and managed by the DevOps Secrets Vault team primarily.

## Contributors

<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->

<!-- readme: collaborators,contributors -start -->
<table>
	<tbody>
		<tr>
            <td align="center">
                <a href="https://github.com/sheldonhull">
                    <img src="https://avatars.githubusercontent.com/u/3526320?v=4" width="100;" alt="sheldonhull"/>
                    <br />
                    <sub><b>Sheldonhull</b></sub>
                </a>
            </td>
            <td align="center">
                <a href="https://github.com/pacificcode">
                    <img src="https://avatars.githubusercontent.com/u/918320?v=4" width="100;" alt="pacificcode"/>
                    <br />
                    <sub><b>Bill Hamilton</b></sub>
                </a>
            </td>
		</tr>
	<tbody>
</table>
<!-- readme: collaborators,contributors -end -->

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

## Lint Action

The lint action now performs a second job of validating that a changie entry was added. This ensures that all pull requests, except those with specific labels, include a changie entry in the `.changes/unreleased` directory.

