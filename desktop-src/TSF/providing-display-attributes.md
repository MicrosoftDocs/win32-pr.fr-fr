---
title: Fournir des attributs d’affichage
description: Text Services Framework (TSF) permet à un service de texte de fournir des attributs d’affichage pour le texte.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Text Services Framework (TSF), attributs d’affichage
- TSF (Text Services Framework), attributs d’affichage
- services de texte, attributs d’affichage
- attributs d'affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f59bb64ef4f06df020a40189d273c703768d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509590"
---
# <a name="providing-display-attributes"></a>Fournir des attributs d’affichage

Text Services Framework (TSF) permet à un service de texte de fournir des attributs d’affichage pour le texte. Cela permet de fournir des commentaires visuels supplémentaires à l’utilisateur. Par exemple, un service de texte du vérificateur d’orthographe peut mettre en surbrillance un mot mal orthographié avec un trait de soulignement rouge. Les attributs d’affichage fournis sont définis par la structure [tf \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) et incluent la couleur de texte, la couleur d’arrière-plan du texte, le style de soulignement, la couleur du soulignement et le trait de soulignement.

Les clients qui utilisent ces informations d’attribut d’affichage sont plus souvent des applications, mais ils peuvent également inclure des services de texte. Le gestionnaire TSF effectue une médiation entre le fournisseur d’attributs d’affichage et le client et effectue le suivi du fournisseur d’attributs d’affichage des attributs d’affichage spécifiques.

Pour fournir des attributs d’affichage, un service de texte doit effectuer les opérations suivantes.

1.  Inscrivez le service de texte en tant que fournisseur d’attributs d’affichage en appelant [ITfCategoryMgr :: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) avec l’identificateur de classe du service de texte pour le premier paramètre, Guid \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER pour le deuxième paramètre et l’identificateur de classe du service de texte pour le troisième paramètre.
2.  Implémentez [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) et rendez-le disponible à partir de la fabrique de classes.
3.  Implémentez [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) et rendez-le disponible à partir de [ITfDisplayAttributeProvider :: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).
4.  Implémentez un objet [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) pour chaque type d’attribut d’affichage fourni par le service de texte.

## <a name="applying-the-display-attributes"></a>Application des attributs d’affichage

Le service de texte doit appliquer l’attribut d’affichage à une plage de texte. Un service de texte peut uniquement modifier la valeur de la propriété pendant une session de modification en lecture/écriture.

En supposant qu’il s’agit d’une session de modification en lecture/écriture, un attribut d’affichage est appliqué de la manière suivante.

1.  Obtenez un objet [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) qui couvre le texte auquel l’attribut d’affichage sera appliqué.
2.  Obtenez un objet [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) pour les attributs de texte en appelant [ITfContext :: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) avec l' \_ attribut prop GUID \_ .
3.  Créez un [TfGuidAtom](tfguidatom.md) à partir du **GUID** de l’identificateur d’attribut d’affichage défini par le service de texte en appelant [ITfCategoryMgr :: RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).
4.  Initialisez une variable VARIANT sur VT \_ I4 et définissez le membre **lVal** sur le **TfGuidAtom** créé à l’étape précédente.
5.  Appliquez l’attribut Display à la plage en appelant [ITfProperty :: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) avec le cookie de modification en lecture/écriture, la plage et la variante initialisée à l’étape précédente.


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



## <a name="supplying-the-display-attribute-information-object"></a>Fourniture de l’objet d’informations d’attribut d’affichage

Un client obtient un objet **ITfDisplayAttributeInfo** de l’une des deux manières suivantes :

1.  Le client appelle [ITfDisplayAttributeMgr :: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) avec l’identificateur **GUID** de l’attribut d’affichage. La première fois que le client appelle **ITfDisplayAttributeMgr :: GetDisplayAttributeInfo**, le gestionnaire TSF crée une instance du fournisseur d’attributs d’affichage en appelant CoCreateInstance avec l’identificateur de classe passé comme premier paramètre à **ITfCategoryMgr :: RegisterCategory**. Les appels suivants à **ITfDisplayAttributeMgr :: GetDisplayAttributeInfo** réutiliseront l’objet de fournisseur d’attributs d’affichage.

    Le gestionnaire TSF appelle ensuite [ITfDisplayAttributeProvider :: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) avec le **GUID** d’attribut d’affichage pour obtenir l’objet **ITfDisplayAttributeInfo** .

    Le gestionnaire TSF transmet ensuite l’objet **ITfDisplayAttributeInfo** au client.

2.  Le client appelle [ITfDisplayAttributeMgr :: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) pour obtenir un objet **IEnumTfDisplayAttributeInfo** qui contient tous les attributs d’affichage fournis par tous les fournisseurs d’attributs d’affichage. Le gestionnaire TSF énumère chaque fournisseur d’attributs d’affichage et crée une instance de chaque fournisseur en appelant CoCreateInstance avec l’identificateur de classe passé comme troisième paramètre à **ITfCategoryMgr :: RegisterCategory**.

    Le gestionnaire TSF appelle ensuite le **ITfDisplayAttributeProvider :: EnumDisplayAttributeInfo** de chaque fournisseur pour obtenir un objet **IEnumTfDisplayAttributeInfo** qui contient tous les attributs d’affichage fournis par le fournisseur.

    Le gestionnaire TSF appelle ensuite la méthode [IEnumTfDisplayAttributeInfo :: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) du fournisseur, en ajoutant chaque objet **ITfDisplayAttributeInfo** obtenu au propre énumérateur du responsable, jusqu’à ce que la fin de l’énumération du fournisseur soit atteinte.

    Lorsque tous les objets **ITfDisplayAttributeInfo** de tous les fournisseurs d’attributs d’affichage sont ajoutés à l’énumérateur du gestionnaire TSF, le gestionnaire retourne son énumérateur au client. Le client appelle ensuite **IEnumTfDisplayAttributeInfo :: Next** une ou plusieurs fois pour obtenir les objets **ITfDisplayAttributeInfo** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[ITfContext :: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[ITfProperty :: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 IEnumTfDisplayAttributeInfo 
</dt> <dt>

 ITfDisplayAttributeProvider::EnumDisplayAttributeInfo 
</dt> <dt>

[IEnumTfDisplayAttributeInfo :: suivant](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




