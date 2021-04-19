---
description: CSourcePosition est une classe abstraite pour l’implémentation de l’interface IMediaPosition sur un filtre source.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: CSourcePosition, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515734"
---
# <a name="csourceposition-class"></a><span data-ttu-id="59b33-103">CSourcePosition, classe</span><span class="sxs-lookup"><span data-stu-id="59b33-103">CSourcePosition class</span></span>

<span data-ttu-id="59b33-104">`CSourcePosition` est une classe abstraite pour l’implémentation de l’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) sur un filtre source.</span><span class="sxs-lookup"><span data-stu-id="59b33-104">`CSourcePosition` is an abstract class for implementing the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface on a source filter.</span></span>

<span data-ttu-id="59b33-105">Cette classe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="59b33-105">This class is obsolete.</span></span> <span data-ttu-id="59b33-106">Si votre filtre source est recherché, il doit exposer l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) au lieu de **IMediaPosition**.</span><span class="sxs-lookup"><span data-stu-id="59b33-106">If your source filter is seekable, it should expose the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface instead of **IMediaPosition**.</span></span> <span data-ttu-id="59b33-107">Vous pouvez utiliser la classe de base [**CSourceSeeking**](csourceseeking.md) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="59b33-107">You can use the [**CSourceSeeking**](csourceseeking.md) base class for this purpose.</span></span>

 

 



