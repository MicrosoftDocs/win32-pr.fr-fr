---
description: Le mot de passe d’ouverture de session automatique doit être protégé à l’aide de la fonction LsaStorePrivateData.
ms.assetid: 7bd4d725-de17-4801-bd06-8d47a777409d
title: Protection du mot de passe de connexion automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25508af4de64554e664426db3e786a1eca34579b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952723"
---
# <a name="protecting-the-automatic-logon-password"></a><span data-ttu-id="3ff86-103">Protection du mot de passe de connexion automatique</span><span class="sxs-lookup"><span data-stu-id="3ff86-103">Protecting the Automatic Logon Password</span></span>

<span data-ttu-id="3ff86-104">Le mot de passe d’ouverture de session automatique doit être protégé à l’aide de la fonction [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) .</span><span class="sxs-lookup"><span data-stu-id="3ff86-104">The automatic logon password should be protected by using the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function.</span></span>

<span data-ttu-id="3ff86-105">L’exemple suivant montre comment protéger le mot de passe d’ouverture de session automatique.</span><span class="sxs-lookup"><span data-stu-id="3ff86-105">The following example shows how to protect the automatic logon password.</span></span> <span data-ttu-id="3ff86-106">L’exemple récupère un handle vers l’objet de [**stratégie**](../secmgmt/policy-object.md) en appelant la fonction [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) .</span><span class="sxs-lookup"><span data-stu-id="3ff86-106">The example retrieves a handle to the [**Policy**](../secmgmt/policy-object.md) object by calling the [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) function.</span></span> <span data-ttu-id="3ff86-107">Pour plus d’informations sur l’objet de **stratégie** et les handles d’objet de **stratégie** , consultez objet de **stratégie** et [ouverture d’un descripteur d’objet de stratégie](../secmgmt/opening-a-policy-object-handle.md), respectivement.</span><span class="sxs-lookup"><span data-stu-id="3ff86-107">For more information about the **Policy** object and **Policy** object handles, see **Policy** object and [Opening a Policy Object Handle](../secmgmt/opening-a-policy-object-handle.md), respectively.</span></span> <span data-ttu-id="3ff86-108">L’exemple définit ensuite le mot de passe protégé en appelant la fonction [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) .</span><span class="sxs-lookup"><span data-stu-id="3ff86-108">The example then sets the protected password by calling the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function.</span></span> <span data-ttu-id="3ff86-109">Notez que si l’appelant transmet **null** pour la valeur de mot de passe protégée, le code efface le mot de passe protégé existant.</span><span class="sxs-lookup"><span data-stu-id="3ff86-109">Note that if the caller passes in **NULL** for the protected password value, then the code clears the existing protected password.</span></span> <span data-ttu-id="3ff86-110">Avant de quitter, le code ferme le descripteur de l’objet de **stratégie** .</span><span class="sxs-lookup"><span data-stu-id="3ff86-110">Before exiting, the code closes the handle to the **Policy** object.</span></span>


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



<span data-ttu-id="3ff86-111">Notez que si Winlogon ne trouve pas de mot de passe stocké par la fonction [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) , il utilise la valeur **DefaultPassword** de la clé Winlogon (le cas échéant) pour le mot de passe d’ouverture de session automatique.</span><span class="sxs-lookup"><span data-stu-id="3ff86-111">Note that if Winlogon cannot find a password stored by the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function, it will use the **DefaultPassword** value of the Winlogon key (if it exists) for the automatic logon password.</span></span>

<span data-ttu-id="3ff86-112">Pour plus d’informations sur la connexion automatique et la clé de Registre Winlogon, consultez [MSGina.dll fonctionnalités](msgina-dll-features.md).</span><span class="sxs-lookup"><span data-stu-id="3ff86-112">For more information about automatic logon and the Winlogon registry key, see [MSGina.dll Features](msgina-dll-features.md).</span></span>

<span data-ttu-id="3ff86-113">Pour plus d’informations sur la protection des mots de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="3ff86-113">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

 

 
