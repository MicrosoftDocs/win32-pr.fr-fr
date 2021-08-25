---
description: Le type enum de type sémantique est l’un des types de format texte.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Type enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c5df6b0f76cc789c148e841827a75e7184aca2892d7d6e2233843e26aac80f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869319"
---
# <a name="enum-type"></a>Type enum

Le type enum de [type sémantique](semantic-types.md) est l’un des [types de format texte](text-format-types.md). Ce type est constitué d’une chaîne de texte choisie par l’utilisateur à partir d’un ensemble de choix. L’outil de fusion remplace la chaîne sélectionnée sélectionnée dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 0 » dans la colonne format, entrer « enum » dans la colonne Type, puis entrer la liste des chaînes possibles dans la colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md). La liste des chaînes possibles doit être fournie sous la forme d’une liste de chaînes Deliminated par des points-virgules. Chaque choix doit se présenter sous la forme « nom = valeur ». Un point-virgule littéral peut être ajouté à la valeur en ajoutant un caractère barre oblique inverse au point-virgule. NULL est une valeur valide, sauf si msmConfigItemNonNullable a été inclus dans le champ Attributes de la table ModuleConfiguration.

 

 



