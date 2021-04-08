---
description: Spécifie si une transformation de Media Foundation (MFT) copie les attributs des exemples d’entrée vers les exemples de sortie.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED, propriété (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864161"
---
# <a name="mfpkey_exattribute_supported-property"></a><span data-ttu-id="a52d0-103">\_Propriété MFPKEY EXattribute \_ prise en charge</span><span class="sxs-lookup"><span data-stu-id="a52d0-103">MFPKEY\_EXATTRIBUTE\_SUPPORTED property</span></span>

<span data-ttu-id="a52d0-104">Spécifie si une transformation de Media Foundation (MFT) copie les attributs des exemples d’entrée vers les exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="a52d0-104">Specifies whether a Media Foundation transform (MFT) copies attributes from input samples to output samples.</span></span>



<span data-ttu-id="a52d0-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a52d0-105">Data type</span></span>

<span data-ttu-id="a52d0-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a52d0-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a52d0-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a52d0-107">PROPVARIANT member</span></span>

<span data-ttu-id="a52d0-108">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="a52d0-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="a52d0-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="a52d0-109">VT\_BOOL</span></span>

<span data-ttu-id="a52d0-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="a52d0-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a52d0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a52d0-111">Remarks</span></span>

<span data-ttu-id="a52d0-112">Cet attribut peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a52d0-112">This attribute can have the following values.</span></span>



| <span data-ttu-id="a52d0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a52d0-113">Value</span></span>              | <span data-ttu-id="a52d0-114">Description</span><span class="sxs-lookup"><span data-stu-id="a52d0-114">Description</span></span>                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a52d0-115">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="a52d0-115">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="a52d0-116">La table MFT copie les attributs des exemples d’entrée vers les exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="a52d0-116">The MFT copies attributes from the input samples to the output samples.</span></span>                                                                                 |
| <span data-ttu-id="a52d0-117">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="a52d0-117">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="a52d0-118">La session multimédia copie les attributs des exemples d’entrée vers les exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="a52d0-118">The Media Session copies attributes from input samples to output samples.</span></span> <span data-ttu-id="a52d0-119">Elle ne remplace pas les attributs définis par la table MFT sur les exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="a52d0-119">It does not overwrite any attributes that the MFT sets on the output samples.</span></span> |



 

<span data-ttu-id="a52d0-120">Pour obtenir cet attribut, appelez **QueryInterface** sur la MFT de l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="a52d0-120">To get this attribute, call **QueryInterface** on the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="a52d0-121">La valeur par défaut **est \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a52d0-121">The default value is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="a52d0-122">Si la MFT n’expose pas l’interface **IPropertyStore** , ou si cette propriété n’est pas définie, traitez la valeur comme **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a52d0-122">If the MFT does not expose the **IPropertyStore** interface, or if this property is not set, treat the value as **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="a52d0-123">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a52d0-123">This property is read-only.</span></span>

> [!NOTE] 
> <span data-ttu-id="a52d0-124">Cet attribut ne s’applique pas aux MFTs asynchrones.</span><span class="sxs-lookup"><span data-stu-id="a52d0-124">This attribute does not apply to asynchronous MFTs.</span></span> <span data-ttu-id="a52d0-125">Les attributs ne seront pas copiés des exemples d’entrée vers les exemples de sortie pour les MFTs asynchrones, quelle que soit la valeur de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="a52d0-125">Attributes will not be copied from the input samples to the output samples for asynchronous MFTs, regardless of the value of this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="a52d0-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="a52d0-126">Examples</span></span>

<span data-ttu-id="a52d0-127">L’exemple suivant retourne la \_ valeur variant true si une table MFT copie des attributs d’exemple.</span><span class="sxs-lookup"><span data-stu-id="a52d0-127">The following example returns VARIANT\_TRUE if an MFT copies sample attributes.</span></span>


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a><span data-ttu-id="a52d0-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a52d0-128">Requirements</span></span>



| <span data-ttu-id="a52d0-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a52d0-129">Requirement</span></span> | <span data-ttu-id="a52d0-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a52d0-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a52d0-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a52d0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a52d0-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a52d0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a52d0-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a52d0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a52d0-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a52d0-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a52d0-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a52d0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a52d0-136"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="a52d0-136"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a52d0-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a52d0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a52d0-138">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a52d0-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a52d0-139">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="a52d0-139">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="a52d0-140">**IMFTransform ::P rocessOutput**</span><span class="sxs-lookup"><span data-stu-id="a52d0-140">**IMFTransform::ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




