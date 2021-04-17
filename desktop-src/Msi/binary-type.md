---
description: Le type binaire de type sémantique est l’un des types de format de clé. Ce type est constitué d’une clé dans la table binaire fournie par l’utilisateur.
ms.assetid: b6a25100-9f3e-4207-b56f-0c27ee16f188
title: Type binaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda0711b53f865bbd844514ed2429d97d91e07a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528858"
---
# <a name="binary-type"></a>Type binaire

Le type binaire de [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md). Ce type est constitué d’une clé dans la [table binaire](binary-table.md) fournie par l’utilisateur.

L’outil de fusion doit substituer un [identificateur](identifier.md) de Windows Installer valide pour les éléments de ce type. Mergemod.dll n’applique pas cette restriction et c’est à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table binaire.

NULL est une valeur valide pour ce type, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la [table ModuleConfiguration](moduleconfiguration-table.md).

Le type binaire peut être utilisé avec les types de ContextData suivants.

**ContextData bitmap**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère à une ligne de la table binaire qui contient une image bitmap. Mergmod.dll ne garantit pas une taille ou un type de bitmap spécifique et l’outil de fusion doit s’assurer que les données sont une image valide. Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « binaire » dans la colonne Type, puis entrer « bitmap » dans la colonne ContextData de la table ModuleConfiguration.

**Icône ContextData**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère à une ligne de la table binaire qui contient une image d’icône. Mergmod.dll ne garantit pas une taille ou un type d’icône spécifique et l’outil de fusion doit s’assurer que les données sont une image valide. Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « binaire » dans la colonne type et entrer « Icon » dans la colonne ContextData de la table ModuleConfiguration. Ce type n’est pas approprié pour une utilisation dans une table de publication.

**EXE ContextData**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère à une ligne de la table binaire qui contient une image exécutable 32 bits. Mergmod.dll ne valide pas les données sont valides et l’outil de fusion doit s’assurer que les données sont un fichier PE valide. Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « binaire » dans la colonne type et entrer « EXE » dans la colonne ContextData de la table ModuleConfiguration.

**EXE64 ContextData**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir une clé étrangère à une ligne de la table binaire qui contient une image exécutable 32 bits ou 64 bits. Mergmod.dll ne valide pas les données sont valides et l’outil de fusion doit s’assurer que les données sont un fichier PE valide. Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément configurable dans la colonne nom, entrer « 1 » dans la colonne format, entrer « binaire » dans la colonne Type, puis entrer « EXE64 » dans la colonne ContextData de la table ModuleConfiguration.

 

 



