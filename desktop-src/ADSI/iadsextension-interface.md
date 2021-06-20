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
# <a name="iadsextension-interface"></a><span data-ttu-id="08604-106">Interface IADsExtension</span><span class="sxs-lookup"><span data-stu-id="08604-106">IADsExtension Interface</span></span>

<span data-ttu-id="08604-107">L’interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="08604-107">The [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface is defined as follows:</span></span>


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



<span data-ttu-id="08604-108">L’agrégateur (ADSI) appelle la méthode [**IADsExtension :: action**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .</span><span class="sxs-lookup"><span data-stu-id="08604-108">The aggregator (ADSI) calls the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span> <span data-ttu-id="08604-109">L’extension doit interpréter le paramètre *dwCode* et chaque paramètre *varData* , conformément à la documentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="08604-109">The extension should interpret the *dwCode* parameter and each *varData* parameter, according to the provider's documentation.</span></span>

<span data-ttu-id="08604-110">L’agrégateur (ADSI) appelle la méthode [**IADsExtension ::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="08604-110">The aggregator (ADSI), calls the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) method.</span></span> <span data-ttu-id="08604-111">Elle est appelée après que ADSI a déterminé l’extension pour la maintenance de la distribution.</span><span class="sxs-lookup"><span data-stu-id="08604-111">It is called after ADSI determines the extension to service the dispatch.</span></span> <span data-ttu-id="08604-112">L’extension peut utiliser les informations de type pour obtenir le DISPID, autrement dit, à l’aide de la fonction [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="08604-112">The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.</span></span>

<span data-ttu-id="08604-113">ADSI appelle normalement la méthode [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) après avoir appelé la fonction [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="08604-113">ADSI normally calls the [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) method after calling the [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) function.</span></span> <span data-ttu-id="08604-114">L’extension doit appeler la méthode réelle qu’elle implémente.</span><span class="sxs-lookup"><span data-stu-id="08604-114">The extension should call the actual method that it implements.</span></span> <span data-ttu-id="08604-115">L’extension peut également utiliser les informations de type et appeler la fonction [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) .</span><span class="sxs-lookup"><span data-stu-id="08604-115">Alternatively, the extension can use type information and call the [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) function.</span></span>

<span data-ttu-id="08604-116">Tous les paramètres ont la même signification que les paramètres de la méthode [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) standard.</span><span class="sxs-lookup"><span data-stu-id="08604-116">All parameters have the same meaning as the parameters in the standard [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) method.</span></span>

 

 