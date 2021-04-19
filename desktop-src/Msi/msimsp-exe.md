---
description: La méthode recommandée pour générer un package de correctif consiste à utiliser des outils de création de correctifs tels que Msimsp.exe et Patchwiz.dll. L’outil Msimsp.exe est disponible uniquement dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106520249"
---
# <a name="msimspexe"></a>Msimsp.exe

La méthode recommandée pour générer un package de correctif consiste à utiliser des outils de création de correctifs tels que Msimsp.exe et [Patchwiz.dll](patchwiz-dll.md). L’outil Msimsp.exe est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Msimsp.exe est un fichier exécutable qui appelle [Patchwiz.dll](patchwiz-dll.md). L’outil peut être utilisé pour créer un package de correctifs en passant le chemin d’accès à un fichier de propriétés de création de correctifs (fichier. PCP) et le chemin d’accès au package de correctifs en cours de création. Msimsp. ex peut également être utilisé pour créer un fichier journal et pour spécifier un dossier temporaire dans lequel les transformations, les armoires et les fichiers utilisés pour créer le package de correctif sont enregistrés.

La syntaxe de la ligne de commande pour Msimsp.exe est :

**Msimsp.exe-s** *\[ chemin d’accès au fichier \] . PCP* **-p** *\[ chemin d’accès \] au fichier. msp* **{options}**

Les options de ligne de commande ne respectent pas la casse, et les séparateurs de barres obliques peuvent être utilisés à la place d’un tiret. Si aucune option n’est spécifiée, Msimsp.exe affiche les valeurs actuelles des propriétés des informations de résumé.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ chemin d’accès au fichier \] . PCP_
</dt> <dd>

Cette valeur est obligatoire et doit être suivie du chemin d’accès au fichier de propriétés de création de correctifs (extension. PCP). Pour plus d’informations, consultez [PatchWiz.dll](patchwiz-dll.md).

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_chemin d’accès au fichier. msp_
</dt> <dd>

Cette valeur est obligatoire et suivie du chemin d’accès au package de correctifs en cours de création (extension. msp).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_chemin d’accès au dossier temporaire_
</dt> <dd>

Optionnel. Suivi du chemin d’accès au dossier temporaire. L’emplacement par défaut est% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

Optionnel. Échoue si le dossier temporaire existe déjà.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_chemin du fichier journal_
</dt> <dd>

Optionnel. Suivi du chemin d’accès au fichier journal décrivant le processus de création des correctifs et les erreurs. Pour plus d’informations, consultez [valeurs de retour pour UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-**_chemin d’accès LP au fichier journal avec les données de performances_
</dt> <dd>

Optionnel. Suivi du chemin d’accès au fichier journal décrivant le processus de création des correctifs et les erreurs. Cette option permet d’écrire les données de performances dans le fichier journal. Cette option requiert la version 4,0 de Patchwiz.dll.

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Optionnel. Affiche une boîte de dialogue si la création du correctif se termine correctement.

</dd> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Affiche l'aide de la ligne de commande.

</dd> </dl>

> [!Note]
> Msimsp.exe peut échouer lorsqu’il appelle Makecab.exe s’il existe des valeurs dans la colonne fichier de la [table de fichiers](file-table.md) du package d’installation qui diffèrent uniquement par la casse. Windows Installer est sensible à la casse et permet à un package d’installation comme dans le tableau ci-dessous uniquement lorsque COMP1 et Comp2 sont installés dans des répertoires différents. Toutefois, dans ce scénario, vous ne pouvez pas utiliser Msimsp.exe ou [Patchwiz.dll](patchwiz-dll.md) pour générer un correctif pour le package, car Msimsp.exe et Patchwiz.dll appellent Makecab.exe, ce qui ne respecte pas la casse.
> 
> Évitez de créer un package d’installation, tel que la [table de fichiers](file-table.md)partielle suivante.
> 
> | Fichier       | -\_ | FileName   |
> |------------|-------------|------------|
> | readme.txt | COMP1       | readme.txt |
> | ReadMe.txt | COMP2       | readme.txt |


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un package de correctifs](creating-a-patch-package.md)
</dt> <dt>

[Exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md)
</dt> <dt>

[Outils de développement Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



