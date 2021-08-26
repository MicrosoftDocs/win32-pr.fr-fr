---
title: Handles de contexte strict et strict
description: Utilisez l' \_ \_ attribut de handle de contexte strict pour tous les descripteurs de contexte.
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91c266fb70b540e08d066e51f61a921b8f88819456e83b909e3be31bb1f518c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017509"
---
# <a name="strict-and-type-strict-context-handles"></a>Handles de contexte strict et strict

Utilisez l’attribut de [**\_ \_ handle de contexte strict**](/windows/desktop/Midl/strict-context-handle) pour tous les descripteurs de contexte. Par défaut, un handle de contexte n’est pas associé à une interface, ce qui signifie qu’un handle de contexte peut être créé sur une interface, puis passé à un autre. Il s’agit d’une attaque simple, et de nombreux serveurs RPC ne peuvent pas l’empêcher.

Si deux interfaces coexistent dans le même processus, une personne malveillante peut ouvrir un descripteur de contexte sur une interface et la passer à une autre, ce qui peut traverser les données inattendues. De nombreux développeurs pensent que leurs logiciels sont la seule interface d’un processus, mais très souvent, ce n’est pas le cas, car le système et de nombreux composants tiers utilisent RPC en interne, et ces interfaces peuvent créer des handles de contexte. Lorsque l’attribut de [**\_ \_ handle de contexte strict**](/windows/desktop/Midl/strict-context-handle) est utilisé, le temps d’exécution RPC garantit qu’un contexte créé sur une interface peut être passé comme argument uniquement aux méthodes de cette interface.

dans les cas où une application est développée pour Windows Vista, l’utilisation d’un [**\_ \_ \_ handle de contexte strict**](/windows/desktop/Midl/type-strict-context-handle) est disponible et recommandée. Les handles de contexte ne sont pas associés à un type spécifique par défaut. Lorsque plusieurs types de handles de contexte sont utilisés dans le même processus, un client malveillant peut passer un handle de contexte à la place d’un autre pour produire des résultats indésirables. L’utilisation du **\_ handle de \_ contexte \_ strict** permet aux applications d’appliquer la cohérence des types de handles de contexte et d’empêcher toute utilisation incompatible de type de handle de contexte.

 

 