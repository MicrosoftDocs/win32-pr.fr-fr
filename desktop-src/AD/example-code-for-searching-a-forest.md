---
title: Exemple de code pour la recherche d’une forêt
description: Cette rubrique contient un exemple de code qui recherche une forêt.
ms.assetid: 56740e95-548a-4e84-ab2e-2bb7a51b7e1e
ms.tgt_platform: multiple
keywords:
- Exemples de Active Directory Active Directory, recherche dans une forêt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92c71afeecebf96ba123e909ad408835de083b8d45cb259a7b371b8214cc5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190286"
---
# <a name="example-code-for-searching-a-forest"></a>Exemple de code pour la recherche d’une forêt

Cette rubrique contient un exemple de code qui recherche une forêt.

L’exemple de code C/C++ suivant est lié à la racine du catalogue global et énumère l’objet unique, qui est la racine de la forêt, afin qu’il puisse être utilisé pour effectuer une recherche dans l’ensemble de la forêt.


```C++
Set gc = GetObject("GC:")
For each child in gc
    Set entpr = child
Next
' Now entpr is an object that can be used
' to search the entire forest.
```



L’exemple de code C/C++ suivant contient une fonction qui retourne un pointeur [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) utilisé pour effectuer une recherche dans l’ensemble de la forêt.

La fonction effectue une liaison sans serveur à la racine du catalogue global, énumère l’élément unique, qui est la racine de la forêt et peut être utilisé pour effectuer une recherche dans l’ensemble de la forêt, appelle [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir un pointeur [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) vers l’objet et retourne ce pointeur que l’appelant doit utiliser pour effectuer une recherche dans la forêt.


```C++
HRESULT GetGC(IDirectorySearch **ppDS)
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
ULONG lFetch;
 
// Set IDirectorySearch pointer to NULL.
*ppDS = NULL;
 
// First, bind to the GC: namespace container object. 
hr = ADsOpenObject(TEXT("GC:"),
                NULL,
                NULL,
                ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                IID_IADsContainer,
                (void**)&pCont);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsOpenObject failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get an enumeration interface for the GC container to enumerate the 
// contents. The actual GC is the only child of the GC container.
hr = ADsBuildEnumerator(pCont, &pEnum);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Now enumerate. There is only one child of the GC: object.
hr = pEnum->Next(1, &var, &lFetch);
if (FAILED(hr)) {
    _tprintf(TEXT("ADsEnumerateNext failed: 0x%x\n"), hr);
    goto cleanup;
} 
 
// Get the IDirectorySearch pointer.
if (( hr == S_OK ) && ( lFetch == 1 ) )     
{    
    pDisp = V_DISPATCH(&var);
    hr = pDisp->QueryInterface( IID_IDirectorySearch, (void**)ppDS); 
}
 
cleanup:
 
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pCont)
    pCont->Release();
if (pDisp)
    (pDisp)->Release();
return hr;
}
```



 

 