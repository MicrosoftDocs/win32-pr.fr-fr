---
description: '&\# 0034 ; Le champ \# de bits&0034 ; type sans demande de contexte que l’utilisateur fournisse un entier dont la valeur est utilisée pour définir un ou plusieurs bits dans un champ de bits. Ce texte peut être dans n’importe quelle langue compatible avec la page de codes de la base de données.'
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Type de champ de type binaire arbitraire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842c9d1725b2bfe9ef0585cafd085ac1ceba33554899909ae3317af38fd7caac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381383"
---
# <a name="arbitrary-bitfield-type"></a>Type de champ de type binaire arbitraire

Le type « champ de bits » sans demande de contexte indique que l’utilisateur fournit un entier dont la valeur est utilisée pour définir un ou plusieurs bits dans un champ de bits. Ce texte peut être dans n’importe quelle langue compatible avec la page de codes de la base de données.

Le type de champ de type binaire aléatoire du [type de sémantique](semantic-types.md) est l’un des types de champ de type binaire. Ce type est constitué d’un entier choisi par l’utilisateur à partir d’un ensemble de choix. L’outil de fusion remplace l’entier sélectionné dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md). Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de l’élément dans la colonne nom, entrer « 3 » dans la colonne format, laisser la colonne type vide et entrer la liste des entiers possibles dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).

La colonne de type est réservée et doit avoir la valeur null. L’entrée dans la colonne ContextData pour tous les types de format de champ de format binaire doit se présenter sous la forme " <mask> ;<Name>=<value>;<Name>=<value>....», où <mask> est une valeur entière indiquant les bits d’intérêt, <Name> est un nom complet localisable pour le choix, et <value> valeur entière décimale. La colonne de contexte est en cours d’utilisation [CMSM spécial format](cmsm-special-format.md) et pour tous les types de champ de type champ. Un caractère littéral « = » ou « ; » peut être entré dans le <Name> champ en le faisant précéder d’une barre oblique inverse (« \\ »).

 

 



