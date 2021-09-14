---
description: ICE88 vérifie que le répertoire référencé dans la colonne DirProperty de la table IniFile existe dans le package Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021466"
---
# <a name="ice88"></a>ICE88

ICE88 vérifie que le répertoire référencé dans la colonne DirProperty de la [table IniFile](inifile-table.md) existe dans le package Windows Installer. ICE88 émet un avertissement si la valeur DirProperty ne représente pas une propriété dans les tables Directory, AppSearch ou Property, certaines [Propriétés du dossier système](property-reference.md)ou une propriété définie par une action personnalisée de type 51.

ICE88 analyse les tables et les propriétés suivantes.

-   [Table de répertoire](directory-table.md)
-   [Table AppSearch](appsearch-table.md)
-   [Table de propriétés](property-table.md)
-   [Table CustomAction](customaction-table.md) , où l’action personnalisée est un [type d’action personnalisé 51](custom-action-type-51.md)
-   [**Propriété ProgramFilesFolder**](programfilesfolder.md)
-   [**Propriété CommonFilesFolder**](commonfilesfolder.md)
-   [**Propriété SystemFolder**](systemfolder.md)
-   [**Propriété ProgramFiles64Folder**](programfiles64folder.md)
-   [**Propriété CommonFiles64Folder**](commonfiles64folder.md)
-   [**Propriété System64Folder**](system64folder.md)

## <a name="result"></a>Résultats

ICE88 publie l’avertissement suivant.



| AVERTISSEMENT ICE88                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dans l’entrée de table IniFile (IniFile =) \[ 3, \] DirProperty = \[ 1 \] est introuvable dans les tables Directory/Property/AppSearch/ca-Type51 et il ne s’agit pas de l’une des propriétés du programme d’installation. | Pour chaque enregistrement de la table IniFile, ICE88 lit la valeur dans la colonne DirProperty. ICE88 recherche la valeur dans la table de [répertoire](directory-table.md), la [table AppSearch](appsearch-table.md)et la [table de propriétés](property-table.md) , et analyse également la liste des propriétés définies par le programme d’installation. ICE88 publie cet avertissement si la valeur est introuvable dans l’analyse. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



