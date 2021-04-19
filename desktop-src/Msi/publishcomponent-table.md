---
description: La table PublishComponent associe les composants listés dans la table de composants à une chaîne de texte de qualificateur et un GUID d’ID de catégorie.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Table PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531930"
---
# <a name="publishcomponent-table"></a>Table PublishComponent

La table PublishComponent associe les composants listés dans la [table de composants](component-table.md) à une chaîne de texte de qualificateur et un GUID d’ID de catégorie. Les composants avec des fonctionnalités parallèles qui ont été regroupées de cette façon sont appelés composants qualifiés. Consultez [composants qualifiés](qualified-components.md). Cela fournit au programme d’installation une méthode pour l’indirection d’un seul niveau lorsqu’il fait référence aux composants. Consultez [utilisation des composants qualifiés](using-qualified-components.md).

La table PublishComponent contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| ComponentId | [GUID](guid.md)             | O   | N        |
| Qualificateur   | [Text](text.md)             | O   | N        |
| -\_ | [Identificateur](identifier.md) | O   | N        |
| AppData     | [Text](text.md)             | N   | O        |
| Fonctionnalité\_   | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

[GUID](guid.md) de chaîne qui représente la catégorie des composants regroupés. Notez que le titre de cette colonne est trompeur. Il s’agit du GUID de la catégorie des composants qualifiés et qui n’est pas le même GUID que celui figurant dans la colonne ComponentId de la [table des composants](component-table.md). Ici, il fait référence à un serveur qui fournit les fonctionnalités d’un composant à des clients externes plutôt qu’au composant lui-même.

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualificateur
</dt> <dd>

Chaîne de texte qui qualifie la valeur dans la colonne ComponentId. Un qualificateur est utilisé pour distinguer plusieurs formes du même composant, par exemple un composant implémenté dans plusieurs langues. Il s’agit des chaînes de texte de qualificateur retournées par [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la colonne une de la [table des composants](component-table.md). Cet identificateur fait référence à l’enregistrement du composant qualifié dans la table des composants.

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData
</dt> <dd>

Texte localisable facultatif qui décrit le composant qualifié de cet enregistrement. La chaîne est généralement analysée par l’application et peut être affichée à l’utilisateur. Il doit décrire le composant qualifié. Ce peut être récupéré avec [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_
</dt> <dd>

Clé externe dans la colonne une du [tableau des fonctionnalités](feature-table.md). Il s’agit de la fonctionnalité qui utilise ce composant qualifié.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table est référencée lorsque l' [action PublishComponents](publishcomponents-action.md) ou l' [action UnpublishComponents](unpublishcomponents-action.md) est exécutée.

Notez que le nom de cette table est trompeur. Cette table n’est pas nécessaire pour créer la publication. Pour plus d’informations sur la façon de définir l’état d’installation des composants à publier, consultez la colonne attributs de la table des [composants](component-table.md) et de la [table des fonctionnalités](feature-table.md) .

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



