# PureBasic Repository Template [![CC0 Badge][CC0 Badge]][CC0 Link]

- https://github.com/fantaisie-software/purebasic-repository-template

A boilerplate for quickly creating [PureBasic] projects with all the right settings in place.

Created by [Tristano Ajmone] on August 12, 2019. Released into the Public Domain.

    PureBasic 5.70 LTS

[CC0 Badge]: https://licensebuttons.net/p/zero/1.0/88x31.png "CC0 1.0 Universal"
[CC0 Link]: #license
[Tristano Ajmone]: https://github.com/tajmone "View Tristano Ajmone's GitHub profile"

-----

**Table of Contents**


<!-- MarkdownTOC autolink="true" bracket="round" autoanchor="false" lowercase="only_ascii" uri_encoding="true" levels="1,2,3,4" -->

- [About this Template](#about-this-template)
    - [What Do I Get?](#what-do-i-get)
        - [Repository settings](#repository-settings)
            - [Git Configurations](#git-configurations)
            - [EditorConfig Settings](#editorconfig-settings)
            - [Travis CI Validation](#travis-ci-validation)
        - [PureBasic License Files](#purebasic-license-files)
        - [README Template](#readme-template)
    - [License](#license)
- [PureBasic Links](#purebasic-links)

<!-- /MarkdownTOC -->

-----

# About this Template

In June 6, 2019 GitHub announced a new feature to [generate new repositories with repository templates]. This is a cool feature, so I decided to create a repository template for PureBasic projects, and release it into the public domain.

You can use this template to quickly create a GitHub repository for PureBasic projects by clicking on the <kbd>Use this template</kbd> button placed on the bar above the files list, or [by clicking on this link].

Any new repository created using this template will be optimally configured for working with PureBasic projects.

For more detailed information on using repository templates, see:

- [GitHub Help » Creating a repository from a template]

To learn more about the internal details of this template, consult the [repository Wiki].

[by clicking on this link]: https://github.com/fantaisie-software/purebasic-repository-template/generate "Create a new repository using the PureBasic Repository Template!"
[generate new repositories with repository templates]: https://github.blog/2019-06-06-generate-new-repositories-with-repository-templates/ "Read full article on GitHub Blog"
[GitHub Help » Creating a repository from a template]: https://help.github.com/en/articles/creating-a-repository-from-a-template
[repository Wiki]: https://github.com/fantaisie-software/purebasic-repository-template/wiki "Go to the Wiki of the PureBasic Repository Template project"

## What Do I Get?

The template is just a boilerplate containing:

- Repository settings designed to optimize PureBasic workflow:
    + [Git configurations](#git-configurations "Jump to section").
    + [EditorConfig code styles consistency](#editorconfig-settings "Jump to section").
    + [Travis CI code styles validation](#travis-ci-validation "Jump to section").
- [License files of PureBasic third party components](#purebasic-license-files "Jump to section").
- [README document template](#readme-template "Jump to section").

### Repository settings

Setting up a repository for optimal workflow is a time-consuming and repetitive task.
This template provides well tested boilerplate settings designed to optimize cross-platform collaborative editing of PureBasic projects.

#### Git Configurations

- [`.gitignore` ](./.gitignore "View source file")
- [`.gitattributes`](./.gitattributes "View source file")


The included `.gitignore` and `.gitattributes` files contain carefully designed patterns that will cover most PureBasic usage scenarios in cross-platform environments.

The `.gitattributes` settings ensure that [end-of-line normalization] is handled properly by Git across all operating systems, avoiding conflicts between Windows and Linux/macOS in collaborative projects.
It also defines some settings for [GitHub Linguist], to cover some PureBasic file extensions not recognized by Linguist, and to ensure proper statistics gathering for the project, and correct syntax highlighting in the GitHub WebUI.

The `.gitignore` file covers common ignore patterns for Windows, Linux and macOS, as well as excluding from the repository PureBasic project and configurations files — which usually are best kept out of a project, due to personal data leakage (with project files) and because these files will end up differing on every end-user machine, where they are overwritten and changed by the PureBasic IDE, thus polluting Git work directory (preventing branch switching) and exposing the project to spurious commits.

[end-of-line normalization]: https://adaptivepatchwork.com/2012/03/01/mind-the-end-of-your-line/ "Learn more on Git EOL normalization from Tim Clem's article 'Mind the End of Your Line'"
[GitHub Linguist]: https://github.com/github/linguist "Visit the GitHub Linguist repository"

#### EditorConfig Settings

- [`.editorconfig`](./.editorconfig)

[EditorConfig] settings help preserving consistent coding styles in repositories where multiple developers work on the same files across various editors and IDEs, protecting it from mixed indentation styles and sizes, file encoding corruption, trailing white spaces and other code inconsistencies commonly found in collaborative editing.

The template provides code style settings for PureBasic sources and other file types commonly found in PureBasic projects:

- Repository configuration files (`.giattributes`, `.gitignore`, etc.)
- Batch and Shell scripts
- Markdown documentation.

Modern editors will automatically pick up these settings from the `.editorconfig` file and enforce them project-wide, overriding user settings in favour of project-specific settings.
[A list of free plug-ins is available at editorconfig.org] for editors and IDEs that don't support [EditorConfig] natively.

[A list of free plug-ins is available at editorconfig.org]: https://editorconfig.org/#download "See the list of EditorConfig plug-ins"
[EditorConfig]: https://editorconfig.org "Visit EditorConfig website"

#### Travis CI Validation

- [`.travis.yml`](./.travis.yml)
- [`validate.sh`](./validate.sh)

The template includes a basic [Travis CI] configuration to automatically validate every commit and pull request against the `.editorconfig` settings, to ensure that submitted contents honour the code style conventions of the project.
[EditorConfig] validation is done via [EClint]  (Node.js).

The `validate.sh` script can also be executed locally to test that all files in the project meet the [EditorConfig] requirements, before committing changes to the repository.

[Travis CI] is a hosted [continuous integration] and deployment service to build and test software projects hosted at GitHub.
The service is freely available for open-source projects and can be activated per-repository or profile-wide.

[continuous integration]: https://en.wikipedia.org/wiki/Continuous_integration "See Wikipedia page on 'Continuous integration'"
[EClint]: https://www.npmjs.com/package/eclint "Visit the EClint page at NPM"
[Node.js]: https://nodejs.org/en/ "Visit Node.js website"
[Travis CI]: https://travis-ci.com "Visit Travis CI website"

### PureBasic License Files

The license files included in this project contain up to date copies of the third party components licenses used by PureBasic.

|                    file                   |                                required by                                |        source        |
|-------------------------------------------|---------------------------------------------------------------------------|----------------------|
| [`PBLicense.txt`][LF_All]                 | Required by [all applications].                                           | [link][LL_All]       |
| [`PBLicense_3DEngine.txt`][LF_3DEngine]   | [OGRE] license for [PureBasic 3D Engine] (OGRE).                          | [link][LL_3DEngine]  |
| [`PBLicense_ExpatXML.txt`][LF_XML]        | [Expat] license for the [XML library].                                    | [link][LL_XML]       |
| [`PBLicense_PCRE.txt`][LF_PCRE]           | [PCRE] license for the [RegularExpression library].                       | [link][LL_PCRE]      |
| [`PBLicense_Scintilla.txt`][LF_Scintilla] | [Scintilla] license for the [Scintilla library].                          | [link][LL_Scintilla] |
| [`PBLicense_udis86.txt`][LF_udis86]       | [Udis86] license for the [disassembly commands] of the [OnError library]. | [link][LL_udis86]    |

These files are a useful time saver for any project, for you can quickly concatenate them into a single `LICENSE` file for distributing your binaries, according to the PureLibs used by your project, and then just delete the original files of the template.
It's much faster than having to manually copy and paste each license from the PureBasic Documentation.

> **IMPORTANT NOTE** — These license files mirror the PureBasic version indicated at the beginning of this document.
> Newer versions of PureBasic might introduce new third party components, and require additional credits and licenses.
> If you're using a different PureBasic version from the one indicated in this document, you should check the licenses provided in the [PureBasic Documentation] of that specific release.
>
> I'll strive to ensure that with every new PureBasic release this template and the license files are updated accordingly (if needed), but I can't be held responsible for any licenses omissions or mistakes — every author is responsible to ensure that his/her project fulfils all the license requirements.

<!-- PB License Files -->

[LF_3DEngine]: ./PBLicense_3DEngine.txt "View license file"
[LF_All]: ./PBLicense.txt "View license file"
[LF_XML]: ./PBLicense_ExpatXML.txt "View license file"
[LF_PCRE]: ./PBLicense_PCRE.txt "View license file"
[LF_Scintilla]: ./PBLicense_Scintilla.txt "View license file"
[LF_udis86]: ./PBLicense_udis86.txt "View license file"

<!-- PB Licenses Links -->

[LL_3DEngine]: https://www.purebasic.com/documentation/reference/license_engine3d.html "View license at PureBasic online Documentation"
[LL_All]: https://www.purebasic.com/documentation/reference/license_application.html "View license at PureBasic online Documentation"
[LL_XML]: https://www.purebasic.com/documentation/mainguide/expat.html "View license at PureBasic online Documentation"
[LL_PCRE]: https://www.purebasic.com/documentation/mainguide/pcre.html "View license at PureBasic online Documentation"
[LL_Scintilla]: https://www.purebasic.com/documentation/mainguide/scintilla.html "View license at PureBasic online Documentation"
[LL_udis86]: https://www.purebasic.com/documentation/mainguide/udis86.html "View license at PureBasic online Documentation"

<!-- 3rd party components and PureLibs -->

[OGRE]: https://www.ogre3d.org "Visit OGRE website"
[Expat]: https://libexpat.github.io "Visit Expat website"
[PCRE]: http://www.pcre.org "Visit OGRE website"
[Scintilla]: https://www.scintilla.org "Visit Scintilla website"
[Udis86]: http://udis86.sourceforge.net "Visit Udis86 website"

[all applications]: https://www.purebasic.com/documentation/reference/license_application.html
[PureBasic 3D Engine]: https://www.purebasic.com/documentation/engine3d/index.html
[XML library]: https://www.purebasic.com/documentation/xml/index.html
[RegularExpression library]: https://www.purebasic.com/documentation/regularexpression/index.html
[Scintilla library]: https://www.purebasic.com/documentation/scintilla/index.html
[disassembly commands]: https://www.purebasic.com/documentation/onerror/examineassembly.html
[OnError library]: https://www.purebasic.com/documentation/onerror/index.html

### README Template

You also get this markdown README file that you're reading right now, which contains the _[PureBasic Links]_ section providing useful links to various PureBasic assets on the Internet, which you might reuse in your project.

It's a well structured markdown document, with reference-style links to PureBasic sites of interest (at the end of the source document) which might come handy — and could spare you a good amount of typing, if you're going to link to them.

If you don't need the README file you can just trash it, but chances are that you'll be adding a `README.md` file to your project anyway, so you might as well just overwrite it, or keep just those reference links that you need.
After some initial thoughts, I finally decided that it was better to include this README file in the template, for the benefit of those wishing to offer links to the PureBasic website and forums, rather than leave it out.
For those who'll need it, it's going to be a true time-saver, while those who don't need it shouldn't be bothered much by having to delete/overwrite it.

[PureBasic Links]: #purebasic-links "Jump to links section"

## License

To the extent possible under law, [Tristano Ajmone] has waived all copyright and related or neighboring rights to the [PureBasic Repository Template]. This work is published from: Italy.

The __[PureBasic Repository Template]__ is released into the public domain via the [CC0 1.0 Universal] dedication, so that it might be freely used for any project, without causing licenses conflicts and without imposing any restrictions or obligations (not even crediting or linking back).

[CC0 1.0 Universal]: https://creativecommons.org/publicdomain/zero/1.0/ "Learn more about Creative Commons 0"
[PureBasic Repository Template]: https://github.com/fantaisie-software/purebasic-repository-template "Visit the PureBasic Repository Template project on GitHub"

> ## No Copyright
>
> The person who associated a work with this deed has dedicated the work to the public domain by waiving all of his or her rights to the work worldwide under copyright law, including all related and neighboring rights, to the extent allowed by law.
>
> You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission. See __Other Information__ below.
>
> ### Other Information
>
> * In no way are the patent or trademark rights of any person affected by CC0, nor are the rights that other persons may have in the work or in how the work is used, such as [publicity or privacy rights].
> * Unless expressly stated otherwise, the person who associated a work with this deed makes no warranties about the work, and disclaims liability for all uses of the work, to the fullest extent permitted by applicable law.
> * When using or citing the work, you should not imply [endorsement] by the author or the affirmer.

[publicity or privacy rights]: https://creativecommons.org/faq/#what-are-publicity-personality-and-privacy-rights
[endorsement]: https://creativecommons.org/faq/#do-i-need-to-be-aware-of-anything-else-when-providing-attribution

# PureBasic Links

- [PureBasic website]
- [PureBasic Forum English]
- [PureBasic Forum French]
- [PureBasic Forum German]
- [PureBasic Documentation]
- [Fantaisie Software on GitHub]

<!-----------------------------------------------------------------------------
                               REFERENCE LINKS
------------------------------------------------------------------------------>

<!-- PureBasic -->

[PureBasic]: https://www.purebasic.com "Visit the PureBasic website"
[PureBasic website]: https://www.purebasic.com "Visit the PureBasic website"
[PureBasic Forum English]: https://www.purebasic.fr/english/ "Visit the PureBasic English Forum"
[PureBasic Forum French]: https://www.purebasic.fr/french/ "Visit the PureBasic French Forum"
[PureBasic Forum German]: https://www.purebasic.fr/german/ "Visit the PureBasic German Forum"
[PureBasic Documentation]: https://www.purebasic.com/documentation/index.html "Go to the online PureBasic Documentation"
[Fantaisie Software on GitHub]: https://github.com/fantaisie-software "Fantaisie Software GitHub profile"

<!-- EOF -->
