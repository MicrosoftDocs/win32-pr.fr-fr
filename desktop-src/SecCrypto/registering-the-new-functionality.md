---
description: La prise en charge de l’inscription de la nouvelle fonctionnalité dans un registre système doit être fournie dans la nouvelle DLL avec la nouvelle fonction.
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: Inscription des nouvelles fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470541ed9b832ad5eaa914c1a35805dbd861a843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536846"
---
# <a name="registering-the-new-functionality"></a><span data-ttu-id="12f9d-103">Inscription des nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="12f9d-103">Registering the New Functionality</span></span>

<span data-ttu-id="12f9d-104">La prise en charge de l’inscription de la nouvelle fonctionnalité dans un registre système doit être fournie dans la nouvelle DLL avec la nouvelle fonction.</span><span class="sxs-lookup"><span data-stu-id="12f9d-104">Support for registering the new functionality in a system registry must be provided in the new DLL along with the new function.</span></span> <span data-ttu-id="12f9d-105">Les [fonctions de prise en charge d’OID](cryptography-functions.md) offrent une assistance pour cette inscription.</span><span class="sxs-lookup"><span data-stu-id="12f9d-105">[OID Support Functions](cryptography-functions.md) provide assistance with this registration.</span></span> <span data-ttu-id="12f9d-106">Regsvr32.exe inscrit de nouvelles fonctions.</span><span class="sxs-lookup"><span data-stu-id="12f9d-106">Regsvr32.exe registers new functions.</span></span> <span data-ttu-id="12f9d-107">Cet outil est inclus dans Windows.</span><span class="sxs-lookup"><span data-stu-id="12f9d-107">This tool is included with Windows.</span></span>

<span data-ttu-id="12f9d-108">La nouvelle DLL doit fournir des points d’entrée [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) pour une utilisation par Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="12f9d-108">The new DLL must provide [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) entry points for use by Regsvr32.exe.</span></span> <span data-ttu-id="12f9d-109">Les fonctions [*CryptoAPI*](../secgloss/c-gly.md) , telles que [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) ou [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), peuvent être utilisées dans ces points d’entrée, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="12f9d-109">[*CryptoAPI*](../secgloss/c-gly.md) functions, such as [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) or [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), can be used within these entry points, as shown in the following example.</span></span>


```C++
//  The DllRegisterServer Entry Point
STDAPI DllRegisterServer(void)
{
    if(!CryptRegisterOIDFunction(
         X509_ASN_ENCODING,                  // Encoding type
         CRYPT_OID_ENCODE_OBJECT_FUNC,       // Function name
         szOID_NEW_CERTIFICATE_TYPE,         // OID
         L"NewCert.dll",                     // Dll name
         L"NewCertificateTypeEncodeObject"   // Override function
         ))                                  //   name
       {
         return E_FAIL;
       }
    else
       {
         return S_OK;
       }
}

// The DllUnregisterServer Entry Point
STDAPI DllUnregisterServer(void)
{
    HRESULT     hr = S_OK;

    if(!CryptUnregisterOIDFunction(
          X509_ASN_ENCODING,             // Encoding type
          CRYPT_OID_ENCODE_OBJECT_FUNC,  // Function name
          szOID_NEW_CERTIFICATE_TYPE     // OID
          ))
    {
       if(ERROR_FILE_NOT_FOUND != GetLastError())
               hr = E_FAIL;
    }
    return hr;
}
```



<span data-ttu-id="12f9d-110">Cet exemple doit être compilé et lié dans la nouvelle DLL.</span><span class="sxs-lookup"><span data-stu-id="12f9d-110">This example must be compiled and linked into the new DLL.</span></span> <span data-ttu-id="12f9d-111">Ces deux points d’entrée, ainsi que le point d’entrée de la fonction, doivent être exportés.</span><span class="sxs-lookup"><span data-stu-id="12f9d-111">These two entry points, along with the function entry point, must be exported.</span></span>

<span data-ttu-id="12f9d-112">Pour installer la nouvelle fonctionnalité sur un ordinateur, exécutez Regsvr32.exe à partir d’une invite de commandes, en spécifiant le nom et le chemin d’accès de la nouvelle DLL.</span><span class="sxs-lookup"><span data-stu-id="12f9d-112">To install the new functionality on a computer, run Regsvr32.exe from a command prompt, specifying the name and path of the new DLL.</span></span> <span data-ttu-id="12f9d-113">Regsvr32.exe accède à la fonction [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) via le point d’entrée de la fonction [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) et inscrit la nouvelle fonction et la nouvelle dll.</span><span class="sxs-lookup"><span data-stu-id="12f9d-113">Regsvr32.exe accesses the [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) function through the [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) function entry point and registers the new function and DLL.</span></span>

 

 
