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
# <a name="media-streaming-terminal-mst"></a><span data-ttu-id="cd437-104">Terminal de diffusion multimédia en continu (MST)</span><span class="sxs-lookup"><span data-stu-id="cd437-104">Media Streaming Terminal (MST)</span></span>

<span data-ttu-id="cd437-105">Le terminal de diffusion multimédia en continu (MST) est un terminal dynamique basé sur l’utilisation de filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cd437-105">The Media Streaming Terminal (MST) is a dynamic terminal based on use of DirectShow filters.</span></span> <span data-ttu-id="cd437-106">Un MSP écrit à l’aide des [classes de base TAPI 3 MSP](tapi-3-msp-base-classes.md) intègre un MST, mais les créateurs de MSP peuvent choisir de l’implémenter sans utiliser les classes de base.</span><span class="sxs-lookup"><span data-stu-id="cd437-106">An MSP written using the [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md) will incorporate an MST, but MSP authors may choose to implement it without using the base classes.</span></span>

<span data-ttu-id="cd437-107">Pour appeler la création de MST, une application effectue un appel à [**ITTerminalSupport :: CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) à l’aide de *PTERMINALCLASS* défini sur CLSID \_ MediaStreamTerminal.</span><span class="sxs-lookup"><span data-stu-id="cd437-107">To invoke MST creation, an application makes a call to [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) using *pTerminalClass* set to CLSID\_MediaStreamTerminal.</span></span>

<span data-ttu-id="cd437-108">Les interfaces [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) et [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) sont ensuite exposées sur le terminal, ce qui permet à une application de régler les performances de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="cd437-108">The [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) and [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) interfaces are then exposed on the terminal, allowing an application to tune streaming performance.</span></span> <span data-ttu-id="cd437-109">Ces interfaces sont déclarées dans Tapi3. h.</span><span class="sxs-lookup"><span data-stu-id="cd437-109">These interfaces are declared in Tapi3.h.</span></span>

<span data-ttu-id="cd437-110">L’implémentation et l’utilisation d’un MST nécessitent une connaissance des filtres DirectShow et de la gestion des graphiques de filtres.</span><span class="sxs-lookup"><span data-stu-id="cd437-110">Implementation and use of an MST requires familiarity with DirectShow filters and filter graph management.</span></span> <span data-ttu-id="cd437-111">Reportez-vous au document DirectShow sous le nœud services graphiques et multimédias du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="cd437-111">Please refer to the DirectShow material under the Graphic and Multimedia Services node of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="cd437-112">La référence de diffusion multimédia en continu est particulièrement utile pour les auteurs MSP.</span><span class="sxs-lookup"><span data-stu-id="cd437-112">The Multimedia Streaming Reference will be particularly useful to MSP authors.</span></span>

 

 
