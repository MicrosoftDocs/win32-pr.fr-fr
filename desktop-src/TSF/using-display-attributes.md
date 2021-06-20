---
title: Utilisation des attributs d’affichage
description: Apprenez à utiliser des attributs d’affichage. Text Services Framework (TSF) permet à un service de texte de fournir des attributs d’affichage pour le texte.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Text Services Framework (TSF), attributs d’affichage
- TSF (Text Services Framework), attributs d’affichage
- Applications compatibles TSF, attributs d’affichage
- attributs d'affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3c576064ab22571b5a7822f5e6ff143add55d03
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406132"
---
# <a name="using-display-attributes"></a><span data-ttu-id="34cfb-108">Utilisation des attributs d’affichage</span><span class="sxs-lookup"><span data-stu-id="34cfb-108">Using Display Attributes</span></span>

<span data-ttu-id="34cfb-109">Text Services Framework (TSF) permet à un service de texte de fournir des attributs d’affichage pour le texte.</span><span class="sxs-lookup"><span data-stu-id="34cfb-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="34cfb-110">Cela permet à une application d’afficher des commentaires visuels supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="34cfb-110">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="34cfb-111">Par exemple, un service de texte du vérificateur d’orthographe peut mettre en surbrillance un mot mal orthographié avec un trait de soulignement rouge.</span><span class="sxs-lookup"><span data-stu-id="34cfb-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="34cfb-112">Les attributs d’affichage qui peuvent être fournis sont définis par la structure [tf \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) et incluent la couleur de texte, la couleur d’arrière-plan du texte, le style de soulignement, la couleur du soulignement et la pondération du soulignement.</span><span class="sxs-lookup"><span data-stu-id="34cfb-112">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="34cfb-113">Lors du rendu de texte, une application doit obtenir les attributs d’affichage du texte dessiné et utiliser les attributs pour modifier la façon dont le texte est dessiné.</span><span class="sxs-lookup"><span data-stu-id="34cfb-113">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="34cfb-114">Procédez comme suit pour obtenir les attributs d’affichage.</span><span class="sxs-lookup"><span data-stu-id="34cfb-114">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="34cfb-115">Obtenez un objet de propriété pour \_ \_ l’attribut prop GUID en appelant [ITfContext :: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span><span class="sxs-lookup"><span data-stu-id="34cfb-115">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="34cfb-116">Obtenez la valeur de l' \_ attribut prop GUID \_ pour la plage spécifiée en appelant [ITfReadOnlyProperty :: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span><span class="sxs-lookup"><span data-stu-id="34cfb-116">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="34cfb-117">Cela fournit une valeur [TfGuidAtom](tfguidatom.md) .</span><span class="sxs-lookup"><span data-stu-id="34cfb-117">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="34cfb-118">Convertit la valeur [TfGuidAtom](tfguidatom.md) en GUID en appelant [ITfCategoryMgr :: GetGuid](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span><span class="sxs-lookup"><span data-stu-id="34cfb-118">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="34cfb-119">Créez un objet [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) pour l’attribut Display en appelant [ITfDisplayAttributeMgr :: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="34cfb-119">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="34cfb-120">Obtenez les informations d’attribut d’affichage en appelant [ITfDisplayAttributeInfo :: GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="34cfb-120">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="34cfb-121">L’exemple de code suivant illustre une fonction qui obtient les attributs d’affichage à partir d’un contexte, d’une plage et d’un cookie de modification fournis.</span><span class="sxs-lookup"><span data-stu-id="34cfb-121">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="34cfb-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34cfb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34cfb-123">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="34cfb-123">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="34cfb-124">ITfContext :: GetProperty</span><span class="sxs-lookup"><span data-stu-id="34cfb-124">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="34cfb-125">ITfReadOnlyProperty :: GetValue</span><span class="sxs-lookup"><span data-stu-id="34cfb-125">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="34cfb-126">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="34cfb-126">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="34cfb-127">ITfCategoryMgr :: GetGUID</span><span class="sxs-lookup"><span data-stu-id="34cfb-127">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="34cfb-128">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="34cfb-128">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="34cfb-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="34cfb-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="34cfb-130">ITfDisplayAttributeInfo::GetAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="34cfb-130">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




