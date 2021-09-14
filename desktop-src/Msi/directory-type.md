---
description: Le type de répertoire de type sémantique est l’un des types de format de clé, qui se compose d’une clé étrangère dans la table de répertoires fournie par l’utilisateur.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Type de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091570"
---
# <a name="directory-type"></a>Type de répertoire

Le type de répertoire de [type sémantique](semantic-types.md) est l’un des [types de format de clé](key-format-types.md), qui se compose d’une clé étrangère dans la table de [répertoires](directory-table.md) fournie par l’utilisateur.

l’outil de fusion doit substituer un [identificateur](identifier.md) de Windows Installer valide pour les éléments de ce type. Mergemod.dll n’applique pas cette restriction et c’est à l’outil de fusion de s’assurer que l’utilisateur fournit une clé valide dans la table de répertoires.

Un élément configurable du type de répertoire doit uniquement modifier le répertoire de destination de l’installation et ne pas modifier l’image source. Un élément configurable de ce type doit donc uniquement modifier les clés étrangères de la table de répertoires et ne pas modifier directement la table de répertoires.

Étant donné que la \_ colonne de répertoire de la [table de composants](component-table.md) n’accepte pas les valeurs NULL, la valeur NULL n’est pas une valeur valide pour un élément configurable de ce type, même si le msmConfigItemNonNullable n’est pas défini dans la colonne attributs.

Le type de répertoire peut être utilisé avec deux types de ContextData.

**IsolationDirectory ContextData**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir un répertoire de destination pour les fichiers dans le module. L’outil Merge Tool remplace l’identificateur de l’annuaire dans les modèles de la colonne value de la [table ModuleSubstitution](modulesubstitution-table.md). Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom du répertoire dans la colonne nom, entrer « 1 » dans la colonne format, entrer « répertoire » dans la colonne type et entrer « IsolationDirectory » dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).

**ShortcutLocation ContextData**

Un module de fusion configurable peut utiliser ce type pour permettre à l’utilisateur de fournir un répertoire de destination pour les raccourcis dans le module. L’outil Merge Tool remplace l’identificateur du raccourci dans les modèles de la colonne value de la [table ModuleSubstitution](modulesubstitution-table.md). Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom du répertoire dans la colonne nom, entrer « 1 » dans la colonne format, entrer « répertoire » dans la colonne type et entrer « ShortcutLocation » dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).

 

 



