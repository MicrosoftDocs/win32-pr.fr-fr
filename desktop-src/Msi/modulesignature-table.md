---
description: La table ModuleSignature est une table obligatoire.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: ModuleSignature, table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529242"
---
# <a name="modulesignature-table"></a>ModuleSignature, table

La table ModuleSignature est une table obligatoire. Il contient toutes les informations nécessaires pour identifier un module de fusion. L’outil de fusion ajoute cette table au fichier. msi s’il n’en existe pas déjà une. La table ModuleSignature d’un module de fusion n’a qu’une seule ligne contenant le ModuleID, la langue et la version. Toutefois, la table ModuleSignature d’un fichier. msi contient une ligne contenant ces informations pour chaque fichier. msm qui a été fusionné dans celui-ci.

Les outils de fusion et de vérification vérifient la table ModuleSignature dans les fichiers. msi pour déterminer si elle contient tous les modules de fusion dépendants requis par le module de fusion actuel (consultez la [table ModuleDependency](moduledependency-table.md)) et si le package d’installation a été précédemment fusionné avec des modules de fusion en conflit (voir la [table ModuleExclusion](moduleexclusion-table.md)).

La table ModuleSignature contient les colonnes suivantes.



| Colonne   | Type                         | Clé | Nullable |
|----------|------------------------------|-----|----------|
| ModuleID | [Identificateur](identifier.md) | O   | N        |
| Language | [Integer](integer.md)       | O   | N        |
| Version  | [Version](version.md)       |     | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificateur qui identifie de façon unique le module de fusion. Deux modules de fusion ne peuvent pas avoir le même ModuleID, à moins que le module de fusion n’ait entièrement une compatibilité descendante avec son prédécesseur. Vous pouvez créer un GUID pour ce champ à l’aide d’un utilitaire tel que GUIDGEN. La colonne ModuleID est une clé primaire pour la table et doit donc respecter la Convention d’affectation de noms pour [nommer les clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md). Par exemple, si le nom lisible du module de fusion est MyLibrary et que le GUID est {880DE2F0-CDD8-11D1-A849-006097ABDE17}, l’entrée dans la colonne ModuleID devient MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous
</dt> <dd>

L’identificateur de langue spécifie la langue par défaut pour le module de fusion. L’identificateur de langue est au format décimal, par exemple, l’anglais des États-Unis est 1033. Le langage utilisé par le module de fusion peut être modifié en appliquant une transformation au module de fusion avant la fusion.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version
</dt> <dd>

Le champ version contient une chaîne qui décrit les versions majeures et mineures du module de fusion.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modules de fusion multilingues](multiple-language-merge-modules.md)
</dt> </dl>

 

 



