---
description: Spécifie si une Media Foundation transformation (MFT) effectue un traitement asynchrone.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: Attribut MF_TRANSFORM_ASYNC (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753149"
---
# <a name="mf_transform_async-attribute"></a><span data-ttu-id="e241a-103">\_Attribut Async de transformation MF \_</span><span class="sxs-lookup"><span data-stu-id="e241a-103">MF\_TRANSFORM\_ASYNC attribute</span></span>

<span data-ttu-id="e241a-104">Spécifie si une Media Foundation transformation (MFT) effectue un traitement asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e241a-104">Specifies whether a Media Foundation transform (MFT) performs asynchronous processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="e241a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e241a-105">Data type</span></span>

<span data-ttu-id="e241a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e241a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e241a-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="e241a-107">Get/set</span></span>

<span data-ttu-id="e241a-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e241a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e241a-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e241a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e241a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e241a-110">Remarks</span></span>

<span data-ttu-id="e241a-111">L’attribut est une valeur booléenne :</span><span class="sxs-lookup"><span data-stu-id="e241a-111">The attribute is a Boolean value:</span></span>

-   <span data-ttu-id="e241a-112">Si l’attribut est différent de zéro, la table MFT effectue un traitement asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e241a-112">If the attribute is nonzero, the MFT performs asynchronous processing.</span></span>
-   <span data-ttu-id="e241a-113">Si l’attribut a la valeur 0 ou n’est pas défini, la table MFT est synchrone.</span><span class="sxs-lookup"><span data-stu-id="e241a-113">If the attribute is 0 or not set, the MFT is synchronous.</span></span>

<span data-ttu-id="e241a-114">Pour récupérer cet attribut, appelez d’abord [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour récupérer le magasin d’attributs de la MFT.</span><span class="sxs-lookup"><span data-stu-id="e241a-114">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT's attribute store.</span></span> <span data-ttu-id="e241a-115">Si cette méthode est réussie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) pour récupérer la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e241a-115">If that method succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span> <span data-ttu-id="e241a-116">Si l’une ou l’autre des deux méthodes échoue, la table MFT est synchrone.</span><span class="sxs-lookup"><span data-stu-id="e241a-116">If either of the two methods fails, the MFT is synchronous.</span></span>

<span data-ttu-id="e241a-117">Pour les MFTs asynchrones, cet attribut doit être défini sur une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e241a-117">For asynchronous MFTs, this attribute must be set to a nonzero value.</span></span> <span data-ttu-id="e241a-118">Pour les MFTs synchrones, cet attribut est facultatif, mais il doit avoir la valeur 0 s’il est présent.</span><span class="sxs-lookup"><span data-stu-id="e241a-118">For synchronous MFTs, this attribute is optional, but must be set to 0 if present.</span></span>

<span data-ttu-id="e241a-119">Les MFTs asynchrones ne sont pas compatibles avec les versions antérieures de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e241a-119">Asynchronous MFTs are not compatible with earlier versions of Media Foundation.</span></span> <span data-ttu-id="e241a-120">Pour utiliser une table MFT asynchrone, le client doit définir l’attribut de [**\_ \_ \_ déverrouillage asynchrone de transformation MF**](mf-transform-async-unlock.md) sur la table MFT.</span><span class="sxs-lookup"><span data-stu-id="e241a-120">To use an asynchronous MFT, the client must set the [**MF\_TRANSFORM\_ASYNC\_UNLOCK**](mf-transform-async-unlock.md) attribute on the MFT.</span></span> <span data-ttu-id="e241a-121">(Le pipeline Microsoft Media Foundation effectue cette étape automatiquement.)</span><span class="sxs-lookup"><span data-stu-id="e241a-121">(The Microsoft Media Foundation pipeline performs this step automatically.)</span></span>

## <a name="examples"></a><span data-ttu-id="e241a-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="e241a-122">Examples</span></span>

<span data-ttu-id="e241a-123">Le code suivant teste si une table MFT effectue un traitement asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e241a-123">The following code tests whether an MFT performs asynchronous processing.</span></span>


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="e241a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e241a-124">Requirements</span></span>



| <span data-ttu-id="e241a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e241a-125">Requirement</span></span> | <span data-ttu-id="e241a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e241a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e241a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e241a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e241a-128">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e241a-128">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e241a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e241a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e241a-130">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e241a-130">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e241a-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e241a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e241a-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="e241a-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e241a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e241a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e241a-134">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e241a-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e241a-135">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="e241a-135">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="e241a-136">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="e241a-136">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="e241a-137">**mode \_ de \_ déverrouillage asynchrone de la transformation MF \_**</span><span class="sxs-lookup"><span data-stu-id="e241a-137">**MF\_TRANSFORM\_ASYNC\_UNLOCK**</span></span>](mf-transform-async-unlock.md)
</dt> </dl>

 

 




