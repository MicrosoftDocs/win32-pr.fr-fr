---
description: quand un appareil est créé, Windows acquisition d’images (wia) crée une arborescence hiérarchique des éléments WIA qui représentent l’appareil et les dossiers et images associés à cet appareil.
ms.assetid: ab7246e8-47bb-4b94-8d91-1c22010ebd9f
title: Énumération d’éléments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c216e658b7105f6b3d88d01bd55a3200af7e45c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231083"
---
# <a name="enumerating-items"></a>Énumération d’éléments

quand un appareil est créé, Windows acquisition d’images (wia) crée une arborescence hiérarchique des éléments WIA qui représentent l’appareil et les dossiers et images associés à cet appareil. Utilisez la méthode de l’élément racine (élément à la racine de l’arborescence qui représente le périphérique) [**IWiaItem :: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (ou [**IWiaItem2 :: EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) pour créer un objet énumérateur et obtenir un pointeur vers son interface [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (ou [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)), qui est utilisée pour naviguer dans l’arborescence d’éléments et accéder aux images ou aux lits d’analyse associés à l’appareil.

L’exemple suivant illustre une fonction qui énumère de manière récursive tous les éléments d’une arborescence, en commençant par un élément racine passé à la fonction.


```
    HRESULT EnumerateItems( IWiaItem *pWiaItem ) //XP or earlier
    HRESULT EnumerateItems( IWiaItem2 *pWiaItem ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaItem)
        {
            return E_INVALIDARG;
        }

        //
        // Get the item type for this item.
        //
        LONG lItemType = 0;
        HRESULT hr = pWiaItem->GetItemType( &lItemType );
        if (SUCCEEDED(hr))
        {
            //
            // If it is a folder, or it has attachments, enumerate its children.
            //
            if (lItemType & WiaItemTypeFolder || lItemType & WiaItemTypeHasAttachments)
            {
                //
                // Get the child item enumerator for this item.
                //
                IEnumWiaItem *pEnumWiaItem = NULL; //XP or earlier
                IEnumWiaItem2 *pEnumWiaItem = NULL; //Vista or later
                
                hr = pWiaItem->EnumChildItems( &pEnumWiaItem );
                if (SUCCEEDED(hr))
                {
                    //
                    // Loop until you get an error or pEnumWiaItem->Next returns
                    // S_FALSE to signal the end of the list.
                    //
                    while (S_OK == hr)
                    {
                        //
                        // Get the next child item.
                        //
                        IWiaItem *pChildWiaItem = NULL; //XP or earlier
                        IWiaItem2 *pChildWiaItem = NULL; //Vista or later
                        
                        hr = pEnumWiaItem->Next( 1, &pChildWiaItem, NULL );

                        //
                        // pEnumWiaItem->Next will return S_FALSE when the list is
                        // exhausted, so check for S_OK before using the returned
                        // value.
                        //
                        if (S_OK == hr)
                        {
                            //
                            // Recurse into this item.
                            //
                            hr = EnumerateItems( pChildWiaItem );

                            //
                            // Release this item.
                            //
                            pChildWiaItem->Release();
                            pChildWiaItem = NULL;
                        }
                    }

                    //
                    // If the result of the enumeration is S_FALSE (which
                    // is normal), change it to S_OK.
                    //
                    if (S_FALSE == hr)
                    {
                        hr = S_OK;
                    }

                    //
                    // Release the enumerator.
                    //
                    pEnumWiaItem->Release();
                    pEnumWiaItem = NULL;
                }
            }
        }
        return  hr;
    }
```



La fonction prend le paramètre **pWiaItem**, un pointeur vers l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (ou [**IWiaItem2**](-wia-iwiaitem2.md)) de l’élément racine de l’arborescence d’éléments à énumérer.

Tout d’abord, la fonction vérifie si l’élément est un dossier ou s’il contient des pièces jointes. Si c’est le cas, il appelle ensuite la méthode [**IWiaItem :: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (ou [**IWiaItem2 :: EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) de **pWiaItem** pour créer un objet énumérateur pour l’arborescence d’éléments. Si cet appel se déroule correctement et que l’énumérateur est valide, la fonction itère au sein des éléments enfants et s’appelle de manière récursive sur chaque élément, en traitant chacun comme un élément racine potentiel pour le niveau suivant d’éléments enfants.

De cette manière, la fonction énumère toutes les branches de l’arborescence d’éléments sous l’élément racine passé à **EnumerateItems**.

 

 



