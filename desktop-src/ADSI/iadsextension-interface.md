---
title: Interface IADsExtension
description: Cet article contient la définition de code C++ de l’interface IADsExtension et une discussion de ses méthodes.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- IADsExtension ADSI, utilisation
- ADSI ADSI, exemple de code C/C++, utilisant IADsExtension
- extensions ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7d59048d29620cdc2d3703b9ba26a852441a47
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405942"
---
# <a name="iadsextension-interface"></a>Interface IADsExtension

L’interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) est définie comme suit :


```C++
IADsExtension : public IUnknown
    {
    public:
        virtual HRESULT STDMETHODCALLTYPE Operate( 
            /* [in] */ DWORD dwCode,
            /* [in] */ VARIANT varData1,
            /* [in] */ VARIANT varData2,
            /* [in] */ VARIANT varData3) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateGetIDsOfNames( 
            /* [in] */ REFIID riid,
            /* [in] */ OLECHAR **rgszNames,
            /* [in] */ unsigned int cNames,
            /* [in] */ LCID lcid,
            /* [out] */ DISPID *rgDispid) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateInvoke( 
            /* [in] */ DISPID dispidMember,
            /* [in] */ REFIID riid,
            /* [in] */ LCID lcid,
            /* [in] */ WORD wFlags,
            /* [in] */ DISPPARAMS *pdispparams,
            /* [out] */ VARIANT *pvarResult,
            /* [out] */ EXCEPINFO *pexcepinfo,
            /* [out] */ unsigned int *puArgErr) = 0;
    };
```



L’agrégateur (ADSI) appelle la méthode [**IADsExtension :: action**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) . L’extension doit interpréter le paramètre *dwCode* et chaque paramètre *varData* , conformément à la documentation du fournisseur.

L’agrégateur (ADSI) appelle la méthode [**IADsExtension ::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . Elle est appelée après que ADSI a déterminé l’extension pour la maintenance de la distribution. L’extension peut utiliser les informations de type pour obtenir le DISPID, autrement dit, à l’aide de la fonction [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) .

ADSI appelle normalement la méthode [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) après avoir appelé la fonction [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . L’extension doit appeler la méthode réelle qu’elle implémente. L’extension peut également utiliser les informations de type et appeler la fonction [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) .

Tous les paramètres ont la même signification que les paramètres de la méthode [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) standard.

 

 