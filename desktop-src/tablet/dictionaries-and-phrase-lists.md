---
description: Le lexique, ou la liste des mots possibles utilisés par le modèle de langage d’un module de reconnaissance particulier, est contenu dans un ou plusieurs dictionnaires.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Dictionnaires et listes d’expressions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cc5b97918e1fed384494e887b604f1d08856e27232ed82f09bceff3ce14fe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110959"
---
# <a name="dictionaries-and-phrase-lists"></a>Dictionnaires et listes d’expressions

Le lexique, ou la liste des mots possibles utilisés par le modèle de langage d’un module de reconnaissance particulier, est contenu dans un ou plusieurs dictionnaires. Le module de reconnaissance recherche tous les dictionnaires disponibles sur le système lors de la compilation des correspondances de reconnaissance. Vous pouvez utiliser les API Microsoft Speech (SAPI) pour modifier certains de ces dictionnaires.

Une liste d’expressions fournit une autre méthode de modification du vocabulaire du module de reconnaissance. L’ajout de mots à une liste d’expressions étend le vocabulaire ; Ajouter des mots, puis contraindre le module de reconnaissance pour utiliser uniquement la liste d’expressions (contrairement à la liste d’expressions et aux dictionnaires), limite le vocabulaire.

Les versions précédentes des API de technologie Tablet PC reposaient sur le concept de listes de mots. Les listes de mots sont presque identiques aux listes d’expressions et sont utilisées dans le même but quand vous travaillez directement avec un objet [**RecognizerContext**](inkrecognizercontext-class.md) dans une application activée pour l’écriture manuscrite. Pour plus d’informations sur l’emplacement et le moment d’utilisation des listes de mots, consultez [définition du contexte pour les contrôles Ink-Enabled](setting-context-for-ink-enabled-controls.md).

Lorsque la taille de la liste avec laquelle vous souhaitez étendre le lexique dépasse 100 000 mots, nous vous recommandons d’utiliser un dictionnaire à la place d’une liste de mots ou d’expressions.

 

 



