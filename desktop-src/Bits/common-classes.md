---
title: Exemples de classes communes
description: Vous pouvez utiliser les exemples de code de cette rubrique comme point de départ pour de nombreuses applications Service de transfert intelligent en arrière-plan (BITS) qui effectuent l’initialisation COM, ont besoin de la gestion des erreurs et reçoivent des notifications de rappel.
ms.assetid: 8fe722a3-fbab-4843-b298-1ea11f54d7a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864fe4aa8d7af5bb6a248364b0e2c636e1c250a6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734845"
---
# <a name="example-common-classes"></a>Exemple : classes communes

Vous pouvez utiliser les exemples de code de cette rubrique comme point de départ pour de nombreuses applications Service de transfert intelligent en arrière-plan (BITS) qui effectuent l’initialisation COM, ont besoin de la gestion des erreurs et reçoivent des notifications de rappel.


L’exemple de code suivant définit une classe d’exception pour gérer les erreurs.


```C++
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};
```



La classe MyException est une classe d’exception générique qui accepte un code HRESULT et une chaîne d’erreur.


L’exemple de code suivant définit une classe d’assistance pour l’acquisition des ressources pour la fonction [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .


```C++
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};
```



La classe CCoInitializer gère l’allocation et la désallocation des ressources pour l’initialisation COM. Cette classe permet d’appeler le destructeur lorsque la classe est hors de portée. Cette classe élimine la nécessité d’appeler la méthode [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) après chaque bloc d’exception.


L’exemple de code suivant est la déclaration de l’interface de rappel CNotifyInterface.


```C++
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor
    CNotifyInterface() {m_lRefCount = 1;};

//Destructor
    ~CNotifyInterface() {};

    //IUnknown methods
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);

private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```



La classe CNotifyInterface dérivée de l’interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) . La classe CNotifyInterface implémente l’interface IUnknown. Pour plus d’informations, consultez [IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown).

CNotifyInterface utilise les méthodes suivantes pour recevoir une notification indiquant qu’un travail est terminé, a été modifié ou est dans un état d’erreur : [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred), [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)et [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror). Toutes ces méthodes prennent un objet de tâche [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) .

Cet exemple utilise [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer des ressources mémoire.


L’exemple de code suivant est l’implémentation de l’interface de rappel [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


```C++
HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed. 

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }
    
    // Clean up
    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```




Le fichier d’en-tête suivant est utilisé pour les classes de code courantes. Ces classes sont utilisées dans les exemples de code précédents.


```C++
// commoncode.h
#pragma once

//
// Exception class used for error handling
//
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};

// CoInitialize helper class
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};

//
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor, Destructor
    CNotifyInterface() {m_lRefCount = 1;};
    ~CNotifyInterface() {};

    //IUnknown
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback2 methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);
private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```




L’exemple de code suivant est l’implémentation des classes de code communes.


```C++
//commoncode.cpp

#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"

HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed.

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }

    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)
</dt> <dt>

[**Méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)
</dt> </dl>

 

 