---
description: Vous pouvez utiliser les instructions suivantes pour configurer les valeurs de regroupement d’applications COM+ pour votre application COM+.
ms.assetid: faba5cb7-745e-4fdf-a3e0-62132da4a843
title: Configuration des valeurs de regroupement d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d3407cd644b68cfc3ef279a9e67603aa1dc2db85302b22dbf0c6ae7219fd3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128971"
---
# <a name="configuring-com-application-pooling-values"></a>Configuration des valeurs de regroupement d’applications COM+

Vous pouvez utiliser les instructions suivantes pour configurer les valeurs de regroupement d’applications COM+ pour votre application COM+.

> [!Note]  
> Les applications de bibliothèque disposent des propriétés de recyclage et de regroupement de leur processus hôte.

 

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Pour configurer le regroupement d’applications COM+ pour une application COM+, procédez comme suit :

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, cliquez avec le bouton droit sur l’application COM+ que vous souhaitez regrouper, puis cliquez sur **Propriétés**.

2.  Sous l’onglet **regroupement & recyclage** , sous mise en **pool d’applications**, entrez une valeur pour taille de **pool**, selon le nombre d’instances de votre application que vous souhaitez exécuter.

3.  Cliquez sur **OK**.

## <a name="visual-basic"></a>Visual Basic

la fonction suivante dans Visual Basic montre comment vous pouvez définir la valeur de regroupement d’applications com+ (représentée par sa propriété ConcurrentApps) pour n’importe quelle application serveur com+ que vous choisissez. pour l’utiliser à partir de Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+.


```VB
Function SetMyApplicationPooling( _
  strApplicationName As String, _
  lngPoolValue As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationPooling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate 
    For Each objApplication in objAppCollection
        If objApplication.Name = strApplicationName Then
            objApplication.Value("ConcurrentApps") = lngPoolValue
            MsgBox strApplicationName & _
              " pooling value set to " & lngPoolValue
            Exit For
        End If
    Next
    objAppCollection.SaveChanges

    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationPooling = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



Pour utiliser la fonction, fournissez une valeur de chaîne pour le nom de l’application serveur COM+ et une valeur entière pour le paramètre de regroupement d’applications souhaité. le code Visual Basic suivant montre comment définir la valeur de regroupement d’applications sur 15 pour l’application nommée « MyApplication » :


```VB
Sub Main()
    If Not SetMyApplicationPooling("MyApplication", 15) Then
        MsgBox "SetMyApplicationPooling failed."
    End If
End Sub

```



## <a name="cc"></a>C/C++

La fonction suivante en C++ montre comment vous pouvez définir la valeur de regroupement d’applications COM+ (représentée par sa propriété ConcurrentApps) pour n’importe quelle application serveur COM+ que vous choisissez. La méthode ErrorDescription est décrite dans [interprétation des codes d’erreur](interpreting-error-codes.md).


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\Com\ComAdmin.dll"
#include "ComAdmin.h"
#include "StrSafe.h"  // For the StringCchLengthW function

BOOL SetMyApplicationPooling (OLECHAR* szMyApp, LONG lPool) {
    IUnknown * pUnknown = NULL;
    ICOMAdminCatalog * pCatalog = NULL;
    ICatalogCollection * pAppColl = NULL;
    ICatalogObject * pApplication = NULL;
    HRESULT hr = S_OK;
    BSTR bstrMyApp = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp
    LCID lLan = 1024;// Use the default language for comparing strings.

try {
    // Test the input pool value.
    if ((lPool < 1) || (lPool > 1048576)) throw(E_INVALIDARG);
    
    // Test the input szMyApp to make sure it's OK to use.
    hr = StringCchLengthW(szMyApp, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert szMyApp to a BSTR.
    bstrMyApp = SysAllocString(szMyApp);

    // Create a COMAdminCatalog object and get its IUnknown.
    hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);

    // Get the ICOMAdminCatalog interface.
   hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) throw(hr);

    // Get an interface to the Applications collection.
    hr = pCatalog->GetCollection(L"Applications", (IDispatch**)&pAppColl);
    if (FAILED (hr)) throw(hr);

    // Populate all of the Applications collection.
    hr = pAppColl->Populate();
    if (FAILED (hr)) throw(hr);

    // Get the number of applications in the collection.
    LONG lCount = -1;
    hr = pAppColl->get_Count(&lCount);
    if (FAILED (hr)) throw(hr);

    // Iterate through each application in the collection.
    VARIANT varName;
    VariantInit(&varName);
    for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
        hr = pAppColl->get_Item(lIdx, (IDispatch**)&pApplication);
        if (FAILED (hr)) throw(hr);

        // Get the Name value of each application.
       hr = pApplication->get_Name(&varName);
        if (FAILED (hr)) throw(hr);

        // Compare the application name to bstrMyApp.
        hr = VarBstrCmp(varName.bstrVal, bstrMyApp, lLan, NULL);
        if (FAILED (hr)) throw(hr);
        if (VARCMP_EQ == hr) {  // The strings are equal.
            // Set the new pooling value.
            VARIANT varPool;
            VariantInit(&varPool);
            varPool.vt = VT_I4;  // Tell the VARIANT it's holding a LONG.
            varPool.lVal = lPool;
            hr = pApplication->put_Value(L"ConcurrentApps", varPool);
            if (FAILED (hr)) throw(hr);
            printf("%S pooling value set to %ld.\n", bstrMyApp, lPool);
            break;
        }
    }
    LONG lNum;
    hr = pAppColl->SaveChanges(&lNum);
    if (FAILED (hr)) throw(hr);

    // Clean up.
    SysFreeString(bstrMyApp);
    pUnknown->Release();
    pUnknown = NULL;
    pApplication->Release();
    pApplication = NULL;
    pAppColl->Release();
    pAppColl = NULL;
    pCatalog->Release();
    pCatalog = NULL;
    return (TRUE);
}  // Try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrMyApp);
    if (NULL != pUnknown) pUnknown>Release();
    pUnknown = NULL;
    if (NULL != pApplication) pApplication->Release();
    pApplication = NULL;
    if (NULL != pAppColl) pAppColl->Release();
    pAppColl = NULL;
    if (NULL != pCatalog) pCatalog->Release();
    pCatalog = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}
}  // SetMyApplicationPooling

```



Pour utiliser la fonction, fournissez une valeur de chaîne pour le nom de l’application serveur COM+ et une valeur entière pour le paramètre de regroupement d’applications souhaité. Le code C++ suivant montre comment définir la valeur de regroupement d’applications sur 15 pour l’application nommée « MyApplication » :

``` syntax
#define _WIN32_DCOM  // To use CoInitializeEx()
void main() {
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! SetMyApplicationPooling (L"MyApplication", 15))
        printf("SetMyApplicationPooling failed.\n");
    CoUninitialize();
}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de regroupement d’applications COM+](com--application-pooling-concepts.md)
</dt> </dl>

 

 



