---
description: Le type d’entier arbitraire du type sémantique est l’un des types de format d’entier.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Type d’entier arbitraire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115378"
---
# <a name="arbitrary-integer-type"></a>Type d’entier arbitraire

Le type d’entier arbitraire du [type sémantique](semantic-types.md) est l’un des [types de format d’entier](integer-format-types.md). Ce type d’élément configurable est un entier fourni par l’utilisateur. L’outil de fusion remplace cet entier dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 2 » dans la colonne format et laisser vides les colonnes type et ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). Les colonnes type et ContextData sont réservées et doivent avoir la valeur null.

 

 



