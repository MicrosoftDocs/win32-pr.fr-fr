---
description: Le type de texte arbitraire du type sémantique est l’un des types de format texte.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Type de texte arbitraire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092626"
---
# <a name="arbitrary-text-type"></a>Type de texte arbitraire

Le type de texte arbitraire du [type sémantique](semantic-types.md) est l’un des [types de format texte](text-format-types.md). Ce type est constitué d’une chaîne de texte arbitraire de n’importe quelle longueur fournie par l’utilisateur. L’outil de fusion remplace cette chaîne arbitraire dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format et laisser vides les colonnes type et ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La chaîne de texte arbitraire peut être dans n’importe quel langage compatible avec la page de codes de la base de données. pour plus d’informations, consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md). NULL est une valeur valide pour la chaîne de texte, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.

 

 



