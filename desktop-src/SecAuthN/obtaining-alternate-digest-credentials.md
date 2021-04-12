---
description: Pour obtenir des informations d’identification autres que celles associées à la session active Logon, renseignez une \_ \_ structure d’identité de l’authentification Winnt avec des \_ informations pour le principal de sécurité de substitution.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Obtention d’autres informations d’identification de Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204155"
---
# <a name="obtaining-alternate-digest-credentials"></a><span data-ttu-id="21334-103">Obtention d’autres informations d’identification de Digest</span><span class="sxs-lookup"><span data-stu-id="21334-103">Obtaining Alternate Digest Credentials</span></span>

<span data-ttu-id="21334-104">Pour obtenir des informations [*d’identification*](../secgloss/c-gly.md) autres que celles associées à la [*session*](../secgloss/s-gly.md)active Logon, renseignez une structure d’identité de l' [**\_ \_ authentification \_ winnt**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) avec des informations pour le [*principal de sécurité*](../secgloss/s-gly.md)de substitution.</span><span class="sxs-lookup"><span data-stu-id="21334-104">To obtain [*credentials*](../secgloss/c-gly.md) other than those associated with the current logon [*session*](../secgloss/s-gly.md), populate a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure with information for the alternate [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="21334-105">Transmettez la structure à la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) à l’aide du paramètre *pAuthData* .</span><span class="sxs-lookup"><span data-stu-id="21334-105">Pass the structure to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function using the *pAuthData* parameter.</span></span>

<span data-ttu-id="21334-106">Le tableau suivant décrit les membres de la structure de l' [**\_ \_ \_ identité d’authentification Winnt**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la sec.</span><span class="sxs-lookup"><span data-stu-id="21334-106">The following table describes the members of the [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure.</span></span>



| <span data-ttu-id="21334-107">Membre</span><span class="sxs-lookup"><span data-stu-id="21334-107">Member</span></span>             | <span data-ttu-id="21334-108">Description</span><span class="sxs-lookup"><span data-stu-id="21334-108">Description</span></span>                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21334-109">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="21334-109">**User**</span></span>           | <span data-ttu-id="21334-110">Chaîne terminée par le caractère null qui contient le nom du principal de sécurité dont les informations d’identification seront utilisées pour établir un contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="21334-110">Null-terminated string containing the name of the security principal whose credentials will be used to establish a security context.</span></span> |
| <span data-ttu-id="21334-111">**UserLength**</span><span class="sxs-lookup"><span data-stu-id="21334-111">**UserLength**</span></span>     | <span data-ttu-id="21334-112">Longueur du membre **utilisateur** , en caractères.</span><span class="sxs-lookup"><span data-stu-id="21334-112">The length of the **User** member, in characters.</span></span> <span data-ttu-id="21334-113">Omettez la valeur null de fin.</span><span class="sxs-lookup"><span data-stu-id="21334-113">Omit the terminating null.</span></span>                                                         |
| <span data-ttu-id="21334-114">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="21334-114">**Domain**</span></span>         | <span data-ttu-id="21334-115">Chaîne terminée par le caractère null qui identifie le domaine contenant le compte du principal de sécurité.</span><span class="sxs-lookup"><span data-stu-id="21334-115">Null-terminated string that identifies the domain containing the account of the security principal.</span></span>                                  |
| <span data-ttu-id="21334-116">**DomainLength**</span><span class="sxs-lookup"><span data-stu-id="21334-116">**DomainLength**</span></span>   | <span data-ttu-id="21334-117">Longueur du membre de **domaine** , en caractères.</span><span class="sxs-lookup"><span data-stu-id="21334-117">The length of the **Domain** member, in characters.</span></span> <span data-ttu-id="21334-118">Omettez la valeur null de fin.</span><span class="sxs-lookup"><span data-stu-id="21334-118">Omit the terminating null.</span></span>                                                       |
| <span data-ttu-id="21334-119">**Mot de passe**</span><span class="sxs-lookup"><span data-stu-id="21334-119">**Password**</span></span>       | <span data-ttu-id="21334-120">Chaîne terminée par le caractère null qui contient le mot de passe du principal de sécurité.</span><span class="sxs-lookup"><span data-stu-id="21334-120">Null-terminated string containing the password of the security principal.</span></span>                                                            |
| <span data-ttu-id="21334-121">**PasswordLength**</span><span class="sxs-lookup"><span data-stu-id="21334-121">**PasswordLength**</span></span> | <span data-ttu-id="21334-122">Longueur du membre de **mot de passe** , en caractères.</span><span class="sxs-lookup"><span data-stu-id="21334-122">The length of the **Password** member, in characters.</span></span> <span data-ttu-id="21334-123">Omettez la valeur null de fin.</span><span class="sxs-lookup"><span data-stu-id="21334-123">Omit the terminating null.</span></span>                                                     |
| <span data-ttu-id="21334-124">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="21334-124">**Flags**</span></span>          | <span data-ttu-id="21334-125">Indique si les membres de la chaîne sont au format ANSI ou [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="21334-125">Indicates whether the string members are in ANSI or [*Unicode*](../secgloss/u-gly.md) format.</span></span>  |



 

<span data-ttu-id="21334-126">Le tableau suivant répertorie les valeurs valides pour le membre **Flags** de la structure.</span><span class="sxs-lookup"><span data-stu-id="21334-126">The following table lists the valid values for the **Flags** member of the structure.</span></span>



| <span data-ttu-id="21334-127">Constante</span><span class="sxs-lookup"><span data-stu-id="21334-127">Constant</span></span>                            | <span data-ttu-id="21334-128">Description</span><span class="sxs-lookup"><span data-stu-id="21334-128">Description</span></span>                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21334-129">SEC \_ identité d’authentification Winnt \_ \_ \_ ANSI</span><span class="sxs-lookup"><span data-stu-id="21334-129">SEC\_WINNT\_AUTH\_IDENTITY\_ANSI</span></span>    | <span data-ttu-id="21334-130">Les chaînes de cette structure sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="21334-130">Strings in this structure are in ANSI format.</span></span>                                                                    |
| <span data-ttu-id="21334-131">SEC \_ identité d’authentification Winnt \_ \_ \_ Unicode</span><span class="sxs-lookup"><span data-stu-id="21334-131">SEC\_WINNT\_AUTH\_IDENTITY\_UNICODE</span></span> | <span data-ttu-id="21334-132">Les chaînes de cette structure sont au format [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="21334-132">Strings in this structure are in [*Unicode*](../secgloss/u-gly.md) format.</span></span> |



 

<span data-ttu-id="21334-133">La structure et les constantes sont déclarées dans le fichier d’en-tête rpcdce. h distribué avec le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="21334-133">The structure and constants are declared in the Rpcdce.h header file distributed with the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="21334-134">L’exemple suivant illustre un appel côté client pour obtenir des informations d’identification de résumé pour un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="21334-134">The following example demonstrates a client-side call to obtain Digest credentials for a specific user account.</span></span>


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



<span data-ttu-id="21334-135">La fonction **\_ tcslen** retourne la longueur de chaîne en caractères, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="21334-135">The **\_tcslen** function returns the string length in characters, not including the terminating null character.</span></span>

<span data-ttu-id="21334-136">Si votre application peut utiliser les informations d’identification établies lors de l’ouverture de session, consultez [obtention des informations d’identification du condensé par défaut](obtaining-default-digest-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="21334-136">If your application can use the credentials established at logon, see [Obtaining Default Digest Credentials](obtaining-default-digest-credentials.md).</span></span>

 

 
