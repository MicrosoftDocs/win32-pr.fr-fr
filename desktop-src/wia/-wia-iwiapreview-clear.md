---
description: 'Libère l’image non filtrée mise en cache par la méthode IWiaPreview :: GetNewPreview. Il libère également le filtre de traitement d’image.'
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'IWiaPreview :: Clear, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515467"
---
# <a name="iwiapreviewclear-method"></a><span data-ttu-id="65955-104">IWiaPreview :: Clear, méthode</span><span class="sxs-lookup"><span data-stu-id="65955-104">IWiaPreview::Clear method</span></span>

<span data-ttu-id="65955-105">Libère l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="65955-105">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="65955-106">Il libère également le filtre de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="65955-106">It also releases the image processing filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="65955-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65955-107">Syntax</span></span>


```C++
void Clear();
```



## <a name="parameters"></a><span data-ttu-id="65955-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65955-108">Parameters</span></span>

<span data-ttu-id="65955-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="65955-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65955-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65955-110">Return value</span></span>

<span data-ttu-id="65955-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="65955-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65955-112">Notes</span><span class="sxs-lookup"><span data-stu-id="65955-112">Remarks</span></span>

<span data-ttu-id="65955-113">Sur **IWiaPreview :: Clear** le composant WIA (Windows Image Acquisition) 2,0 Preview libère tous les pointeurs d’interface qu’il stocke.</span><span class="sxs-lookup"><span data-stu-id="65955-113">On **IWiaPreview::Clear** the Windows Image Acquisition (WIA) 2.0 Preview Component releases all interface pointers that it stores.</span></span> <span data-ttu-id="65955-114">Le composant d’aperçu WIA 2,0 conserve les références à *pWiaItem2* et *PWiaTransferCallback* passées dans [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="65955-114">The WIA 2.0 Preview Component keeps references to *pWiaItem2* and *pWiaTransferCallback* passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="65955-115">Pour être précis, le composant WIA 2,0 Preview conserve une référence à *pWiaItem2* et le filtre de traitement d’image du pilote, qui à son tour conserve une référence à *pWiaTransferCallback*.</span><span class="sxs-lookup"><span data-stu-id="65955-115">To be precise, the WIA 2.0 Preview Component keeps a reference to *pWiaItem2* and the driver's image processing filter, which in turn keeps a reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="65955-116">Sur **IWiaPreview :: Clear**, le composant WIA 2,0 Preview libère également sa référence à *pWiaItem2* et au filtre de traitement d’image, qui à son tour libère sa référence à *pWiaTransferCallback*.</span><span class="sxs-lookup"><span data-stu-id="65955-116">On **IWiaPreview::Clear**, the WIA 2.0 Preview Component also releases its reference to *pWiaItem2* and to the image processing filter, which in turn releases its reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="65955-117">Le composant d’aperçu WIA 2,0 supprime l’image mise en cache et non filtrée qu’elle stocke en interne.</span><span class="sxs-lookup"><span data-stu-id="65955-117">The WIA 2.0 Preview Component deletes the cached, unfiltered image that it stores internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="65955-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65955-118">Requirements</span></span>



| <span data-ttu-id="65955-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65955-119">Requirement</span></span> | <span data-ttu-id="65955-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="65955-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65955-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65955-121">Minimum supported client</span></span><br/> | <span data-ttu-id="65955-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65955-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="65955-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65955-123">Minimum supported server</span></span><br/> | <span data-ttu-id="65955-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65955-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="65955-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="65955-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="65955-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="65955-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="65955-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="65955-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65955-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65955-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




