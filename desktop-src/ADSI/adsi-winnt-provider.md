---
title: Fournisseur WinNT ADSI
description: Le fournisseur Microsoft ADSI implémente un ensemble d’objets ADSI pour prendre en charge différentes interfaces ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI du fournisseur Winnt ADSI
- ADSI du fournisseur de services Winnt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379599"
---
# <a name="adsi-winnt-provider"></a><span data-ttu-id="c5c75-105">Fournisseur WinNT ADSI</span><span class="sxs-lookup"><span data-stu-id="c5c75-105">ADSI WinNT Provider</span></span>

<span data-ttu-id="c5c75-106">Le fournisseur Microsoft ADSI implémente un ensemble d’objets ADSI pour prendre en charge différentes interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="c5c75-106">The Microsoft ADSI provider implements a set of ADSI objects to support various ADSI interfaces.</span></span> <span data-ttu-id="c5c75-107">Le nom de l’espace de noms pour le fournisseur Windows est « Winnt » et ce fournisseur est communément appelé le fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="c5c75-107">The namespace name for the Windows provider is "WinNT" and this provider is commonly referred to as the WinNT provider.</span></span> <span data-ttu-id="c5c75-108">Pour accéder au fournisseur WinNT, établissez une liaison à l’un des [objets ADSI de Winnt](adsi-objects-of-winnt.md)à l’aide de la valeur [ADsPath de Winnt](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="c5c75-108">To access the WinNT provider, bind to any of the [ADSI objects of WinNT](adsi-objects-of-winnt.md), using the [WinNT AdsPath](winnt-adspath.md).</span></span>

<span data-ttu-id="c5c75-109">Le fournisseur Winnt est inclus dans le composant système ADSI pour Windows et Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c5c75-109">The WinNT provider is included in the ADSI system component for Windows and Windows Server.</span></span>

> [!Note]  
> <span data-ttu-id="c5c75-110">Le fournisseur Winnt par défaut ne peut pas être considéré comme entièrement thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c5c75-110">The default WinNT provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="c5c75-111">Les Writers d’applications multithread doivent gérer le multithreading pour coordonner correctement tout accès entre les threads via l’utilisation appropriée d’objets de synchronisation tels que les sémaphores, les mutex, les sections critiques, etc.</span><span class="sxs-lookup"><span data-stu-id="c5c75-111">Writers of multithreaded applications should handle multithreading to properly coordinate any access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




