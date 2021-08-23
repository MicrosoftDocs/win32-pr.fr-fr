---
description: le terminal de diffusion multimédia en continu (MST) est un terminal dynamique basé sur l’utilisation de filtres de DirectShow. Un MSP écrit à l’aide des classes de base TAPI 3 MSP intègre un MST, mais les créateurs de MSP peuvent choisir de l’implémenter sans utiliser les classes de base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Terminal de diffusion multimédia en continu (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eeb9ad231c114ca18b4dea0926b861360ab5a359cd9ee8c48fd1c388a941a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002907"
---
# <a name="media-streaming-terminal-mst"></a>Terminal de diffusion multimédia en continu (MST)

le terminal de diffusion multimédia en continu (MST) est un terminal dynamique basé sur l’utilisation de filtres de DirectShow. Un MSP écrit à l’aide des [classes de base TAPI 3 MSP](tapi-3-msp-base-classes.md) intègre un MST, mais les créateurs de MSP peuvent choisir de l’implémenter sans utiliser les classes de base.

Pour appeler la création de MST, une application effectue un appel à [**ITTerminalSupport :: CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) à l’aide de *PTERMINALCLASS* défini sur CLSID \_ MediaStreamTerminal.

Les interfaces [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) et [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) sont ensuite exposées sur le terminal, ce qui permet à une application de régler les performances de diffusion en continu. Ces interfaces sont déclarées dans Tapi3. h.

l’implémentation et l’utilisation d’un MST nécessitent une connaissance des filtres de DirectShow et de la gestion des graphiques de filtres. reportez-vous à la documentation DirectShow sous le nœud Services graphiques et multimédias du kit de développement logiciel (SDK) de la plateforme. La référence de diffusion multimédia en continu est particulièrement utile pour les auteurs MSP.

 

 
