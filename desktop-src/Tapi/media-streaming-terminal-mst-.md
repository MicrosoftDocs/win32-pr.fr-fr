---
description: Le terminal de diffusion multimédia en continu (MST) est un terminal dynamique basé sur l’utilisation de filtres DirectShow. Un MSP écrit à l’aide des classes de base TAPI 3 MSP intègre un MST, mais les créateurs de MSP peuvent choisir de l’implémenter sans utiliser les classes de base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Terminal de diffusion multimédia en continu (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953404"
---
# <a name="media-streaming-terminal-mst"></a>Terminal de diffusion multimédia en continu (MST)

Le terminal de diffusion multimédia en continu (MST) est un terminal dynamique basé sur l’utilisation de filtres DirectShow. Un MSP écrit à l’aide des [classes de base TAPI 3 MSP](tapi-3-msp-base-classes.md) intègre un MST, mais les créateurs de MSP peuvent choisir de l’implémenter sans utiliser les classes de base.

Pour appeler la création de MST, une application effectue un appel à [**ITTerminalSupport :: CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) à l’aide de *PTERMINALCLASS* défini sur CLSID \_ MediaStreamTerminal.

Les interfaces [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) et [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) sont ensuite exposées sur le terminal, ce qui permet à une application de régler les performances de diffusion en continu. Ces interfaces sont déclarées dans Tapi3. h.

L’implémentation et l’utilisation d’un MST nécessitent une connaissance des filtres DirectShow et de la gestion des graphiques de filtres. Reportez-vous au document DirectShow sous le nœud services graphiques et multimédias du kit de développement logiciel (SDK) de la plateforme. La référence de diffusion multimédia en continu est particulièrement utile pour les auteurs MSP.

 

 
