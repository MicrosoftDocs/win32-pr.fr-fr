---
description: Le type de sémantique mis en forme est l’un des types de format texte.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Type mis en forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021707"
---
# <a name="formatted-type"></a>Type mis en forme

Le type de [sémantique](semantic-types.md) mis en forme est l’un des [types de format texte](text-format-types.md). ce type est constitué d’une chaîne de texte arbitraire de toute longueur fournie par l’utilisateur et au format texte mis en forme Windows Installer. Pour plus d’informations, consultez [formatée](formatted.md). L’outil de fusion remplace cette chaîne dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format, entrer « formaté » dans la colonne type et laisser vide la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La chaîne peut être dans n’importe quel langage compatible avec la page de codes de la base de données. pour plus d’informations, consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md). NULL est une valeur valide pour la chaîne de texte, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.

 

 



