---
title: Choix d’une séquence de protocole
description: Les meilleures pratiques pour le choix d’une séquence de protocole impliquent l’utilisation de ncacn \_ IP \_ TCP et Ncalrpc, et non ncacn \_ NP, ncacn \_ SPX et ncadg \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3dea44868b96361ccaddc6e339f94fde92704f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031773"
---
# <a name="choosing-a-protocol-sequence"></a><span data-ttu-id="c708b-103">Choix d’une séquence de protocole</span><span class="sxs-lookup"><span data-stu-id="c708b-103">Choosing a Protocol Sequence</span></span>

<span data-ttu-id="c708b-104">**Bonne pratique :** Utilisez [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) pour effectuer un appel distant.</span><span class="sxs-lookup"><span data-stu-id="c708b-104">**Best practice:** Use [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) when making a remote call.</span></span> <span data-ttu-id="c708b-105">Utilisez [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) pour les appels locaux.</span><span class="sxs-lookup"><span data-stu-id="c708b-105">Use [**ncalrpc**](/windows/desktop/Midl/ncalrpc) for local calls.</span></span> <span data-ttu-id="c708b-106">N’utilisez pas [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ SPX**](/windows/desktop/Midl/ncacn-spx)ou l’une des séquences de protocole **ncadg \_ \*** ; elles sont moins efficaces et ont des capacités inférieures.</span><span class="sxs-lookup"><span data-stu-id="c708b-106">Do not use [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), [**ncacn\_spx**](/windows/desktop/Midl/ncacn-spx), or any of the **ncadg\_\*** protocol sequences; they are less efficient and have inferior capabilities.</span></span>

 

 