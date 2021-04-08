---
title: Utilisation des attributs d’affichage
description: Text Services Framework (TSF) permet à un service de texte de fournir des attributs d’affichage pour le texte.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Text Services Framework (TSF), attributs d’affichage
- TSF (Text Services Framework), attributs d’affichage
- Applications compatibles TSF, attributs d’affichage
- attributs d'affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc725f67fab904db23f6232ac5efb5d63c62c26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671762"
---
# <a name="using-display-attributes"></a>Utilisation des attributs d’affichage

Text Services Framework (TSF) permet à un service de texte de fournir des attributs d’affichage pour le texte. Cela permet à une application d’afficher des commentaires visuels supplémentaires. Par exemple, un service de texte du vérificateur d’orthographe peut mettre en surbrillance un mot mal orthographié avec un trait de soulignement rouge. Les attributs d’affichage qui peuvent être fournis sont définis par la structure [tf \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) et incluent la couleur de texte, la couleur d’arrière-plan du texte, le style de soulignement, la couleur du soulignement et la pondération du soulignement.

Lors du rendu de texte, une application doit obtenir les attributs d’affichage du texte dessiné et utiliser les attributs pour modifier la façon dont le texte est dessiné. Procédez comme suit pour obtenir les attributs d’affichage.

1.  Obtenez un objet de propriété pour \_ \_ l’attribut prop GUID en appelant [ITfContext :: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).
2.  Obtenez la valeur de l' \_ attribut prop GUID \_ pour la plage spécifiée en appelant [ITfReadOnlyProperty :: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue). Cela fournit une valeur [TfGuidAtom](tfguidatom.md) .
3.  Convertit la valeur [TfGuidAtom](tfguidatom.md) en GUID en appelant [ITfCategoryMgr :: GetGuid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).
4.  Créez un objet [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) pour l’attribut Display en appelant [ITfDisplayAttributeMgr :: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).
5.  Obtenez les informations d’attribut d’affichage en appelant [ITfDisplayAttributeInfo :: GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).

L’exemple de code suivant illustre une fonction qui obtient les attributs d’affichage à partir d’un contexte, d’une plage et d’un cookie de modification fournis.


```C++
HRESULT GetDispAttrFromRange(   ITfContext *pContext, 
                                ITfRange *pRange, 
                                TfEditCookie ec, 
                                TF_DISPLAYATTRIBUTE *pDispAttr)
{
    HRESULT     hr;
    
    //Create the category manager. 
    ITfCategoryMgr  *pCategoryMgr;
    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfCategoryMgr, 
                            (LPVOID*)&pCategoryMgr);
    if(FAILED(hr))
    {
        return hr;
    }

    //Create the display attribute manager. 
    ITfDisplayAttributeMgr  *pDispMgr;
    hr = CoCreateInstance(  CLSID_TF_DisplayAttributeMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfDisplayAttributeMgr, 
                            (LPVOID*)&pDispMgr);
    if(FAILED(hr))
    {
        pCategoryMgr->Release();
        return hr;
    }
    
    //Get the display attribute property. 
    ITfProperty *pProp;
    hr = pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pProp);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);
        hr = pProp->GetValue(ec, pRange, &var);
        if(S_OK == hr)  //Returns S_FALSE if the range is not completely covered by the property.  
        {
            if(VT_I4 == var.vt)
            {
                //The property is a guidatom. 
                GUID    guid;

                //Convert the guidatom into a GUID. 
                hr = pCategoryMgr->GetGUID((TfGuidAtom)var.lVal, &guid);
                if(SUCCEEDED(hr))
                {
                    ITfDisplayAttributeInfo *pDispInfo;

                    //Get the display attribute info object for this attribute. 
                    hr = pDispMgr->GetDisplayAttributeInfo(guid, &pDispInfo, NULL);
                    if(SUCCEEDED(hr))
                    {
                        //Get the display attribute info. 
                        hr = pDispInfo->GetAttributeInfo(pDispAttr);

                        pDispInfo->Release();
                    }
                }
            }
            else
            {
                //An error occurred; GUID_PROP_ATTRIBUTE must always be VT_I4. 
                hr = E_FAIL;
            }
            VariantClear(&var);
        }
    pProp->Release();
    }

    pCategoryMgr->Release();
    pDispMgr->Release();

    return hr;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfContext :: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[ITfReadOnlyProperty :: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr :: GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 ITfDisplayAttributeInfo::GetAttributeInfo 
</dt> </dl>

 

 




