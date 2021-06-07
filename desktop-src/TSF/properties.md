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
ms.openlocfilehash: f5b94a1f6c504fcd3e6491af9e66b399d59a3eeb
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524213"
---
# <a name="properties-common-elements"></a>Propriétés (éléments communs)

Text Services Framework (TSF) fournit des propriétés qui associent les métadonnées à une plage de texte. Ces propriétés incluent, sans s’y limiter, les attributs d’affichage tels que le texte en gras, l’identificateur de langue du texte et les données brutes fournies par un service de texte, telles que les données audio associées au texte du service de texte vocal.

L’exemple suivant montre comment une propriété de couleur de texte hypothétique avec les valeurs possibles rouge (R), vert (G) ou bleu (B) peut être affichée.


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Les propriétés de différents types peuvent se chevaucher. Par exemple, prenez l’exemple précédent et ajoutez un attribut de texte qui peut être gras (B) ou italique (I).


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Le texte « This » est en gras, « is » est à la fois en gras et en rouge, « some » s’affiche normalement, « Color » est vert et en italique et « Text » est en italique.

Les propriétés du même type ne peuvent pas se chevaucher. Par exemple, la situation suivante n’est pas autorisée, car « is » et « Color » ont des valeurs qui se chevauchent des mêmes types.


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a>Types de propriétés

TSF définit trois types de propriétés différents.



|   Type de propriété             |   Description                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| statique         | Un objet de propriété statique stocke les données de propriété avec du texte. Elle stocke également la plage d’informations de texte pour chaque plage à laquelle la propriété s’applique. ITfReadOnlyProperty :: GetType retourne la \_ \_ catégorie statique TFCAT PROPSTYLE de GUID \_ .                                                                                                                                                                                                                      |
| Static-Compact | Un objet de propriété static-compact est identique à un objet de propriété statique, sauf qu’une propriété de compactage statique ne stocke pas de données de plage. Lorsque la plage couverte par une propriété statique-compact est demandée, une plage est créée pour chaque groupe de propriétés adjacentes. Les propriétés statiques et compactes sont le moyen le plus efficace pour stocker des propriétés par caractère. ITfReadOnlyProperty :: GetType retourne la \_ Catégorie GUID TFCAT \_ PROPSTYLE \_ STATICCOMPACT. |
| Custom         | Un objet de propriété personnalisée stocke les informations de plage pour chaque plage à laquelle la propriété s’applique. Toutefois, il ne stocke pas les données réelles de la propriété. Au lieu de cela, une propriété personnalisée stocke un objet ITfPropertyStore. Le gestionnaire TSF utilise cet objet pour accéder aux données de propriété et les gérer. ITfReadOnlyProperty :: GetType retourne la \_ \_ catégorie personnalisée GUID TFCAT PROPSTYLE \_ .                                                                    |



 

## <a name="working-with-properties"></a>Utilisation des propriétés

La valeur de propriété et les attributs sont obtenus à l’aide de l’interface [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) et modifiés à l’aide de l’interface [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) .

Si un type de propriété spécifique est requis, [ITfContext :: GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) est utilisé. **ITfContext :: GetProperty** requiert un **GUID** qui identifie la propriété à obtenir. TSF définit un ensemble d' [identificateurs de propriété prédéfinis](predefined-properties.md) utilisés ou un service de texte peut définir ses propres identificateurs de propriété. Si une propriété personnalisée est utilisée, le fournisseur de propriétés doit publier le **GUID** de la propriété et le format des données obtenues.

Par exemple, pour obtenir le **CLSID** pour le propriétaire d’une plage de texte, appelez **ITfContext :: GetProperty** pour obtenir l’objet de propriété, appelez [ITfProperty :: FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) pour obtenir la plage qui couvre entièrement la propriété, puis appelez [ITfReadOnlyProperty :: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) pour obtenir une [TfGuidAtom](/windows/desktop/TSF/tfguidatom) qui représente le **CLSID** du service de texte qui possède le texte. L’exemple suivant montre une fonction qui, étant donné un contexte, une plage et un cookie de modification, obtient le **CLSID** du service de texte qui possède le texte.


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



Les propriétés peuvent également être énumérées en obtenant une interface [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) à partir de [ITfContext :: EnumProperties,](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).

## <a name="persistent-storage-of-properties"></a>Stockage persistant des propriétés

Souvent, les propriétés sont transparentes pour une application et sont utilisées par un ou plusieurs services de texte. Pour conserver les données de propriété, par exemple lors de l’enregistrement dans un fichier, une application doit sérialiser les données de propriété lorsqu’elles sont stockées et désérialiser les données de propriété lorsque les données sont restaurées. Dans ce cas, l’application ne doit pas être intéressée par des propriétés individuelles, mais elle doit énumérer toutes les propriétés dans le contexte et les stocker.

Lors du stockage des données de propriété, une application doit effectuer les étapes suivantes.

1.  Obtenez un énumérateur de propriété en appelant **ITfContext :: EnumProperties,**.
2.  Énumérez chaque propriété en appelant [IEnumTfProperties :: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).
3.  Pour chaque propriété, obtenez un énumérateur de plage en appelant [ITfReadOnlyProperty :: EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).
4.  Énumérez chaque plage dans la propriété en appelant [IEnumTfRanges :: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).
5.  Pour chaque plage de la propriété, appelez [ITextStoreACPServices :: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) avec la propriété, Range, une structure [ \_ ACP d' \_ \_ en- \_ tête de propriété persistante TF](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) et un objet de flux implémenté par l’application.
6.  Écrivez le contenu de la structure ACP de l' **\_ \_ \_ en-tête \_ de propriété persistante TF** dans la mémoire persistante.
7.  Écrivez le contenu de l’objet de flux dans la mémoire persistante.
8.  Poursuivez les étapes précédentes pour toutes les plages dans toutes les propriétés.
9.  L’application doit écrire un certain type de terminiator dans le flux afin que, lorsque les données sont restaurées, un point d’arrêt puisse être identifié.


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



**ITextStoreACPServices :: Serialize**[ITfPropertyStore :: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)

Lors de la restauration des données de propriétés, une application doit effectuer les étapes suivantes.

1.  Définissez le pointeur de flux sur le début de la première structure ACP de l' **\_ \_ \_ en-tête \_ de propriété persistante TF** .
2.  Lisez la structure ACP de l' **\_ \_ \_ en-tête \_ de propriété persistante TF** .
3.  Appelez **ITfContext :: GetProperty** avec le membre **guidType** de la structure ACP de l' **\_ \_ \_ en-tête \_ de propriété persistante TF** .
4.  À ce stade, l’application peut effectuer l’une des deux opérations suivantes :
    1.  Créer une instance d’un objet [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) que l’application doit implémenter. Appelez ensuite [ITextStoreACPServices :: unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) avec **null** pour *pStream* et le pointeur **ITfPersistentPropertyLoaderACP** .
    2.  Transmettez le flux d’entrée à **ITextStoreACPServices :: unserialize** et **null** pour *pLoader*.

    La première méthode est préférable, car elle est la plus efficace. Si vous implémentez la deuxième méthode, toutes les données de propriété sont lues à partir du flux pendant l’appel de **ITextStoreACPServices :: unserialize** . La première méthode fait en sorte que les données de propriété soient lues à la demande ultérieurement.
5.  Répétez les étapes précédentes jusqu’à ce que tous les blocs de propriété soient désérialisés.


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



 

 
