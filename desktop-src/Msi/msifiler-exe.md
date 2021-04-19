---
description: MsiFiler.exe remplit la table de fichiers avec des versions de fichier, des langues et des tailles basées sur un répertoire source. Il peut également mettre à jour la table MsiFileHash avec des hachages de fichier.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515009"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe remplit la [table de fichiers](file-table.md) avec des versions de fichier, des langues et des tailles basées sur un répertoire source. Il peut également mettre à jour la [table MsiFileHash](msifilehash-table.md) avec des hachages de fichier.

## <a name="syntax"></a>Syntaxe

**msifiler.exe-d** *{base de données}* **\[ -v \] \[ -h \] \[ -s \] altsource**

## <a name="command-line-options"></a>Options de la ligne de commande

Msifiler.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse. Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.



| Option | Paramètre   | Description                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | La base de données (fichier. msi) à mettre à jour.                                                                                                                              |
| -v     |             | Utilisez le mode détaillé.                                                                                                                                                            |
| -H     |             | Remplissez la [table MsiFileHash](msifilehash-table.md). La table est créée si elle n’existe pas déjà. La table MsiFileHash peut uniquement être utilisée avec des fichiers sans version. |
| -S     | *Altsource* | Altsource spécifie un autre répertoire pour rechercher les fichiers.                                                                                                              |



 

Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de développement Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Utilisation de la table Directory](using-the-directory-table.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



