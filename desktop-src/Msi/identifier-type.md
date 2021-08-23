---
description: Le type d’identificateur du type sémantique est l’un des types de format texte.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Type d’identificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1061f6d813b0803dbe1aa0d8e49e7f93cffba6e100f778901441f4bc4ed710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634780"
---
# <a name="identifier-type"></a>Type d’identificateur

Le type d’identificateur du [type sémantique](semantic-types.md) est l’un des [types de format texte](text-format-types.md). ce type est constitué d’une chaîne de texte fournie par l’utilisateur au format d’un [identificateur](identifier.md)de Windows Installer. L’outil de fusion remplace cette chaîne dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format, entrer « identificateur » dans la colonne type et laisser vide la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La chaîne peut être dans n’importe quel langage compatible avec la page de codes de la base de données. consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md). NULL est une valeur valide pour la chaîne de texte, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.

 

 



