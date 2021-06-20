---
title: Fournir des attributs d’affichage
description: Découvrez comment fournir des attributs d’affichage. Text Services Framework (TSF) permet à un service de texte de fournir des attributs d’affichage pour le texte.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Text Services Framework (TSF), attributs d’affichage
- TSF (Text Services Framework), attributs d’affichage
- services de texte, attributs d’affichage
- attributs d'affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780cc191e39d5b1d0c3329bab87af5267e4a6c73
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406112"
---
# <a name="providing-display-attributes"></a><span data-ttu-id="0b7d6-108">Fournir des attributs d’affichage</span><span class="sxs-lookup"><span data-stu-id="0b7d6-108">Providing Display Attributes</span></span>

<span data-ttu-id="0b7d6-109">Text Services Framework (TSF) permet à un service de texte de fournir des attributs d’affichage pour le texte.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="0b7d6-110">Cela permet de fournir des commentaires visuels supplémentaires à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-110">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="0b7d6-111">Par exemple, un service de texte du vérificateur d’orthographe peut mettre en surbrillance un mot mal orthographié avec un trait de soulignement rouge.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="0b7d6-112">Les attributs d’affichage fournis sont définis par la structure [tf \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) et incluent la couleur de texte, la couleur d’arrière-plan du texte, le style de soulignement, la couleur du soulignement et le trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-112">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="0b7d6-113">Les clients qui utilisent ces informations d’attribut d’affichage sont plus souvent des applications, mais ils peuvent également inclure des services de texte.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-113">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="0b7d6-114">Le gestionnaire TSF effectue une médiation entre le fournisseur d’attributs d’affichage et le client et effectue le suivi du fournisseur d’attributs d’affichage des attributs d’affichage spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-114">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="0b7d6-115">Pour fournir des attributs d’affichage, un service de texte doit effectuer les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-115">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="0b7d6-116">Inscrivez le service de texte en tant que fournisseur d’attributs d’affichage en appelant [ITfCategoryMgr :: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) avec l’identificateur de classe du service de texte pour le premier paramètre, Guid \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER pour le deuxième paramètre et l’identificateur de classe du service de texte pour le troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-116">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="0b7d6-117">Implémentez [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) et rendez-le disponible à partir de la fabrique de classes.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-117">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="0b7d6-118">Implémentez [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) et rendez-le disponible à partir de [ITfDisplayAttributeProvider :: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="0b7d6-118">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="0b7d6-119">Implémentez un objet [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) pour chaque type d’attribut d’affichage fourni par le service de texte.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-119">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="0b7d6-120">Application des attributs d’affichage</span><span class="sxs-lookup"><span data-stu-id="0b7d6-120">Applying the Display Attributes</span></span>

<span data-ttu-id="0b7d6-121">Le service de texte doit appliquer l’attribut d’affichage à une plage de texte.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-121">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="0b7d6-122">Un service de texte peut uniquement modifier la valeur de la propriété pendant une session de modification en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-122">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="0b7d6-123">En supposant qu’il s’agit d’une session de modification en lecture/écriture, un attribut d’affichage est appliqué de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-123">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="0b7d6-124">Obtenez un objet [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) qui couvre le texte auquel l’attribut d’affichage sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-124">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="0b7d6-125">Obtenez un objet [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) pour les attributs de texte en appelant [ITfContext :: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) avec l' \_ attribut prop GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="0b7d6-125">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="0b7d6-126">Créez un [TfGuidAtom](tfguidatom.md) à partir du **GUID** de l’identificateur d’attribut d’affichage défini par le service de texte en appelant [ITfCategoryMgr :: RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="0b7d6-126">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="0b7d6-127">Initialisez une variable VARIANT sur VT \_ I4 et définissez le membre **lVal** sur le **TfGuidAtom** créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-127">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="0b7d6-128">Appliquez l’attribut Display à la plage en appelant [ITfProperty :: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) avec le cookie de modification en lecture/écriture, la plage et la variante initialisée à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-128">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


```C++
STDAPI CEditSession::DoEditSession(TfEditCookie ec)
{
    HRESULT hr;
    ITfCategoryMgr *pCategoryMgr;
    TfGuidAtom  gaDisplayAttribute = TF_INVALID_GUIDATOM;

    //Create a TfGuidAtom for the display attribute identifier. 
    hr = CoCreateInstance(CLSID_TF_CategoryMgr,
                         NULL, 
                         CLSCTX_INPROC_SERVER, 
                         IID_ITfCategoryMgr, 
                         (void**)&pCategoryMgr);
    
    if(SUCCEEDED(hr))
    {
        hr = pCategoryMgr->RegisterGUID(guidDisplayAttribute, &gaDisplayAttribute);

        pCategoryMgr->Release();
    }
    
    //Apply the display attribute to the selected text. 
    if(TF_INVALID_GUIDATOM != gaDisplayAttribute)
    {
        TF_SELECTION tfSel;
        ULONG cFetched;

        //Get the selection. 
        hr = m_pContext->GetSelection(ec, TF_DEFAULT_SELECTION, 1, &tfSel, &cFetched);
        if(SUCCEEDED(hr) && cFetched)
        {
            ITfProperty *pDisplayAttributeProperty;

            //Get the display attribute property. 
            hr = m_pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pDisplayAttributeProperty);
            if(SUCCEEDED(hr))
            {
                VARIANT var;

                VariantInit(&var);

                //All display attributes are TfGuidAtoms and TfGuidAtoms are VT_I4. 
                var.vt = VT_I4; 
                var.lVal = gaDisplayAttribute;

                //Set the display attribute value over the range. 
                hr = pDisplayAttributeProperty->SetValue(ec, tfSel.range, &var);

                pDisplayAttributeProperty->Release();
            }

            tfSel.range->Release();
        }
    }

    return S_OK;
}
```



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="0b7d6-129">Fourniture de l’objet d’informations d’attribut d’affichage</span><span class="sxs-lookup"><span data-stu-id="0b7d6-129">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="0b7d6-130">Un client obtient un objet **ITfDisplayAttributeInfo** de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b7d6-130">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="0b7d6-131">Le client appelle [ITfDisplayAttributeMgr :: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) avec l’identificateur **GUID** de l’attribut d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-131">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="0b7d6-132">La première fois que le client appelle **ITfDisplayAttributeMgr :: GetDisplayAttributeInfo**, le gestionnaire TSF crée une instance du fournisseur d’attributs d’affichage en appelant CoCreateInstance avec l’identificateur de classe passé comme premier paramètre à **ITfCategoryMgr :: RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-132">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="0b7d6-133">Les appels suivants à **ITfDisplayAttributeMgr :: GetDisplayAttributeInfo** réutiliseront l’objet de fournisseur d’attributs d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-133">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="0b7d6-134">Le gestionnaire TSF appelle ensuite [ITfDisplayAttributeProvider :: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) avec le **GUID** d’attribut d’affichage pour obtenir l’objet **ITfDisplayAttributeInfo** .</span><span class="sxs-lookup"><span data-stu-id="0b7d6-134">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="0b7d6-135">Le gestionnaire TSF transmet ensuite l’objet **ITfDisplayAttributeInfo** au client.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-135">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="0b7d6-136">Le client appelle [ITfDisplayAttributeMgr :: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) pour obtenir un objet **IEnumTfDisplayAttributeInfo** qui contient tous les attributs d’affichage fournis par tous les fournisseurs d’attributs d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-136">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="0b7d6-137">Le gestionnaire TSF énumère chaque fournisseur d’attributs d’affichage et crée une instance de chaque fournisseur en appelant CoCreateInstance avec l’identificateur de classe passé comme troisième paramètre à **ITfCategoryMgr :: RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-137">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="0b7d6-138">Le gestionnaire TSF appelle ensuite le **ITfDisplayAttributeProvider :: EnumDisplayAttributeInfo** de chaque fournisseur pour obtenir un objet **IEnumTfDisplayAttributeInfo** qui contient tous les attributs d’affichage fournis par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-138">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="0b7d6-139">Le gestionnaire TSF appelle ensuite la méthode [IEnumTfDisplayAttributeInfo :: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) du fournisseur, en ajoutant chaque objet **ITfDisplayAttributeInfo** obtenu au propre énumérateur du responsable, jusqu’à ce que la fin de l’énumération du fournisseur soit atteinte.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-139">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="0b7d6-140">Lorsque tous les objets **ITfDisplayAttributeInfo** de tous les fournisseurs d’attributs d’affichage sont ajoutés à l’énumérateur du gestionnaire TSF, le gestionnaire retourne son énumérateur au client.</span><span class="sxs-lookup"><span data-stu-id="0b7d6-140">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="0b7d6-141">Le client appelle ensuite **IEnumTfDisplayAttributeInfo :: Next** une ou plusieurs fois pour obtenir les objets **ITfDisplayAttributeInfo** .</span><span class="sxs-lookup"><span data-stu-id="0b7d6-141">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b7d6-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b7d6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b7d6-143">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="0b7d6-143">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="0b7d6-144">ITfCategoryMgr::RegisterCategory</span><span class="sxs-lookup"><span data-stu-id="0b7d6-144">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="0b7d6-145">ITfDisplayAttributeProvider</span><span class="sxs-lookup"><span data-stu-id="0b7d6-145">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="0b7d6-146">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="0b7d6-146">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="0b7d6-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="0b7d6-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="0b7d6-148">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="0b7d6-148">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="0b7d6-149">ITfRange</span><span class="sxs-lookup"><span data-stu-id="0b7d6-149">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="0b7d6-150">ITfProperty</span><span class="sxs-lookup"><span data-stu-id="0b7d6-150">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="0b7d6-151">ITfContext :: GetProperty</span><span class="sxs-lookup"><span data-stu-id="0b7d6-151">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="0b7d6-152">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="0b7d6-152">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="0b7d6-153">ITfCategoryMgr::RegisterGUID</span><span class="sxs-lookup"><span data-stu-id="0b7d6-153">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="0b7d6-154">ITfProperty :: SetValue</span><span class="sxs-lookup"><span data-stu-id="0b7d6-154">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="0b7d6-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="0b7d6-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="0b7d6-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="0b7d6-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="0b7d6-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="0b7d6-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="0b7d6-158">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="0b7d6-158">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="0b7d6-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="0b7d6-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="0b7d6-160">IEnumTfDisplayAttributeInfo :: suivant</span><span class="sxs-lookup"><span data-stu-id="0b7d6-160">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




