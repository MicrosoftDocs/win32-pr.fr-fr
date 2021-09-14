---
description: Le mot de passe d’ouverture de session automatique doit être protégé à l’aide de la fonction LsaStorePrivateData.
ms.assetid: 7bd4d725-de17-4801-bd06-8d47a777409d
title: Protection du mot de passe de connexion automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25508af4de64554e664426db3e786a1eca34579b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324794"
---
# <a name="protecting-the-automatic-logon-password"></a>Protection du mot de passe de connexion automatique

Le mot de passe d’ouverture de session automatique doit être protégé à l’aide de la fonction [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) .

L’exemple suivant montre comment protéger le mot de passe d’ouverture de session automatique. L’exemple récupère un handle vers l’objet de [**stratégie**](../secmgmt/policy-object.md) en appelant la fonction [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) . Pour plus d’informations sur l’objet de **stratégie** et les handles d’objet de **stratégie** , consultez objet de **stratégie** et [ouverture d’un descripteur d’objet de stratégie](../secmgmt/opening-a-policy-object-handle.md), respectivement. L’exemple définit ensuite le mot de passe protégé en appelant la fonction [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) . Notez que si l’appelant transmet **null** pour la valeur de mot de passe protégée, le code efface le mot de passe protégé existant. Avant de quitter, le code ferme le descripteur de l’objet de **stratégie** .


```C++
#include <windows.h>
#include <stdio.h>

DWORD UpdateDefaultPassword(WCHAR * pwszSecret)
{

    LSA_OBJECT_ATTRIBUTES ObjectAttributes;
    LSA_HANDLE LsaPolicyHandle = NULL;

    LSA_UNICODE_STRING lusSecretName;
    LSA_UNICODE_STRING lusSecretData;
    USHORT SecretNameLength;
    USHORT SecretDataLength;

    NTSTATUS ntsResult = STATUS_SUCCESS;
    DWORD dwRetCode = ERROR_SUCCESS;

    //  Object attributes are reserved, so initialize to zeros.
    ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

    //  Get a handle to the Policy object.
    ntsResult = LsaOpenPolicy(
        NULL,    // local machine
        &ObjectAttributes, 
        POLICY_CREATE_SECRET,
        &LsaPolicyHandle);

    if( STATUS_SUCCESS != ntsResult )
    {
        //  An error occurred. Display it as a win32 error code.
        dwRetCode = LsaNtStatusToWinError(ntsResult);
        wprintf(L"Failed call to LsaOpenPolicy %lu\n", dwRetCode);
        return dwRetCode;
    } 

    //  Initialize an LSA_UNICODE_STRING for the name of the
    //  private data ("DefaultPassword").
    SecretNameLength = (USHORT)wcslen(L"DefaultPassword");
    lusSecretName.Buffer = L"DefaultPassword";
    lusSecretName.Length = SecretNameLength * sizeof(WCHAR);
    lusSecretName.MaximumLength =
        (SecretNameLength+1) * sizeof(WCHAR);

    //  If the pwszSecret parameter is NULL, then clear the secret.
    if( NULL == pwszSecret )
    {
        wprintf(L"Clearing the secret...\n");
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            NULL);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }
    else
    {
        wprintf(L"Setting the secret...\n");
        //  Initialize an LSA_UNICODE_STRING for the value
        //  of the private data. 
        SecretDataLength = (USHORT)wcslen(pwszSecret);
        lusSecretData.Buffer = pwszSecret;
        lusSecretData.Length = SecretDataLength * sizeof(WCHAR);
        lusSecretData.MaximumLength =
            (SecretDataLength+1) * sizeof(WCHAR);
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            &lusSecretData);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }

    LsaClose(LsaPolicyHandle);

    if (dwRetCode != ERROR_SUCCESS)
        wprintf(L"Failed call to LsaStorePrivateData %lu\n",
            dwRetCode);
    
    return dwRetCode;

}

```



Notez que si Winlogon ne trouve pas de mot de passe stocké par la fonction [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) , il utilise la valeur **DefaultPassword** de la clé Winlogon (le cas échéant) pour le mot de passe d’ouverture de session automatique.

Pour plus d’informations sur la connexion automatique et la clé de Registre Winlogon, consultez [MSGina.dll fonctionnalités](msgina-dll-features.md).

Pour plus d’informations sur la protection des mots de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).

 

 
