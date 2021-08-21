---
description: La table TypeLib contient les informations qui doivent être placées dans l’enregistrement du registre des bibliothèques de types.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Table TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862bc37e325f8c615e8158cfa431c927841f6b33c403c804726cea8fee6f0469
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499999"
---
# <a name="typelib-table"></a>Table TypeLib

La table TypeLib contient les informations qui doivent être placées dans l’enregistrement du registre des bibliothèques de types.

La table TypeLib contient les colonnes suivantes.



| Colonne      | Type                               | Clé | Nullable |
|-------------|------------------------------------|-----|----------|
| LibID       | [GUID](guid.md)                   | O   | N        |
| Langage    | [Integer](integer.md)             | O   | N        |
| Composant\_ | [Identificateur](identifier.md)       | O   | N        |
| Version     | [DoubleInteger](doubleinteger.md) | N   | O        |
| Description | [Text](text.md)                   | N   | O        |
| Répertoire\_ | [Identificateur](identifier.md)       | N   | O        |
| Caractéristique\_   | [Identificateur](identifier.md)       | N   | N        |
| Coût        | [DoubleInteger](doubleinteger.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID
</dt> <dd>

GUID qui identifie la bibliothèque.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous
</dt> <dd>

Langage de la bibliothèque de types. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table des composants](component-table.md). Cette colonne identifie le composant appartenant à \_ la fonctionnalité dont le fichier de clé est la bibliothèque de types en cours d’enregistrement.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version
</dt> <dd>

Il s’agit de la version de la bibliothèque. Les versions majeure et mineure sont encodées dans la valeur entière de quatre octets. La version mineure est dans les huit bits inférieurs. La version principale est au milieu de seize bits.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Description localisable de la bibliothèque.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Clé externe dans la première colonne de la [table de répertoires](directory-table.md). Cette colonne identifie le chemin d’accès de l’aide pour la bibliothèque de types. Cette colonne est ignorée lors de la publicité.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_
</dt> <dd>

Clé externe dans la première colonne du [tableau des fonctionnalités](feature-table.md). Cette colonne spécifie la fonctionnalité qui doit être installée pour que la bibliothèque de types soit opérationnelle.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Coûts
</dt> <dd>

Coût associé à l’inscription de la bibliothèque de types en octets. Il doit s’agir d’un nombre non négatif ou d’une valeur null.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette table est référencée lorsque l' [action RegisterTypeLibraries](registertypelibraries-action.md) ou l' [action UnregisterTypeLibraries](unregistertypelibraries-action.md) est exécutée.

Le programme d’installation écrit toutes les informations d’inscription de la bibliothèque de types dans l' \_ emplacement de Registre HKEY local \_ machine (HKLM). C’est le cas même pour les installations par utilisateur. Les bibliothèques de types ne peuvent pas être inscrites dans des emplacements par utilisateur (HKCU).

Les auteurs de packages d’installation sont fortement recommandés par rapport à l’utilisation de la table TypeLib. Au lieu de cela, ils doivent inscrire les bibliothèques de types à l’aide de la table [du Registre](registry-table.md) . Voici quelques raisons pour lesquelles éviter l’inscription automatique :

-   Si une installation qui utilise la table TypeLib échoue et doit être restaurée, la restauration peut ne pas restaurer l’état de l’ordinateur qui existait avant la restauration. Les bibliothèques de types inscrites avant la restauration ne peuvent pas être inscrites après la restauration.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
</dl>

 

 



