---
description: La prise en charge de l’inscription de la nouvelle fonctionnalité dans un registre système doit être fournie dans la nouvelle DLL avec la nouvelle fonction.
ms.assetid: 7a6af325-4891-40db-8d33-c9782bd438e5
title: Inscription des nouvelles fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5d56153199542c11f00a3ec23d90d35a682c5fe93f91d2978dcd4f72628219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900594"
---
# <a name="registering-the-new-functionality"></a>Inscription des nouvelles fonctionnalités

La prise en charge de l’inscription de la nouvelle fonctionnalité dans un registre système doit être fournie dans la nouvelle DLL avec la nouvelle fonction. Les [fonctions de prise en charge d’OID](cryptography-functions.md) offrent une assistance pour cette inscription. Regsvr32.exe inscrit de nouvelles fonctions. Cet outil est inclus dans Windows.

La nouvelle DLL doit fournir des points d’entrée [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) pour une utilisation par Regsvr32.exe. Les fonctions [*CryptoAPI*](../secgloss/c-gly.md) , telles que [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) ou [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction), peuvent être utilisées dans ces points d’entrée, comme illustré dans l’exemple suivant.


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



Cet exemple doit être compilé et lié dans la nouvelle DLL. Ces deux points d’entrée, ainsi que le point d’entrée de la fonction, doivent être exportés.

Pour installer la nouvelle fonctionnalité sur un ordinateur, exécutez Regsvr32.exe à partir d’une invite de commandes, en spécifiant le nom et le chemin d’accès de la nouvelle DLL. Regsvr32.exe accède à la fonction [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction) via le point d’entrée de la fonction [**DllRegisterServer**](/previous-versions/windows/desktop/legacy/aa369359(v=vs.85)) et inscrit la nouvelle fonction et la nouvelle dll.

 

 
