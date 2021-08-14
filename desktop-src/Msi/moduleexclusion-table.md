---
description: La table ModuleExclusion conserve une liste d’autres modules de fusion qui sont incompatibles dans la même base de données de programme d’installation.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Table ModuleExclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 008d10e65d81b5668821e1a999cf08f5a10c55db3372a4b0230d560462a977c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996439"
---
# <a name="moduleexclusion-table"></a>Table ModuleExclusion

La table ModuleExclusion conserve une liste d’autres modules de fusion qui sont incompatibles dans la même base de données de programme d’installation. Cette table active un outil de fusion ou de vérification pour vérifier que les modules de fusion en conflit ne sont pas fusionnés dans la base de données du programme d’installation de l’utilisateur. L’outil vérifie en faisant référence croisée à cette table avec la table ModuleSignature dans la base de données du programme d’installation.

La table ModuleExclusion contient les colonnes suivantes.



| Colonne             | Type                         | Clé | Nullable |
|--------------------|------------------------------|-----|----------|
| ModuleID           | [Identificateur](identifier.md) | O   | N        |
| ModuleLanguage     | [Integer](integer.md)       | O   | N        |
| ExcludedID         | [Identificateur](identifier.md) | O   | N        |
| ExcludedLanguage   | [Integer](integer.md)       | O   | N        |
| ExcludedMinVersion | [Version](version.md)       |     | O        |
| ExcludedMaxVersion | [Version](version.md)       |     | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificateur du module de fusion. Il s’agit d’une clé étrangère dans la [table ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage
</dt> <dd>

ID de langue décimal du module de fusion dans ModuleID. Il s’agit d’une clé étrangère dans la [table ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID
</dt> <dd>

Identificateur d’un module de fusion exclu.

</dd> <dt>

<span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage
</dt> <dd>

ID de langue numérique du module de fusion dans ExcludedID. La colonne ExcludedLanguage peut spécifier l’ID de langue pour une seule langue, par exemple 1033 pour l’anglais des États-Unis, ou spécifier l’ID de langue d’un groupe de langues, par exemple 9 pour l’anglais. La colonne ExcludedLanguage peut accepter des ID de langue négatifs. La signification de la valeur dans la colonne ExcludedLanguage est la suivante.



| ExcludedLanguage | Signification                                                              |
|------------------|----------------------------------------------------------------------|
| > 0           | Excluez les ID de langue spécifiés par ExcludedLanguage.              |
| = 0              | Exclut aucun ID de langue.                                             |
| < 0           | Excluez tous les ID de langue, à l’exception de ceux spécifiés par ExcludedLanguage. |



 

</dd> <dt>

<span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion
</dt> <dd>

Version minimale exclue d’une plage. Si le champ ExcludedMinVersion a la valeur null, toutes les versions antérieures à ExcludedMaxVersion sont exclues. Si ExcludedMinVersion et ExcludedMaxVersion ont tous les deux la valeur null, il n’existe aucune exclusion basée sur la version.

</dd> <dt>

<span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion
</dt> <dd>

Version maximale exclue d’une plage. Si le champ ExcludedMaxVersion a la valeur null, toutes les versions après ExcludedMinVersion sont exclues. Si ExcludedMinVersion et ExcludedMaxVersion ont tous les deux la valeur null, il n’existe aucune exclusion basée sur la version.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



