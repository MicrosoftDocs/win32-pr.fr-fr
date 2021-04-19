---
description: La classe CSeekingPassThru est un objet d’assistance qui crée des objets CPosPassThru et CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: CSeekingPassThru, classe (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528385"
---
# <a name="cseekingpassthru-class"></a><span data-ttu-id="adad8-103">CSeekingPassThru, classe</span><span class="sxs-lookup"><span data-stu-id="adad8-103">CSeekingPassThru class</span></span>

<span data-ttu-id="adad8-104">La `CSeekingPassThru` classe est un objet d’assistance qui crée des objets [**CPosPassThru**](cpospassthru.md) et [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="adad8-104">The `CSeekingPassThru` class is a helper object that creates [**CPosPassThru**](cpospassthru.md) and [**CRendererPosPassThru**](crendererpospassthru.md) objects.</span></span>

<span data-ttu-id="adad8-105">Les classes **CPosPassThru** et **CRendererPosPassThru** sont des objets d’assistance qui transmettent des commandes en amont, de sorte que la `CSeekingPassThru` classe est un objet d’assistance pour créer des objets d’assistance.</span><span class="sxs-lookup"><span data-stu-id="adad8-105">The **CPosPassThru** and **CRendererPosPassThru** classes are helper objects that pass seeking commands upstream, so the `CSeekingPassThru` class is a helper object for creating helper objects.</span></span>

<span data-ttu-id="adad8-106">Il n’est pas nécessaire d’utiliser cette classe directement.</span><span class="sxs-lookup"><span data-stu-id="adad8-106">It is not necessary to use this class directly.</span></span> <span data-ttu-id="adad8-107">Utilisez plutôt la fonction [**CreatePosPassThru**](createpospassthru.md) , qui gère tous les détails de l’utilisation de cette classe.</span><span class="sxs-lookup"><span data-stu-id="adad8-107">Instead, use the [**CreatePosPassThru**](createpospassthru.md) function, which handles all of the details of using this class.</span></span> <span data-ttu-id="adad8-108">Elle présente l’avantage supplémentaire de charger l’objet à partir de Quartz.dll, ce qui réduit quelque peu la taille du code de votre filtre.</span><span class="sxs-lookup"><span data-stu-id="adad8-108">It has the further advantage of loading the object from Quartz.dll, which reduces the code size of your filter somewhat.</span></span> <span data-ttu-id="adad8-109">Pour plus d’informations, consultez [**CPosPassThru**](cpospassthru.md).</span><span class="sxs-lookup"><span data-stu-id="adad8-109">For more information, see [**CPosPassThru**](cpospassthru.md).</span></span>

<span data-ttu-id="adad8-110">La `CSeekingPassThru` classe expose l’interface [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) .</span><span class="sxs-lookup"><span data-stu-id="adad8-110">The `CSeekingPassThru` class exposes the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface.</span></span> <span data-ttu-id="adad8-111">La méthode [**ISeekingPassThru :: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) Initialise l’objet.</span><span class="sxs-lookup"><span data-stu-id="adad8-111">The [**ISeekingPassThru::Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) method initializes the object.</span></span> <span data-ttu-id="adad8-112">Une fois l’objet initialisé, le filtre peut l’interroger pour les interfaces [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) et [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="adad8-112">After the object is initialized, the filter can query it for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interfaces.</span></span>



| <span data-ttu-id="adad8-113">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="adad8-113">Public Methods</span></span>                                                  | <span data-ttu-id="adad8-114">Description</span><span class="sxs-lookup"><span data-stu-id="adad8-114">Description</span></span>                        |
|-----------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="adad8-115">**CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="adad8-115">**CSeekingPassThru**</span></span>](cseekingpassthru-cseekingpassthru.md)   | <span data-ttu-id="adad8-116">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="adad8-116">Constructor method.</span></span>                |
| [<span data-ttu-id="adad8-117">**~ CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="adad8-117">**~CSeekingPassThru**</span></span>](cseekingpassthru--cseekingpassthru.md) | <span data-ttu-id="adad8-118">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="adad8-118">Destructor method.</span></span>                 |
| [<span data-ttu-id="adad8-119">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="adad8-119">**CreateInstance**</span></span>](cseekingpassthru-createinstance.md)       | <span data-ttu-id="adad8-120">Crée une instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="adad8-120">Creates an instance of the object.</span></span> |
| <span data-ttu-id="adad8-121">Méthodes ISeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="adad8-121">ISeekingPassThru Methods</span></span>                                        | <span data-ttu-id="adad8-122">Description</span><span class="sxs-lookup"><span data-stu-id="adad8-122">Description</span></span>                        |
| [<span data-ttu-id="adad8-123">**Rein**</span><span class="sxs-lookup"><span data-stu-id="adad8-123">**Init**</span></span>](cseekingpassthru-init.md)                           | <span data-ttu-id="adad8-124">Initialise l'objet.</span><span class="sxs-lookup"><span data-stu-id="adad8-124">Initializes the object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="adad8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adad8-125">Requirements</span></span>



| <span data-ttu-id="adad8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adad8-126">Requirement</span></span> | <span data-ttu-id="adad8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="adad8-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adad8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="adad8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="adad8-129"><dt>Seekpt. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adad8-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="adad8-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="adad8-130">Library</span></span><br/> | <dl> <span data-ttu-id="adad8-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="adad8-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




