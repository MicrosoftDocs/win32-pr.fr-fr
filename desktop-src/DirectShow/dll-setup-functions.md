---
description: Ces fonctions inscrivent un filtre.
ms.assetid: c9c4976f-d4c5-465e-8ad7-4294c05d0e0a
title: Fonctions de configuration des DLL (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DLL
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 449c6899c207365118a57e396bb52817282453ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539532"
---
# <a name="dll-setup-functions"></a><span data-ttu-id="2d604-103">Fonctions de configuration des DLL</span><span class="sxs-lookup"><span data-stu-id="2d604-103">DLL Setup Functions</span></span>

<span data-ttu-id="2d604-104">Ces fonctions inscrivent un filtre.</span><span class="sxs-lookup"><span data-stu-id="2d604-104">These functions register a filter.</span></span>



| <span data-ttu-id="2d604-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="2d604-105">Function</span></span>                                                         | <span data-ttu-id="2d604-106">Description</span><span class="sxs-lookup"><span data-stu-id="2d604-106">Description</span></span>                                        |
|------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2d604-107">**AMovieDllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="2d604-107">**AMovieDllRegisterServer**</span></span>](amoviedllregisterserver.md)       | <span data-ttu-id="2d604-108">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="2d604-108">Obsolete.</span></span>                                          |
| [<span data-ttu-id="2d604-109">**AMovieDllRegisterServer2**</span><span class="sxs-lookup"><span data-stu-id="2d604-109">**AMovieDllRegisterServer2**</span></span>](amoviedllregisterserver2.md)     | <span data-ttu-id="2d604-110">Inscrit et annule l’inscription des filtres.</span><span class="sxs-lookup"><span data-stu-id="2d604-110">Registers and unregisters filters.</span></span>                 |
| [<span data-ttu-id="2d604-111">**AMovieDllUnregisterServer**</span><span class="sxs-lookup"><span data-stu-id="2d604-111">**AMovieDllUnregisterServer**</span></span>](amoviedllunregisterserver.md)   | <span data-ttu-id="2d604-112">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="2d604-112">Obsolete.</span></span>                                          |
| [<span data-ttu-id="2d604-113">**AMovieSetupRegisterFilter**</span><span class="sxs-lookup"><span data-stu-id="2d604-113">**AMovieSetupRegisterFilter**</span></span>](amoviesetupregisterfilter.md)   | <span data-ttu-id="2d604-114">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="2d604-114">Obsolete.</span></span>                                          |
| [<span data-ttu-id="2d604-115">**AMovieSetupRegisterFilter2**</span><span class="sxs-lookup"><span data-stu-id="2d604-115">**AMovieSetupRegisterFilter2**</span></span>](amoviesetupregisterfilter2.md) | <span data-ttu-id="2d604-116">Enregistre les mérites, les codes confidentiels et les types de média d’un filtre.</span><span class="sxs-lookup"><span data-stu-id="2d604-116">Registers a filter's merit, pins, and media types.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="2d604-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d604-117">Requirements</span></span>



| <span data-ttu-id="2d604-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d604-118">Requirement</span></span> | <span data-ttu-id="2d604-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d604-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d604-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d604-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2d604-121"><dt>DLLSETUP. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d604-121"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2d604-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2d604-122">Library</span></span><br/> | <dl> <span data-ttu-id="2d604-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2d604-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




