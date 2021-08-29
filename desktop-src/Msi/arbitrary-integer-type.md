---
description: Le type d’entier arbitraire du type sémantique est l’un des types de format d’entier.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Type d’entier arbitraire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b965b623d2a0a213335086e9139a621fc093fc18bea2d1873faf68e4f24f2961
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821829"
---
# <a name="arbitrary-integer-type"></a>Type d’entier arbitraire

Le type d’entier arbitraire du [type sémantique](semantic-types.md) est l’un des [types de format d’entier](integer-format-types.md). Ce type d’élément configurable est un entier fourni par l’utilisateur. L’outil de fusion remplace cet entier dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 2 » dans la colonne format et laisser vides les colonnes type et ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). Les colonnes type et ContextData sont réservées et doivent avoir la valeur null.

 

 



