---
description: Permet au filtre de traitement d’image d’écrire des propriétés sur le pilote (et l’appareil).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'IWiaImageFilter :: ApplyProperties, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538678"
---
# <a name="iwiaimagefilterapplyproperties-method"></a><span data-ttu-id="43c64-103">IWiaImageFilter :: ApplyProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="43c64-103">IWiaImageFilter::ApplyProperties method</span></span>

<span data-ttu-id="43c64-104">Permet au filtre de traitement d’image d’écrire des propriétés sur le pilote (et l’appareil).</span><span class="sxs-lookup"><span data-stu-id="43c64-104">Enables the image processing filter to write properties back to the driver (and device).</span></span>

## <a name="syntax"></a><span data-ttu-id="43c64-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43c64-105">Syntax</span></span>


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a><span data-ttu-id="43c64-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43c64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c64-107">*pWiaPropertyStorage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43c64-107">*pWiaPropertyStorage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43c64-108">Tapez : \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _</span><span class="sxs-lookup"><span data-stu-id="43c64-108">Type: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)\** _</span></span>

<span data-ttu-id="43c64-109">Spécifie un pointeur vers [_ *IWiaPropertyStorage* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pour les propriétés à appliquer.</span><span class="sxs-lookup"><span data-stu-id="43c64-109">Specifies a pointer to the [_ *IWiaPropertyStorage*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) for the properties to be applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c64-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43c64-110">Return value</span></span>

<span data-ttu-id="43c64-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="43c64-111">Type: **HRESULT**</span></span>

<span data-ttu-id="43c64-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="43c64-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43c64-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43c64-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43c64-114">Notes</span><span class="sxs-lookup"><span data-stu-id="43c64-114">Remarks</span></span>

<span data-ttu-id="43c64-115">N’appelez pas cette méthode directement à partir de votre application.</span><span class="sxs-lookup"><span data-stu-id="43c64-115">Do not call this method directly from your application.</span></span> <span data-ttu-id="43c64-116">Elle est appelée par l’acquisition d’images Windows (WIA) 2,0 après que le filtre de traitement d’image a traité les données brutes.</span><span class="sxs-lookup"><span data-stu-id="43c64-116">It is called by Windows Image Acquisition (WIA) 2.0 after the image processing filter has processed the raw data.</span></span>

<span data-ttu-id="43c64-117">*pWiaPropertyStorage* est l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) dans laquelle le filtre de traitement d’image doit écrire des propriétés.</span><span class="sxs-lookup"><span data-stu-id="43c64-117">*pWiaPropertyStorage* is the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface into which the image processing filter should write properties.</span></span> <span data-ttu-id="43c64-118">Un filtre de traitement d’image doit utiliser uniquement la méthode [IPropertyStorage :: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) pour écrire des propriétés.</span><span class="sxs-lookup"><span data-stu-id="43c64-118">An image processing filter should use only the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) method to write properties.</span></span>

<span data-ttu-id="43c64-119">Cette méthode permet au filtre de traitement d’image d’écrire des propriétés sur le pilote (et l’appareil).</span><span class="sxs-lookup"><span data-stu-id="43c64-119">This method allows the image processing filter to write properties back to the driver (and device).</span></span> <span data-ttu-id="43c64-120">Cela peut être nécessaire pour les filtres qui implémentent des fonctionnalités telles que l’exposition automatique lors de l’analyse des films.</span><span class="sxs-lookup"><span data-stu-id="43c64-120">This may be necessary for filters that implement features such as auto-exposure during film scanning.</span></span>

## <a name="requirements"></a><span data-ttu-id="43c64-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43c64-121">Requirements</span></span>



| <span data-ttu-id="43c64-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43c64-122">Requirement</span></span> | <span data-ttu-id="43c64-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="43c64-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43c64-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43c64-124">Minimum supported client</span></span><br/> | <span data-ttu-id="43c64-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43c64-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="43c64-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43c64-126">Minimum supported server</span></span><br/> | <span data-ttu-id="43c64-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43c64-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43c64-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="43c64-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="43c64-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="43c64-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="43c64-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="43c64-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43c64-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43c64-131"><dt>Wia.idl</dt></span></span> </dl> |



 

 
