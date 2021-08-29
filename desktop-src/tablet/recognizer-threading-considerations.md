---
description: Bien qu’un&\# 160 ; contexte de reconnaissance&\# 160 ; ne soit pas accessible sur deux threads simultanément par la plateforme Tablet PC, la fonction AdviseInkChange peut être appelée à tout moment sur n’importe quel thread.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Considérations sur les threads de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f28f387a0073eab7b85250d02d3983f83c3e9633c955d0f5503c06766745ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843339"
---
# <a name="recognizer-threading-considerations"></a>Considérations sur les threads de reconnaissance

Bien qu’un contexte de module de [reconnaissance](hrecocontext-handle.md) ne soit pas accessible sur deux threads simultanément par la plateforme Tablet PC, la fonction [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) peut être appelée à tout moment sur n’importe quel thread. Étant donné que la plateforme Tablet PC ne garantit pas qu’il n’existe qu’un seul contexte de reconnaissance à la fois, deux contextes de reconnaissance distincts dans des threads distincts peuvent tenter d’accéder simultanément à votre module de [reconnaissance](hrecognizer-handle.md). Par conséquent, les variables globales de votre moteur de reconnaissance doivent être thread-safe.

Les listes de mots sont une implémentation facultative qui permet d’améliorer la précision. Si votre module de reconnaissance implémente des listes de mots, il doit être thread-safe. Pour plus d’informations sur l’utilisation des listes de mots, consultez [utilisation de dictionnaires d’applications](using-application-dictionaries.md).

Pour plus d’informations sur les autres considérations relatives aux threads, consultez Considérations sur les [Threads Tablet PC](tablet-pc-threading-considerations.md).

 

 



