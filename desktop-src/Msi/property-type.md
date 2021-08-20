---
description: Le type de propriété de type sémantique est l’un des types de format de clé. Ce type se compose d’une clé étrangère dans la table de propriétés fournie par l’utilisateur.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Type de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6446b5a0ef5f2cf1bc969f531a3b8c35e6990a2ca3eee3c0002e4f62fbf4cea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145332"
---
# <a name="property-type"></a>Type de propriété

Le type de propriété de [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md). Ce type se compose d’une clé étrangère dans la [table de propriétés](property-table.md) fournie par l’utilisateur.

l’outil de fusion doit substituer un [identificateur](identifier.md) de Windows Installer valide pour les éléments de ce type. Mergemod.dll n’applique pas cette restriction et c’est à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table de propriétés. Les clés primaires de la table de propriétés sont les noms de propriété.

NULL est une valeur valide pour ce type, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la [table ModuleConfiguration](moduleconfiguration-table.md).

Le type de propriété peut être utilisé avec les types de ContextData suivants.

**ContextData null**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir un nom de propriété à une table de base de données dans le module. L’outil Merge Tool remplace l’identificateur de la propriété dans les modèles de la colonne value de la [table ModuleSubstitution](modulesubstitution-table.md). Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « propriété » dans la colonne type et laisser vide la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).

**ContextData public**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir le nom d’une [propriété publique](public-properties.md) à une table de base de données dans le module. L’outil Merge Tool remplace l’identificateur de la propriété dans les modèles de la colonne value de la [table ModuleSubstitution](modulesubstitution-table.md). Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « propriété » dans la colonne Type, puis entrer « public » dans la colonne ContextData de la table ModuleConfiguration.

**ContextData privé**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir le nom d’une [propriété privée](private-properties.md) à une table de base de données dans le module. L’outil Merge Tool remplace l’identificateur de la propriété dans les modèles de la colonne value de la [table ModuleSubstitution](modulesubstitution-table.md). Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « propriété » dans la colonne Type, puis entrer « Private » dans la colonne ContextData de la table ModuleConfiguration.

 

 



