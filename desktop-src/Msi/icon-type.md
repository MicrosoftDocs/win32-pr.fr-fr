---
description: Le type d’icône du type sémantique est l’un des types de format de clé. Ce type est constitué d’une clé dans la table d’icônes fournie par l’utilisateur.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Type d’icône
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28510eff674d1f25e632b1181943af70da73d9fc97a6a64ec5abd0807fe15cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634952"
---
# <a name="icon-type"></a>Type d’icône

Le type d’icône du [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md). Ce type est constitué d’une clé dans la [table d’icônes](icon-table.md) fournie par l’utilisateur.

l’outil de fusion doit substituer un [identificateur](identifier.md) de Windows Installer valide pour les éléments de ce type. Mergemod.dll n’applique pas cette restriction et c’est à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table d’icônes.

NULL est une valeur valide pour ce type, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la [table ModuleConfiguration](moduleconfiguration-table.md).

Le type binaire peut être utilisé avec les types de ContextData suivants.

**ShortcutIcon ContextData**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère à une ligne dans la [table d’icônes](icon-table.md) qui contient une image pouvant être utilisée comme icône de raccourci. Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « Icon » dans la colonne de type et entrer « ShorcutIcon » dans la colonne ContextData de la table ModuleConfiguration. Ce type n’est pas approprié pour une utilisation dans une table d’interface utilisateur. Pour modifier une clé de la table d’icônes de ces tables, consultez icône ContextData sous [type binaire](binary-type.md).

 

 



