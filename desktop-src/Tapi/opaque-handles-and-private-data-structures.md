---
description: Les handles opaques sont utilisés dans TSPI pour faire référence aux structures de données qui représentent des lignes, des téléphones et des apparences d’appel.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Descripteurs opaques et structures de données privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951351"
---
# <a name="opaque-handles-and-private-data-structures"></a><span data-ttu-id="7f2b5-103">Descripteurs opaques et structures de données privées</span><span class="sxs-lookup"><span data-stu-id="7f2b5-103">Opaque Handles and Private Data Structures</span></span>

<span data-ttu-id="7f2b5-104">Les handles opaques sont utilisés dans TSPI pour faire référence aux structures de données qui représentent des lignes, des téléphones et des apparences d’appel.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-104">Opaque handles are used in TSPI to refer to the data structures representing lines, phones, and call appearances.</span></span> <span data-ttu-id="7f2b5-105">Celles-ci apparaissent en tant que paramètres de la plupart des fonctions et des rappels.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-105">These appear as parameters to most of the functions and callbacks.</span></span> <span data-ttu-id="7f2b5-106">Il existe peu de fonctions qui font référence à l’appareil à l’aide d’un identificateur d’appareil au lieu d’un handle opaque.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-106">There are few functions that refer to the device using a device identifier instead of an opaque handle.</span></span> <span data-ttu-id="7f2b5-107">Dans ce cas, la référence se rapporte à l’appareil lui-même plutôt qu’à une structure de données.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-107">In such a case, the reference is to the device itself rather than to a data structure.</span></span> <span data-ttu-id="7f2b5-108">Les fonctions qui fonctionnent de cette manière sont généralement celles appelées à des moments d’initialisation précoces avant la création des structures de données et l’échange des handles opaques.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-108">Functions that work in this fashion are typically those called at early initialization times before data structures are created and opaque handles are exchanged.</span></span>

<span data-ttu-id="7f2b5-109">Le fournisseur de services doit décider comment interpréter ces handles.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-109">The service provider must decide how to interpret these handles.</span></span> <span data-ttu-id="7f2b5-110">Un fournisseur de services utilise généralement le pointeur vers sa structure de données ou vers l’index dans un tableau de structures de données comme handle opaque.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-110">A service provider typically uses the pointer to its data structure or to the index into an array of data structures as its opaque handle.</span></span> <span data-ttu-id="7f2b5-111">La seule restriction est que le fournisseur de services ne peut pas utiliser la valeur 0 comme [HDRVLINE](hdrvline.md), HDRVCALL ou [HDRVPHONE](hdrvphone.md).</span><span class="sxs-lookup"><span data-stu-id="7f2b5-111">The only restriction is that the service provider cannot use the value 0 as an [HDRVLINE](hdrvline.md), HDRVCALL, or [HDRVPHONE](hdrvphone.md).</span></span> <span data-ttu-id="7f2b5-112">La valeur 0 ou **null** pour un descripteur a une signification spéciale dans certaines opérations.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-112">The value 0 or **NULL** for a handle has a special meaning in some operations.</span></span>

 

 



