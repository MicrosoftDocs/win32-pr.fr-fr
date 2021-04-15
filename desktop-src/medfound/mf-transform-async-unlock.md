---
description: Active l’utilisation d’une transformation de Media Foundation asynchrone (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: Attribut MF_TRANSFORM_ASYNC_UNLOCK (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527400"
---
# <a name="mf_transform_async_unlock-attribute"></a><span data-ttu-id="f185b-103">\_Attribut de \_ déverrouillage asynchrone de transformation MF \_</span><span class="sxs-lookup"><span data-stu-id="f185b-103">MF\_TRANSFORM\_ASYNC\_UNLOCK attribute</span></span>

<span data-ttu-id="f185b-104">Active l’utilisation d’une transformation de Media Foundation asynchrone (MFT).</span><span class="sxs-lookup"><span data-stu-id="f185b-104">Enables the use of an asynchronous Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="f185b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f185b-105">Data type</span></span>

<span data-ttu-id="f185b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f185b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f185b-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f185b-107">Get/set</span></span>

<span data-ttu-id="f185b-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f185b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f185b-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f185b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f185b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f185b-110">Remarks</span></span>

<span data-ttu-id="f185b-111">Les MFTs asynchrones ne sont pas compatibles avec les versions antérieures de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f185b-111">Asynchronous MFTs are not compatible with earlier versions of Microsoft Media Foundation.</span></span> <span data-ttu-id="f185b-112">Pour empêcher les applications existantes d’utiliser accidentellement une table MFT asynchrone, cet attribut doit être défini sur une valeur différente de zéro pour qu’une table MFT asynchrone puisse être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f185b-112">To prevent existing applications from accidentally using an asynchronous MFT, this attribute must be set to a nonzero value before an asynchronous MFT can be used.</span></span> <span data-ttu-id="f185b-113">Le pipeline Media Foundation définit automatiquement l’attribut, de sorte que la plupart des applications n’ont pas besoin d’utiliser cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f185b-113">The Media Foundation pipeline automatically sets the attribute, so that most applications do not need to use this attribute.</span></span> <span data-ttu-id="f185b-114">Toutefois, si une application utilise une table MFT asynchrone en dehors du pipeline Media Foundation, l’application doit définir cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f185b-114">However, if an application uses an asynchronous MFT outside of the Media Foundation pipeline, the application must set this attribute.</span></span>

<span data-ttu-id="f185b-115">Les MFTs synchrones ne nécessitent pas cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f185b-115">Synchronous MFTs do not require this attribute.</span></span>

<span data-ttu-id="f185b-116">Pour tester si une table MFT est asynchrone, récupérez la valeur de l’attribut [ \_ \_ Async de transformation MF](mf-transform-async.md) sur la table MFT.</span><span class="sxs-lookup"><span data-stu-id="f185b-116">To test whether an MFT is asynchronous, get the value of the [MF\_TRANSFORM\_ASYNC](mf-transform-async.md) attribute on the MFT.</span></span>

## <a name="examples"></a><span data-ttu-id="f185b-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="f185b-117">Examples</span></span>

<span data-ttu-id="f185b-118">Le code suivant déverrouille une table MFT asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f185b-118">The following code unlocks an asynchronous MFT.</span></span>


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="f185b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f185b-119">Requirements</span></span>



| <span data-ttu-id="f185b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f185b-120">Requirement</span></span> | <span data-ttu-id="f185b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f185b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f185b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f185b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f185b-123">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f185b-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f185b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f185b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f185b-125">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f185b-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f185b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f185b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f185b-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f185b-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f185b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f185b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f185b-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f185b-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f185b-130">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="f185b-130">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="f185b-131">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="f185b-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




