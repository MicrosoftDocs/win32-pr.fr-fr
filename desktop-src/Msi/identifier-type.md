---
description: Le type d’identificateur du type sémantique est l’un des types de format texte.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Type d’identificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021403"
---
# <a name="identifier-type"></a>Type d’identificateur

Le type d’identificateur du [type sémantique](semantic-types.md) est l’un des [types de format texte](text-format-types.md). ce type est constitué d’une chaîne de texte fournie par l’utilisateur au format d’un [identificateur](identifier.md)de Windows Installer. L’outil de fusion remplace cette chaîne dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format, entrer « identificateur » dans la colonne type et laisser vide la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La chaîne peut être dans n’importe quel langage compatible avec la page de codes de la base de données. consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md). NULL est une valeur valide pour la chaîne de texte, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.

 

 



