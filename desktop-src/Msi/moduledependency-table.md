---
description: La table ModuleDependency conserve une liste d’autres modules de fusion requis pour que ce module de fusion fonctionne correctement.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Table ModuleDependency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524284"
---
# <a name="moduledependency-table"></a>Table ModuleDependency

La table ModuleDependency conserve une liste d’autres modules de fusion requis pour que ce module de fusion fonctionne correctement. Cette table active un outil de fusion ou de vérification pour s’assurer que les modules de fusion nécessaires sont en fait inclus dans la base de données du programme d’installation de l’utilisateur. L’outil vérifie en faisant référence à cette table à l’aide de la table ModuleSignature dans la base de données du programme d’installation.

La table ModuleDependency contient les colonnes suivantes.



| Colonne           | Type                         | Clé | Nullable |
|------------------|------------------------------|-----|----------|
| ModuleID         | [Identificateur](identifier.md) | O   | N        |
| ModuleLanguage   | [Integer](integer.md)       | O   | N        |
| RequiredID       | [Identificateur](identifier.md) | O   | N        |
| RequiredLanguage | [Integer](integer.md)       | O   | N        |
| RequiredVersion  | [Version](version.md)       |     | O        |



 

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

<span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID
</dt> <dd>

Identificateur du module de fusion requis par le module de fusion dans ModuleID.

</dd> <dt>

<span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage
</dt> <dd>

ID de langue numérique du module de fusion dans RequiredID. La colonne RequiredLanguage peut spécifier l’ID de langue pour une seule langue, par exemple 1033 pour l’anglais des États-Unis, ou spécifier l’ID de langue d’un groupe de langues, par exemple 9 pour l’anglais. Si le champ contient un ID de langue de groupe, tout module de fusion avec un code de langue dans ce groupe est conforme à la dépendance. Si RequiredLanguage a la valeur 0, tout module de fusion remplissant les autres conditions requises est conforme à la dépendance.

</dd> <dt>

<span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion
</dt> <dd>

Version du module de fusion dans RequiredID. Si ce champ a la valeur null, toute version remplit la dépendance.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



