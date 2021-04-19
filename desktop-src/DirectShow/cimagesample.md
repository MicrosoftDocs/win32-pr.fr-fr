---
description: La classe CImageSample implémente un exemple de média qui gère une image bitmap indépendante du périphérique (DIB) GDI.
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: CImageSample, classe (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528780"
---
# <a name="cimagesample-class"></a><span data-ttu-id="e9a20-103">CImageSample, classe</span><span class="sxs-lookup"><span data-stu-id="e9a20-103">CImageSample class</span></span>

![hiérarchie de la classe cimagesample](images/wutil03.png)

<span data-ttu-id="e9a20-105">La `CImageSample` classe implémente un exemple de média qui gère une image bitmap indépendante du périphérique (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="e9a20-105">The `CImageSample` class implements a media sample that manages a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="e9a20-106">Cette classe dérive de la classe [**CMediaSample**](cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a20-106">This class derives from the [**CMediaSample**](cmediasample.md) class.</span></span> <span data-ttu-id="e9a20-107">Elle est destinée à être utilisée avec la classe [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a20-107">It is intended to be used with the [**CImageAllocator**](cimageallocator.md) class.</span></span> <span data-ttu-id="e9a20-108">La classe **CImageAllocator** fournit un allocateur qui crée des `CImageSample` objets.</span><span class="sxs-lookup"><span data-stu-id="e9a20-108">The **CImageAllocator** class provides an allocator that creates `CImageSample` objects.</span></span>



| <span data-ttu-id="e9a20-109">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="e9a20-109">Protected Member Variables</span></span>                        | <span data-ttu-id="e9a20-110">Description</span><span class="sxs-lookup"><span data-stu-id="e9a20-110">Description</span></span>                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="e9a20-111">**m \_ DibData**</span><span class="sxs-lookup"><span data-stu-id="e9a20-111">**m\_DibData**</span></span>](cimagesample-m-dibdata.md)      | <span data-ttu-id="e9a20-112">Contient des informations sur le DIB que cet objet gère.</span><span class="sxs-lookup"><span data-stu-id="e9a20-112">Contains information about the DIB that this object is managing.</span></span>  |
| [<span data-ttu-id="e9a20-113">**m \_ bInit**</span><span class="sxs-lookup"><span data-stu-id="e9a20-113">**m\_bInit**</span></span>](cimagesample-m-binit.md)          | <span data-ttu-id="e9a20-114">Indique si l’objet a été initialisé.</span><span class="sxs-lookup"><span data-stu-id="e9a20-114">Indicates whether the object has been initialized.</span></span>                |
| <span data-ttu-id="e9a20-115">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="e9a20-115">Public Methods</span></span>                                    | <span data-ttu-id="e9a20-116">Description</span><span class="sxs-lookup"><span data-stu-id="e9a20-116">Description</span></span>                                                       |
| [<span data-ttu-id="e9a20-117">**CImageSample**</span><span class="sxs-lookup"><span data-stu-id="e9a20-117">**CImageSample**</span></span>](cimagesample-cimagesample.md) | <span data-ttu-id="e9a20-118">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="e9a20-118">Constructor method.</span></span>                                               |
| [<span data-ttu-id="e9a20-119">**GetDIBData**</span><span class="sxs-lookup"><span data-stu-id="e9a20-119">**GetDIBData**</span></span>](cimagesample-getdibdata.md)     | <span data-ttu-id="e9a20-120">Récupère des informations sur le DIB que cet objet gère.</span><span class="sxs-lookup"><span data-stu-id="e9a20-120">Retrieves information about the DIB that this object is managing.</span></span> |
| [<span data-ttu-id="e9a20-121">**SetDIBData**</span><span class="sxs-lookup"><span data-stu-id="e9a20-121">**SetDIBData**</span></span>](cimagesample-setdibdata.md)     | <span data-ttu-id="e9a20-122">Définit des informations sur le DIB que cet objet gère.</span><span class="sxs-lookup"><span data-stu-id="e9a20-122">Sets information about the DIB that this object is managing.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="e9a20-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9a20-123">Requirements</span></span>



| <span data-ttu-id="e9a20-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9a20-124">Requirement</span></span> | <span data-ttu-id="e9a20-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9a20-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a20-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9a20-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e9a20-127"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9a20-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9a20-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9a20-128">Library</span></span><br/> | <dl> <span data-ttu-id="e9a20-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e9a20-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




