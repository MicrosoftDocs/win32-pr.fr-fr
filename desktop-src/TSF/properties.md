---
title: Propriétés (éléments communs)
description: Text Services Framework (TSF) fournit des propriétés qui associent les métadonnées à une plage de texte.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- Text Services Framework (TSF), propriétés
- TSF (Text Services Framework), propriétés
- services de texte, propriétés
- Applications compatibles TSF, propriétés
- properties
- Text Services Framework (TSF), types de propriété
- TSF (Text Services Framework), types de propriété
- services de texte, types de propriété
- Applications compatibles TSF, types de propriété
- types de propriétés
- Text Services Framework (TSF), stockage persistant des propriétés
- TSF (Text Services Framework), stockage persistant des propriétés
- services de texte, stockage persistant des propriétés
- Applications compatibles TSF, stockage persistant des propriétés
- stockage persistant des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff852bccfb7d9b6c94e57a2fa0cf8eef6fbdf18
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106541161"
---
# <a name="properties-common-elements"></a><span data-ttu-id="8d1f5-118">Propriétés (éléments communs)</span><span class="sxs-lookup"><span data-stu-id="8d1f5-118">Properties (Common Elements)</span></span>

<span data-ttu-id="8d1f5-119">Text Services Framework (TSF) fournit des propriétés qui associent les métadonnées à une plage de texte.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-119">Text Services Framework (TSF) provides properties that associate metadata with a range of text.</span></span> <span data-ttu-id="8d1f5-120">Ces propriétés incluent, sans s’y limiter, les attributs d’affichage tels que le texte en gras, l’identificateur de langue du texte et les données brutes fournies par un service de texte, telles que les données audio associées au texte du service de texte vocal.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-120">These properties include, but are not limited to, display attributes such as bold text, the language identifier of the text, and raw data provided by a text service such as the audio data associated with text from the speech text service.</span></span>

<span data-ttu-id="8d1f5-121">L’exemple suivant montre comment une propriété de couleur de texte hypothétique avec les valeurs possibles rouge (R), vert (G) ou bleu (B) peut être affichée.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-121">The following example demonstrates how a hypothetical text color property with possible values of red (R), green (G), or blue (B) can be viewed.</span></span>


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="8d1f5-122">Les propriétés de différents types peuvent se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-122">Properties of different types can overlap.</span></span> <span data-ttu-id="8d1f5-123">Par exemple, prenez l’exemple précédent et ajoutez un attribut de texte qui peut être gras (B) ou italique (I).</span><span class="sxs-lookup"><span data-stu-id="8d1f5-123">For example, take the previous example and add a text attribute that can be either bold (B) or italic (I).</span></span>


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="8d1f5-124">Le texte « This » est en gras, « is » est à la fois en gras et en rouge, « some » s’affiche normalement, « Color » est vert et en italique et « Text » est en italique.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-124">The text "this" would be bold, "is" would be both bold and red, "some" would be displayed normally, "colored" would be green and italicized and "text" would be italicized.</span></span>

<span data-ttu-id="8d1f5-125">Les propriétés du même type ne peuvent pas se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-125">Properties of the same type cannot overlap.</span></span> <span data-ttu-id="8d1f5-126">Par exemple, la situation suivante n’est pas autorisée, car « is » et « Color » ont des valeurs qui se chevauchent des mêmes types.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-126">For example, the following situation is not allowed because "is" and "colored" have overlapping values of the same types.</span></span>


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a><span data-ttu-id="8d1f5-127">Types de propriétés</span><span class="sxs-lookup"><span data-stu-id="8d1f5-127">Property Types</span></span>

<span data-ttu-id="8d1f5-128">TSF définit trois types de propriétés différents.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-128">TSF defines three different types of properties.</span></span>



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d1f5-129">statique</span><span class="sxs-lookup"><span data-stu-id="8d1f5-129">Static</span></span>         | <span data-ttu-id="8d1f5-130">Un objet de propriété statique stocke les données de propriété avec du texte.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-130">A static property object stores the property data with text.</span></span> <span data-ttu-id="8d1f5-131">Elle stocke également la plage d’informations de texte pour chaque plage à laquelle la propriété s’applique.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-131">It also stores the range of text information for each range that the property applies to.</span></span> <span data-ttu-id="8d1f5-132">ITfReadOnlyProperty :: GetType retourne la \_ \_ catégorie statique TFCAT PROPSTYLE de GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="8d1f5-132">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATIC category.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="8d1f5-133">Static-Compact</span><span class="sxs-lookup"><span data-stu-id="8d1f5-133">Static-Compact</span></span> | <span data-ttu-id="8d1f5-134">Un objet de propriété static-compact est identique à un objet de propriété statique, sauf qu’une propriété de compactage statique ne stocke pas de données de plage.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-134">A static-compact property object is identical to a static property object except a static-compact property does not store range data.</span></span> <span data-ttu-id="8d1f5-135">Lorsque la plage couverte par une propriété statique-compact est demandée, une plage est créée pour chaque groupe de propriétés adjacentes.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-135">When the range covered by a static-compact property is requested, a range is created for each group of adjacent properties.</span></span> <span data-ttu-id="8d1f5-136">Les propriétés statiques et compactes sont le moyen le plus efficace pour stocker des propriétés par caractère.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-136">Static-compact properties are the most efficient way to store properties on a per-character basis.</span></span> <span data-ttu-id="8d1f5-137">ITfReadOnlyProperty :: GetType retourne la \_ Catégorie GUID TFCAT \_ PROPSTYLE \_ STATICCOMPACT.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-137">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATICCOMPACT category.</span></span> |
| <span data-ttu-id="8d1f5-138">Custom</span><span class="sxs-lookup"><span data-stu-id="8d1f5-138">Custom</span></span>         | <span data-ttu-id="8d1f5-139">Un objet de propriété personnalisée stocke les informations de plage pour chaque plage à laquelle la propriété s’applique.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-139">A custom property object stores the range information for each range that the property applies to.</span></span> <span data-ttu-id="8d1f5-140">Toutefois, il ne stocke pas les données réelles de la propriété.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-140">It does not, however, store the actual data for the property.</span></span> <span data-ttu-id="8d1f5-141">Au lieu de cela, une propriété personnalisée stocke un objet ITfPropertyStore.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-141">Instead, a custom property stores an ITfPropertyStore object.</span></span> <span data-ttu-id="8d1f5-142">Le gestionnaire TSF utilise cet objet pour accéder aux données de propriété et les gérer. ITfReadOnlyProperty :: GetType retourne la \_ \_ catégorie personnalisée GUID TFCAT PROPSTYLE \_ .</span><span class="sxs-lookup"><span data-stu-id="8d1f5-142">The TSF manager uses this object to access and maintain the property data.ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_CUSTOM category.</span></span>                                                                    |



 

## <a name="working-with-properties"></a><span data-ttu-id="8d1f5-143">Utilisation des propriétés</span><span class="sxs-lookup"><span data-stu-id="8d1f5-143">Working with Properties</span></span>

<span data-ttu-id="8d1f5-144">La valeur de propriété et les attributs sont obtenus à l’aide de l’interface [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) et modifiés à l’aide de l’interface [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) .</span><span class="sxs-lookup"><span data-stu-id="8d1f5-144">The property value and attributes are obtained using the [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) interface and modified using the [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) interface.</span></span>

<span data-ttu-id="8d1f5-145">Si un type de propriété spécifique est requis, [ITfContext :: GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-145">If a specific property type is required, then [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) is used.</span></span> <span data-ttu-id="8d1f5-146">**ITfContext :: GetProperty** requiert un **GUID** qui identifie la propriété à obtenir.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-146">**ITfContext::GetProperty** requires a **GUID** that identifies the property to obtain.</span></span> <span data-ttu-id="8d1f5-147">TSF définit un ensemble d' [identificateurs de propriété prédéfinis](predefined-properties.md) utilisés ou un service de texte peut définir ses propres identificateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-147">TSF defines a set of [predefined property identifiers](predefined-properties.md) used or a text service can define its own property identifiers.</span></span> <span data-ttu-id="8d1f5-148">Si une propriété personnalisée est utilisée, le fournisseur de propriétés doit publier le **GUID** de la propriété et le format des données obtenues.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-148">If a custom property is used, the property provider must publish the property **GUID** and the format of the data obtained.</span></span>

<span data-ttu-id="8d1f5-149">Par exemple, pour obtenir le **CLSID** pour le propriétaire d’une plage de texte, appelez **ITfContext :: GetProperty** pour obtenir l’objet de propriété, appelez [ITfProperty :: FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) pour obtenir la plage qui couvre entièrement la propriété, puis appelez [ITfReadOnlyProperty :: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) pour obtenir une [TfGuidAtom](/windows/desktop/TSF/tfguidatom) qui représente le **CLSID** du service de texte qui possède le texte.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-149">For example, to obtain the **CLSID** for the owner of a range of text, call **ITfContext::GetProperty** to obtain the property object, call [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) to obtain the range that entirely covers the property, then call [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) to get a [TfGuidAtom](/windows/desktop/TSF/tfguidatom) that represents the **CLSID** of the text service that owns the text.</span></span> <span data-ttu-id="8d1f5-150">L’exemple suivant montre une fonction qui, étant donné un contexte, une plage et un cookie de modification, obtient le **CLSID** du service de texte qui possède le texte.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-150">The following example shows a function that, given a context, range and an edit cookie, will obtain the **CLSID** of the text service that owns the text.</span></span>


```C++
HRESULT GetTextOwner(   ITfContext *pContext, 
                        ITfRange *pRange, 
                        TfEditCookie ec, 
                        CLSID *pclsidOwner)
{
    HRESULT     hr;
    ITfProperty *pProp;

    *pclsidOwner = GUID_NULL;

    hr = pContext->GetProperty(GUID_PROP_TEXTOWNER, &pProp);
    if(S_OK == hr)
    {
        ITfRange    *pPropRange;

        hr = pProp->FindRange(ec, pRange, &pPropRange, TF_ANCHOR_START);
        if(S_OK == hr)
        {
            VARIANT var;

            VariantInit(&var);
            hr = pProp->GetValue(ec, pPropRange, &var);
            if(S_OK == hr)
            {
                if(VT_I4 == var.vt)
                {
                    /*
                    var.lVal is a TfGuidAtom that represents the CLSID of the 
                    text owner. Use ITfCategoryMgr to obtain the CLSID from 
                    the TfGuidAtom.
                    */
                    ITfCategoryMgr  *pCatMgr;

                    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                                            NULL, 
                                            CLSCTX_INPROC_SERVER, 
                                            IID_ITfCategoryMgr, 
                                            (LPVOID*)&pCatMgr);
                    if(SUCCEEDED(hr))
                    {
                        hr = pCatMgr->GetGUID((TfGuidAtom)var.lVal, pclsidOwner);
                        if(SUCCEEDED(hr))
                        {
                            /*
                            *pclsidOwner now contains the CLSID of the text 
                            service that owns the text at the selection.
                            */
                        }

                        pCatMgr->Release();
                    }
                }
                else
                {
                    //Unrecognized VARIANT type 
                    hr = E_FAIL;
                }
                
                VariantClear(&var);
            }
            
            pPropRange->Release();
        }
        
        pProp->Release();
    }

    return hr;
}

```



<span data-ttu-id="8d1f5-151">Les propriétés peuvent également être énumérées en obtenant une interface [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) à partir de [ITfContext :: EnumProperties,](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span><span class="sxs-lookup"><span data-stu-id="8d1f5-151">Properties can also be enumerated by obtaining an [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) interface from [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span></span>

## <a name="persistent-storage-of-properties"></a><span data-ttu-id="8d1f5-152">Stockage persistant des propriétés</span><span class="sxs-lookup"><span data-stu-id="8d1f5-152">Persistent Storage of Properties</span></span>

<span data-ttu-id="8d1f5-153">Souvent, les propriétés sont transparentes pour une application et sont utilisées par un ou plusieurs services de texte.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-153">Often, properties are transparent to an application and are used by one or more text services.</span></span> <span data-ttu-id="8d1f5-154">Pour conserver les données de propriété, par exemple lors de l’enregistrement dans un fichier, une application doit sérialiser les données de propriété lorsqu’elles sont stockées et désérialiser les données de propriété lorsque les données sont restaurées.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-154">In order to preserve the property data, such as when saving to a file, an application must serialize the property data when it is stored and unserialize the property data when the data is restored.</span></span> <span data-ttu-id="8d1f5-155">Dans ce cas, l’application ne doit pas être intéressée par des propriétés individuelles, mais elle doit énumérer toutes les propriétés dans le contexte et les stocker.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-155">In this case, the application should not be interested in individual properties, but should enumerate all properties in the context and store them.</span></span>

<span data-ttu-id="8d1f5-156">Lors du stockage des données de propriété, une application doit effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-156">When storing property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="8d1f5-157">Obtenez un énumérateur de propriété en appelant **ITfContext :: EnumProperties,**.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-157">Obtain a property enumerator by calling **ITfContext::EnumProperties**.</span></span>
2.  <span data-ttu-id="8d1f5-158">Énumérez chaque propriété en appelant [IEnumTfProperties :: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span><span class="sxs-lookup"><span data-stu-id="8d1f5-158">Enumerate each property by calling [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span></span>
3.  <span data-ttu-id="8d1f5-159">Pour chaque propriété, obtenez un énumérateur de plage en appelant [ITfReadOnlyProperty :: EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span><span class="sxs-lookup"><span data-stu-id="8d1f5-159">For each property, obtain a range enumerator by calling [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span></span>
4.  <span data-ttu-id="8d1f5-160">Énumérez chaque plage dans la propriété en appelant [IEnumTfRanges :: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span><span class="sxs-lookup"><span data-stu-id="8d1f5-160">Enumerate each range in the property by calling [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span></span>
5.  <span data-ttu-id="8d1f5-161">Pour chaque plage de la propriété, appelez [ITextStoreACPServices :: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) avec la propriété, Range, une structure [ \_ ACP d' \_ \_ en- \_ tête de propriété persistante TF](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) et un objet de flux implémenté par l’application.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-161">For each range in the property, call [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) with the property, range, a [TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) structure, and a stream object implemented by the application.</span></span>
6.  <span data-ttu-id="8d1f5-162">Écrivez le contenu de la structure ACP de l' **\_ \_ \_ en-tête \_ de propriété persistante TF** dans la mémoire persistante.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-162">Write the contents of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure into persistent memory.</span></span>
7.  <span data-ttu-id="8d1f5-163">Écrivez le contenu de l’objet de flux dans la mémoire persistante.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-163">Write the contents of the stream object into persistent memory.</span></span>
8.  <span data-ttu-id="8d1f5-164">Poursuivez les étapes précédentes pour toutes les plages dans toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-164">Continue the previous steps for all of the ranges in all of the properties.</span></span>
9.  <span data-ttu-id="8d1f5-165">L’application doit écrire un certain type de terminiator dans le flux afin que, lorsque les données sont restaurées, un point d’arrêt puisse être identifié.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-165">The application should write some type of terminiator into the stream so that, when the data is restored, a stopping point can be identified.</span></span>


```C++
HRESULT SaveProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        TfEditCookie ec, 
                        IStream *pStream)
{
    HRESULT             hr;
    IEnumTfProperties   *pEnumProps;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;
    ULONG uWritten;
    
    //Enumerate the properties in the context. 
    hr = pContext->EnumProperties(&pEnumProps);
    if(SUCCEEDED(hr))
    {
        ITfProperty *pProp;
        ULONG       uFetched;

        while(SUCCEEDED(pEnumProps->Next(1, &pProp, &uFetched)) && uFetched)
        {
            //Enumerate all the ranges that contain the property. 
            IEnumTfRanges   *pEnumRanges;
            hr = pProp->EnumRanges(ec, &pEnumRanges, NULL);
            if(SUCCEEDED(hr))
            {
                IStream *pTempStream;

                //Create a temporary stream to write the property data to. 
                hr = CreateStreamOnHGlobal(NULL, TRUE, &pTempStream);
                if(SUCCEEDED(hr))
                {
                    ITfRange    *pRange;

                    while(SUCCEEDED(pEnumRanges->Next(1, &pRange, &uFetched)) && uFetched)
                    {
                        LARGE_INTEGER li;

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);
                        
                        //Get the property header and data for the range. 
                        hr = pServices->Serialize(pProp, pRange, &PropHeader, pTempStream);

                        /*
                        Write the property header into the primary stream. 
                        The header also contains the size of the property 
                        data.
                        */
                        hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);

                        //Copy the property data from the temporary stream into the primary stream. 
                        ULARGE_INTEGER  uli;
                        uli.QuadPart = PropHeader.cb;

                        hr = pTempStream->CopyTo(pStream, uli, NULL, NULL);

                        pRange->Release();
                    }
                    
                    pTempStream->Release();
                }
                
                pEnumRanges->Release();
            }
            
            pProp->Release();
        }
        
        pEnumProps->Release();
    }

    //Write a property header with zero size and guid into the stream as a terminator 
    ZeroMemory(&PropHeader, sizeof(PropHeader));
    hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

    return hr;
}

```



<span data-ttu-id="8d1f5-166">**ITextStoreACPServices :: Serialize**[ITfPropertyStore :: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span><span class="sxs-lookup"><span data-stu-id="8d1f5-166">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span></span>

<span data-ttu-id="8d1f5-167">Lors de la restauration des données de propriétés, une application doit effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-167">When restoring property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="8d1f5-168">Définissez le pointeur de flux sur le début de la première structure ACP de l' **\_ \_ \_ en-tête \_ de propriété persistante TF** .</span><span class="sxs-lookup"><span data-stu-id="8d1f5-168">Set the stream pointer to the start of the first **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
2.  <span data-ttu-id="8d1f5-169">Lisez la structure ACP de l' **\_ \_ \_ en-tête \_ de propriété persistante TF** .</span><span class="sxs-lookup"><span data-stu-id="8d1f5-169">Read the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
3.  <span data-ttu-id="8d1f5-170">Appelez **ITfContext :: GetProperty** avec le membre **guidType** de la structure ACP de l' **\_ \_ \_ en-tête \_ de propriété persistante TF** .</span><span class="sxs-lookup"><span data-stu-id="8d1f5-170">Call **ITfContext::GetProperty** with the **guidType** member of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
4.  <span data-ttu-id="8d1f5-171">À ce stade, l’application peut effectuer l’une des deux opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d1f5-171">The application can do one of two things at this point.</span></span>
    1.  <span data-ttu-id="8d1f5-172">Créer une instance d’un objet [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) que l’application doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-172">Create an instance of an [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) object that the application must implement.</span></span> <span data-ttu-id="8d1f5-173">Appelez ensuite [ITextStoreACPServices :: unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) avec **null** pour *pStream* et le pointeur **ITfPersistentPropertyLoaderACP** .</span><span class="sxs-lookup"><span data-stu-id="8d1f5-173">Then call [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) with **NULL** for *pStream* and the **ITfPersistentPropertyLoaderACP** pointer.</span></span>
    2.  <span data-ttu-id="8d1f5-174">Transmettez le flux d’entrée à **ITextStoreACPServices :: unserialize** et **null** pour *pLoader*.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-174">Pass the input stream to **ITextStoreACPServices::Unserialize** and **NULL** for *pLoader*.</span></span>

    <span data-ttu-id="8d1f5-175">La première méthode est préférable, car elle est la plus efficace.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-175">The first method is preferred as it is the most efficient.</span></span> <span data-ttu-id="8d1f5-176">Si vous implémentez la deuxième méthode, toutes les données de propriété sont lues à partir du flux pendant l’appel de **ITextStoreACPServices :: unserialize** .</span><span class="sxs-lookup"><span data-stu-id="8d1f5-176">Implementing the second method causes all of the property data to be read from the stream during the **ITextStoreACPServices::Unserialize** call.</span></span> <span data-ttu-id="8d1f5-177">La première méthode fait en sorte que les données de propriété soient lues à la demande ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-177">The first method causes the property data to be read on demand at a later time.</span></span>
5.  <span data-ttu-id="8d1f5-178">Répétez les étapes précédentes jusqu’à ce que tous les blocs de propriété soient désérialisés.</span><span class="sxs-lookup"><span data-stu-id="8d1f5-178">Repeat the previous steps until all property blocks are unserialized.</span></span>


```C++
HRESULT LoadProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        IStream *pStream)
{
    HRESULT hr;
    ULONG   uRead;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;

    /*
    Read each property header and property data from the stream. The 
    list of properties is terminated by a TF_PERSISTENT_PROPERTY_HEADER_ACP 
    structure with a cb member of zero.
    */
    hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    while(  SUCCEEDED(hr) && 
            (sizeof(PropHeader) == uRead) && 
            (0 != PropHeader.cb))
    {
        ITfProperty *pProp;

        hr = pContext->GetProperty(PropHeader.guidType, &pProp);
        if(SUCCEEDED(hr))
        {
            /*
            Have TSF read the property data from the stream. This call 
            requests a read-only lock, so be sure it can be granted 
            or else this method will fail.
            */
            CTSFPersistentPropertyLoader *pLoader = new CTSFPersistentPropertyLoader(&PropHeader, pStream);
            hr = pServices->Unserialize(pProp, &PropHeader, NULL, pLoader);

            pProp->Release();
        }

        //Read the next header. 
        hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    }

    return hr;
}

```



 

 
