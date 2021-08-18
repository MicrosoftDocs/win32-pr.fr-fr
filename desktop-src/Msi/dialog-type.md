---
description: Le type de dialogue de type sémantique est l’un des types de format de clé. Ce type se compose d’une clé étrangère dans la table de boîtes de dialogue fournie par l’utilisateur.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Type de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f945b499cfab5ca8b3bf85180c16d9be88f4093b258513a11b5059874cb403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764019"
---
# <a name="dialog-type"></a>Type de dialogue

Le type de dialogue de [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md). Ce type se compose d’une clé étrangère dans la [table de boîtes de dialogue](dialog-table.md) fournie par l’utilisateur.

l’outil de fusion doit substituer un [identificateur](identifier.md) de Windows Installer valide pour les éléments de ce type. Mergemod.dll n’applique pas cette restriction et c’est à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table de dialogue.

NULL est une valeur valide pour ce type, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la [table ModuleConfiguration](moduleconfiguration-table.md).

Le type de dialogue peut être utilisé avec les types de ContextData suivants.

**DialogNext ContextData**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère dans la table de boîtes de dialogue. Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « boîte de dialogue » dans la colonne type et entrer « DialogNext » dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).

**DialogPrev ContextData**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère dans la table de boîtes de dialogue. Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « boîte de dialogue » dans la colonne type et entrer « DialogPrev » dans la colonne ContextData de la table ModuleConfiguration.

 

 



