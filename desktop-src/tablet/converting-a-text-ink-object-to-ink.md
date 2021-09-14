---
description: Implémentation de la conversion d’un objet texte Ink (tInk) en Ink.
ms.assetid: 9365da4c-3667-49f0-838f-f099d28dab44
title: Conversion d’un objet Ink Text en Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8c7fe4a7847834fffda2df9c4ab94293756cee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226633"
---
# <a name="converting-a-text-ink-object-to-ink"></a>Conversion d’un objet Ink Text en Ink

Implémentation de la conversion d’un objet texte Ink (tInk) en Ink.

## <a name="to-convert-from-a-text-ink-object-to-ink"></a>Pour convertir un objet Ink Text en Ink

1.  Utilisez l’interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) pour écrire le contenu de l’objet Ink text dans un flux. L’objet Ink Text utilise le format sérialisé en encre pour écrire sur le vapeur.
2.  Lit le contenu du flux dans un tableau d’octets.
3.  Utilisez la méthode [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) de l’objet [**InkDisp**](inkdisp-class.md) pour charger le contenu du flux dans l’objet **InkDisp** .

## <a name="text-ink-object-to-ink-object-example"></a>Exemple d’objet Ink Text vers un objet Ink

Le fragment de code suivant convertit un objet Ink Text en Ink.

Tout d’abord, le code obtient un objet Ink Text.


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



Ensuite, le code crée un pointeur pour le flux qui contient le contenu de l’objet Ink Text.


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



Ensuite, le code obtient l’interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) à partir de l’objet Ink Text.


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



Ensuite, le code utilise l’interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) pour enregistrer le contenu de l’objet Ink text dans le flux.


```C++
if( SUCCEEDED(hr) && pIPersistStream )
{
    // Create the stream 
    if( SUCCEEDED(hr=CreateStreamOnHGlobal(NULL, TRUE, &spStream)) && spStream )
    {
        // Save the TextInk through IPersistStream Interface to the IStream
        hr = spIPersistStream->Save(spStream, FALSE);
    }
}
```



Ensuite, le code crée un objet [**InkCollector**](inkcollector-class.md) , crée un objet [**InkDisp**](inkdisp-class.md) pour le **InkCollector**, joint le **InkCollector** à la fenêtre d’application et active la collecte d’encres sur le **InkCollector**.


```C++
// Now create an InkCollector object along with InkDisp Object
if( SUCCEEDED(hr) && spStream)
{
    CComPtr<IInkCollector *> spIInkCollector;
    CComPtr<IInkDisp *> spIInkDisp = NULL;

    // Create the InkCollector object.
    hr = CoCreateInstance(CLSID_InkCollector, 
        NULL, CLSCTX_INPROC_SERVER, 
        IID_IInkCollector, 
        (void **) &spIInkCollector);
    if (FAILED(hr)) 
        return -1;

    // Get a pointer to the Ink object
    hr = spIInkCollector->get_Ink(&spIInkDisp);
    if (FAILED(hr)) 
        return -1;

    // Tell InkCollector the window to collect ink in
    hr = spIInkCollector->put_hWnd((long)hwnd);
    if (FAILED(hr)) 
        return -1;

    // Enable ink input in the window
    hr = spIInkCollector->put_Enabled(VARIANT_TRUE);
    if (FAILED(hr)) 
        return -1;
```



Ensuite, le code récupère la taille du flux et crée un tableau sécurisé pour contenir le contenu du flux.


```C++
    // Now create a variant data type based on the IStream data
    const LARGE_INTEGER li0 = {0, 0};
    ULARGE_INTEGER uli = {0,0};

    // Find the size of the stream
    hr = spStream->Seek(li0, STREAM_SEEK_END, &uli);
    ASSERT(0 == uli.HighPart);
    DWORD dwSize = uli.LowPart;

    // Set uli to point to the beginning of the stream.
    hr=spStream->Seek(li0, STREAM_SEEK_SET, &uli);
    ASSERT(SUCCEEDED(hr));

    // Create a safe array to hold the stream contents
    if( SUCCEEDED(hr) )
    {
        VARIANT vtData;
        VariantInit(&vtData);
        vtData.vt = VT_ARRAY | VT_UI1;

        vtData.parray = ::SafeArrayCreateVector(VT_UI1, 0, dwSize);
        if (vtData.parray)
        {
```



Enfin, le code accède au tableau safe et utilise la méthode [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) de l’objet [**InkDisp**](inkdisp-class.md) pour charger l’encre à partir du tableau.


```C++
            DWORD dwRead = 0;
            LPBYTE pbData = NULL; 

            if (SUCCEEDED(::SafeArrayAccessData(vtData.parray, (void**)&pbData)))
            {
                // Read the data from the stream to the varian data and load that into an InkDisp object
                if (TRUE == spStream->Read(pbData, uli.LowPart, &dwRead)
                    && SUCCEEDED(spIInkDisp->Load(vtData)))
                {
                    hr = S_OK;
                }
                ::SafeArrayUnaccessData(vtData.parray);
            }
            ::SafeArrayDestroy(vtData.parray);
        }
    }
}
```



 

 
