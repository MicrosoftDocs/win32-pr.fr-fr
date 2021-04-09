---
description: En général, cette méthode est appelée à partir de DllUnregisterServer. L’exemple de code suivant peut être placé dans le code de DllUnregisterServer.
ms.assetid: a5567c3b-edc0-427a-9751-ba221611e92c
title: Annuler l’inscription d’un terminal enfichable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb53f27dc7b468fd4288fd407faee00ab1ece8ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864982"
---
# <a name="unregister-a-pluggable-terminal"></a><span data-ttu-id="64509-104">Annuler l’inscription d’un terminal enfichable</span><span class="sxs-lookup"><span data-stu-id="64509-104">Unregister a Pluggable Terminal</span></span>

<span data-ttu-id="64509-105">En général, cette méthode est appelée à partir de **DllUnregisterServer**.</span><span class="sxs-lookup"><span data-stu-id="64509-105">In general, this method will be called from **DllUnregisterServer**.</span></span> <span data-ttu-id="64509-106">L’exemple de code suivant peut être placé dans le code de **DllUnregisterServer**.</span><span class="sxs-lookup"><span data-stu-id="64509-106">The following sample code can be put into the code for **DllUnregisterServer**.</span></span>

``` syntax
ITPluggableTerminalClassRegistration* pTerminal;

BSTR bstrTerminalSuperclass = SysAllocString(L"{F7438990-D6EB-11d0-82A6-00AA00B5CA1B}");

// If (NULL == bstrTermSuperclass) process the error here.

BSTR bstrTerminalClass = SysAllocString(L"{AED6483E-3304-11d2-86F1-006008B0E5D2}");

// If (NULL == bstrTerminalClass) process the error here.

HRESULT hr;
hr = CoCreateInstance( 
    CLSID_PluggableTerminalRegistration,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_ITPluggableTerminalClassRegistration,
    (void**)&pTerminal);

hr = pTerminal->put_TerminalClass( bstrTerminalClass );
// If (hr != S_OK) process the error here. 
hr = pTerminal->Delete( bstrTerminalSuperclass );
// If (hr != S_OK) process the error here. 

// Release the memory created by SysAllocString().
SysFreeString(bstrTerminalClass);
SysFreeString(bstrTerminalSuperclass);
```

 

 



