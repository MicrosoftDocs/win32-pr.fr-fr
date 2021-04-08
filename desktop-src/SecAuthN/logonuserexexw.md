---
description: La fonction LogonUserExExW tente de connecter un utilisateur à l’ordinateur local.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: LogonUserExExW, fonction (Winbasep. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035017"
---
# <a name="logonuserexexw-function"></a><span data-ttu-id="7ec6d-103">LogonUserExExW fonction)</span><span class="sxs-lookup"><span data-stu-id="7ec6d-103">LogonUserExExW function</span></span>

<span data-ttu-id="7ec6d-104">La fonction **LogonUserExExW** tente de connecter un utilisateur à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-104">The **LogonUserExExW** function attempts to log a user on to the local computer.</span></span> <span data-ttu-id="7ec6d-105">L’ordinateur local est l’ordinateur à partir duquel **LogonUserExExW** a été appelé.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-105">The local computer is the computer from which **LogonUserExExW** was called.</span></span> <span data-ttu-id="7ec6d-106">Vous ne pouvez pas utiliser **LogonUserExExW** pour vous connecter à un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-106">You cannot use **LogonUserExExW** to log on to a remote computer.</span></span> <span data-ttu-id="7ec6d-107">Spécifiez l’utilisateur à l’aide d’un nom d’utilisateur et d’un domaine et [*authentifiez*](../secgloss/a-gly.md) l’utilisateur à l’aide d’un mot de passe en texte clair.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-107">Specify the user by using a user name and domain and [*authenticate*](../secgloss/a-gly.md) the user by using a plaintext password.</span></span> <span data-ttu-id="7ec6d-108">Si la fonction est réussie, elle reçoit un handle vers un jeton qui représente l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-108">If the function succeeds, it receives a handle to a token that represents the logged-on user.</span></span> <span data-ttu-id="7ec6d-109">Vous pouvez ensuite utiliser ce handle de jeton pour emprunter l’identité de l’utilisateur spécifié ou, dans la plupart des cas, pour créer un [*processus*](../secgloss/p-gly.md) qui s’exécute dans le contexte de l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-109">You can then use this token handle to impersonate the specified user or, in most cases, to create a [*process*](../secgloss/p-gly.md) that runs in the context of the specified user.</span></span>

<span data-ttu-id="7ec6d-110">Cette fonction est similaire à la fonction [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) , à ceci près qu’elle prend le paramètre supplémentaire, *pTokenGroups*, qui est un ensemble d’un ou plusieurs [*identificateurs de sécurité*](../secgloss/s-gly.md) (SID) qui sont ajoutés au jeton renvoyé à l’appelant lorsque l’ouverture de session est réussie.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-110">This function is similar to the [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) function, except that it takes the additional parameter, *pTokenGroups*, which is a set of one or more [*security identifiers*](../secgloss/s-gly.md) (SIDs) that are added to the token returned to the caller when the logon is successful.</span></span>

<span data-ttu-id="7ec6d-111">Cette fonction n’est pas déclarée dans un en-tête public et n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-111">This function is not declared in a public header and has no associated import library.</span></span> <span data-ttu-id="7ec6d-112">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-112">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec6d-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ec6d-113">Syntax</span></span>


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a><span data-ttu-id="7ec6d-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ec6d-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec6d-115">*lpszUsername* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-115">*lpszUsername* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-116">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-116">A pointer to a null-terminated string that specifies the name of the user.</span></span> <span data-ttu-id="7ec6d-117">Il s’agit du nom du compte d’utilisateur auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-117">This is the name of the user account to log on to.</span></span> <span data-ttu-id="7ec6d-118">Si vous utilisez le format UPN ( [*user principal name*](../secgloss/u-gly.md) ), le paramètre *lpszDomain* doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-118">If you use the [*user principal name*](../secgloss/u-gly.md) (UPN) format, the *lpszDomain* parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7ec6d-119">*lpszDomain* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-119">*lpszDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-120">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du domaine ou du serveur dont la base de données du compte contient le compte *lpszUsername* .</span><span class="sxs-lookup"><span data-stu-id="7ec6d-120">A pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the *lpszUsername* account.</span></span> <span data-ttu-id="7ec6d-121">Si ce paramètre a la **valeur null**, le nom d’utilisateur doit être spécifié au format UPN.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-121">If this parameter is **NULL**, the user name must be specified in UPN format.</span></span> <span data-ttu-id="7ec6d-122">Si ce paramètre est « . », la fonction valide le compte à l’aide de la base de données de comptes locale uniquement.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-122">If this parameter is ".", the function validates the account by using only the local account database.</span></span>

</dd> <dt>

<span data-ttu-id="7ec6d-123">*lpszPassword* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-123">*lpszPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-124">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le mot de passe en texte clair pour le compte d’utilisateur spécifié par *lpszUsername*.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-124">A pointer to a null-terminated string that specifies the plaintext password for the user account specified by *lpszUsername*.</span></span> <span data-ttu-id="7ec6d-125">Lorsque vous avez fini d’utiliser le mot de passe, effacez le mot de passe de la mémoire en appelant la fonction [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7ec6d-125">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="7ec6d-126">Pour plus d’informations sur la protection des mots de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="7ec6d-126">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ec6d-127">*dwLogonType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-127">*dwLogonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-128">Type d’opération d’ouverture de session à effectuer.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-128">The type of logon operation to perform.</span></span> <span data-ttu-id="7ec6d-129">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7ec6d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ec6d-130">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="7ec6d-131">Signification</span><span class="sxs-lookup"><span data-stu-id="7ec6d-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <span data-ttu-id="7ec6d-132"><dt>**LOGON32 \_ Ouverture de session \_ interactive**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-132"><dt>**LOGON32\_LOGON\_INTERACTIVE**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="7ec6d-133">Ce type d’ouverture de session est destiné aux utilisateurs qui se connectent de manière interactive à l’ordinateur, comme un utilisateur connecté par un serveur [*Terminal*](../secgloss/t-gly.md) Server, un interpréteur de commandes à distance ou un processus similaire.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-133">This logon type is intended for users who will be interactively using the computer, such as a user being logged on by a [*terminal*](../secgloss/t-gly.md) server, remote shell, or similar process.</span></span> <span data-ttu-id="7ec6d-134">Ce type d’ouverture de session a des frais supplémentaires pour la mise en cache des informations de connexion pour les opérations déconnectées. par conséquent, il est inapproprié pour certaines applications client/serveur, telles qu’un serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-134">This logon type has the additional expense of caching logon information for disconnected operations; therefore, it is inappropriate for some client/server applications, such as a mail server.</span></span><br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <span data-ttu-id="7ec6d-135"><dt>**LOGON32 \_ CONNEXION \_ réseau**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-135"><dt>**LOGON32\_LOGON\_NETWORK**</dt> <dt>3</dt></span></span> </dl>                                | <span data-ttu-id="7ec6d-136">Ce type d’ouverture de session est destiné aux serveurs à hautes performances pour authentifier les mots de passe en texte clair.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-136">This logon type is intended for high performance servers to authenticate plaintext passwords.</span></span> <span data-ttu-id="7ec6d-137">La fonction **LogonUserExExW** ne met pas en cache les informations d’identification pour ce type de connexion.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-137">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <span data-ttu-id="7ec6d-138"><dt>**LOGON32 \_ \_Lot d’ouverture de session**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-138"><dt>**LOGON32\_LOGON\_BATCH**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="7ec6d-139">Ce type de connexion est destiné aux serveurs batch, où les processus peuvent s’exécuter pour le compte d’un utilisateur sans leur intervention directe.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-139">This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention.</span></span> <span data-ttu-id="7ec6d-140">Ce type est également destiné aux serveurs de performances plus importants qui traitent de nombreuses tentatives d’authentification en texte clair à la fois, comme les serveurs de messagerie ou les serveurs Web.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-140">This type is also for higher performance servers that process many plaintext authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="7ec6d-141">La fonction **LogonUserExExW** ne met pas en cache les informations d’identification pour ce type de connexion.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-141">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <span data-ttu-id="7ec6d-142"><dt>**LOGON32 \_ \_Service d’ouverture de session**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-142"><dt>**LOGON32\_LOGON\_SERVICE**</dt> <dt>5</dt></span></span> </dl>                                | <span data-ttu-id="7ec6d-143">Indique une ouverture de session de type service.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-143">Indicates a service-type logon.</span></span> <span data-ttu-id="7ec6d-144">Le compte fourni doit avoir le privilège de service activé.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-144">The account provided must have the service privilege enabled.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <span data-ttu-id="7ec6d-145"><dt>**LOGON32 \_ Ouverture de session \_ déverrouillage**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-145"><dt>**LOGON32\_LOGON\_UNLOCK**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="7ec6d-146">Ce type de connexion concerne les dll [*Gina*](../secgloss/g-gly.md) qui se connectent aux utilisateurs qui se connectent de manière interactive à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-146">This logon type is for [*GINA*](../secgloss/g-gly.md) DLLs that log on users who will be interactively using the computer.</span></span> <span data-ttu-id="7ec6d-147">Ce type d’ouverture de session peut générer un enregistrement d’audit unique qui indique le moment où la station de travail a été déverrouillée.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-147">This logon type can generate a unique audit record that shows when the workstation was unlocked.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <span data-ttu-id="7ec6d-148"><dt>**LOGON32 \_ \_Texte en \_ clair du réseau de connexion**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-148"><dt>**LOGON32\_LOGON\_NETWORK\_CLEARTEXT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="7ec6d-149">Ce type d’ouverture de session conserve le nom et le mot de passe dans le [*package d’authentification*](../secgloss/a-gly.md), ce qui permet au serveur d’établir des connexions à d’autres serveurs réseau tout en usurpant l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-149">This logon type preserves the name and password in the [*authentication package*](../secgloss/a-gly.md), which allows the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="7ec6d-150">Un serveur peut accepter des informations d’identification en texte clair d’un client, appeler **LogonUserExExW**, vérifier que l’utilisateur peut accéder au système sur le réseau et toujours communiquer avec d’autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-150">A server can accept plaintext credentials from a client, call **LogonUserExExW**, verify that the user can access the system across the network, and still communicate with other servers.</span></span> <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <span data-ttu-id="7ec6d-151"><dt>**LOGON32 \_ Ouvrir une session- \_ nouvelles \_ informations d’identification**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-151"><dt>**LOGON32\_LOGON\_NEW\_CREDENTIALS**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="7ec6d-152">Ce type d’ouverture de session permet à l’appelant de cloner son jeton actuel et de spécifier de nouvelles informations d’identification pour les connexions sortantes.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-152">This logon type allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="7ec6d-153">La nouvelle session d’ouverture de session a le même identificateur local, mais elle utilise des informations d’identification différentes pour d’autres connexions réseau.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-153">The new logon session has the same local identifier but uses different credentials for other network connections.</span></span><br/> <span data-ttu-id="7ec6d-154">Ce type d’ouverture de session est pris en charge uniquement par le fournisseur **LOGON32 \_ \_ WINNT50** Logon Provider.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-154">This logon type is supported only by the **LOGON32\_PROVIDER\_WINNT50** logon provider.</span></span><br/>                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="7ec6d-155">*dwLogonProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-155">*dwLogonProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-156">Fournisseur d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-156">The logon provider.</span></span> <span data-ttu-id="7ec6d-157">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-157">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7ec6d-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ec6d-158">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="7ec6d-159">Signification</span><span class="sxs-lookup"><span data-stu-id="7ec6d-159">Meaning</span></span>                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <span data-ttu-id="7ec6d-160"><dt>**\_Fournisseur LOGON32 \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-160"><dt>**LOGON32\_PROVIDER\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="7ec6d-161">Utilisez le fournisseur d’ouverture de session standard pour le système.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-161">Use the standard logon provider for the system.</span></span> <span data-ttu-id="7ec6d-162">Le [*fournisseur de sécurité*](../secgloss/s-gly.md) par défaut est NTLM.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-162">The default [*security provider*](../secgloss/s-gly.md) is NTLM.</span></span><br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <span data-ttu-id="7ec6d-163"><dt>**\_Fournisseur LOGON32 \_ WINNT50**</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-163"><dt>**LOGON32\_PROVIDER\_WINNT50**</dt></span></span> </dl> | <span data-ttu-id="7ec6d-164">Utilisez le fournisseur Negotiate Logon.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-164">Use the negotiate logon provider.</span></span> <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <span data-ttu-id="7ec6d-165"><dt>**\_Fournisseur LOGON32 \_ WINNT40**</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-165"><dt>**LOGON32\_PROVIDER\_WINNT40**</dt></span></span> </dl> | <span data-ttu-id="7ec6d-166">Utilisez le fournisseur d’ouverture de session NTLM.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-166">Use the NTLM logon provider.</span></span><br/>                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="7ec6d-167">*pTokenGroups* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-167">*pTokenGroups* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-168">Pointeur vers une structure [**de \_ groupes de jetons**](/windows/win32/api/winnt/ns-winnt-token_groups) qui spécifie une liste de SID de groupe ajoutée au jeton que cette fonction reçoit lorsque la connexion réussit.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-168">A pointer to a [**TOKEN\_GROUPS**](/windows/win32/api/winnt/ns-winnt-token_groups) structure that specifies a list of group SIDs that are added to the token that this function receives upon successful logon.</span></span> <span data-ttu-id="7ec6d-169">Les SID ajoutés au jeton affectent également l’expansion de groupe.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-169">Any SIDs added to the token also effect group expansion.</span></span> <span data-ttu-id="7ec6d-170">Par exemple, si les SID ajoutés sont membres de groupes locaux, ces groupes sont également ajoutés au jeton d’accès reçu.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-170">For example, if the added SIDs are members of local groups, those groups are also added to the received access token.</span></span>

<span data-ttu-id="7ec6d-171">Si ce paramètre n’est pas **null**, l’appelant de cette fonction doit avoir le privilège de **privilège de se \_ TCB \_** accordé et activé.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-171">If this parameter is not **NULL**, the caller of this function must have the **SE\_TCB\_PRIVILEGE** privilege granted and enabled.</span></span>

</dd> <dt>

<span data-ttu-id="7ec6d-172">*phToken* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-172">*phToken* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-173">Pointeur vers une variable de handle qui reçoit un handle vers un jeton qui représente l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-173">A pointer to a handle variable that receives a handle to a token that represents the specified user.</span></span>

<span data-ttu-id="7ec6d-174">Vous pouvez utiliser le handle retourné dans les appels à la fonction [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .</span><span class="sxs-lookup"><span data-stu-id="7ec6d-174">You can use the returned handle in calls to the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function.</span></span>

<span data-ttu-id="7ec6d-175">Dans la plupart des cas, le handle retourné est un [*jeton principal*](../secgloss/p-gly.md) que vous pouvez utiliser dans les appels à la fonction [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="7ec6d-175">In most cases, the returned handle is a [*primary token*](../secgloss/p-gly.md) that you can use in calls to the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="7ec6d-176">Toutefois, si vous spécifiez l' \_ indicateur de réseau de connexion LOGON32 \_ , **LogonUserExExW** retourne un [*jeton d’emprunt d’identité*](../secgloss/i-gly.md) que vous ne pouvez pas utiliser dans **CreateProcessAsUser** , sauf si vous appelez [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) pour convertir le jeton d’emprunt d’identité en jeton principal.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-176">However, if you specify the LOGON32\_LOGON\_NETWORK flag, **LogonUserExExW** returns an [*impersonation token*](../secgloss/i-gly.md) that you cannot use in **CreateProcessAsUser** unless you call [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) to convert the impersonation token to a primary token.</span></span>

<span data-ttu-id="7ec6d-177">Lorsque vous n’avez plus besoin de ce handle, fermez-le en appelant la fonction [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="7ec6d-177">When you no longer need this handle, close it by calling the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

</dd> <dt>

<span data-ttu-id="7ec6d-178">*ppLogonSid* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-178">*ppLogonSid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-179">Pointeur vers un pointeur vers un SID qui reçoit le SID de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-179">A pointer to a pointer to a SID that receives the SID of the user logged on.</span></span>

<span data-ttu-id="7ec6d-180">Lorsque vous avez fini d’utiliser le SID, libérez-le en appelant la fonction [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) .</span><span class="sxs-lookup"><span data-stu-id="7ec6d-180">When you have finished using the SID, free it by calling the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function.</span></span>

</dd> <dt>

<span data-ttu-id="7ec6d-181">*ppProfileBuffer* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-181">*ppProfileBuffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-182">Pointeur vers un pointeur qui reçoit l’adresse d’une mémoire tampon qui contient le profil de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-182">A pointer to a pointer that receives the address of a buffer that contains the logged on user's profile.</span></span>

</dd> <dt>

<span data-ttu-id="7ec6d-183">*pdwProfileLength* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-183">*pdwProfileLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-184">Pointeur vers une **valeur DWORD** qui reçoit la longueur de la mémoire tampon du profil.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-184">A pointer to a **DWORD** that receives the length of the profile buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7ec6d-185">*pQuotaLimits* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-185">*pQuotaLimits* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec6d-186">Pointeur vers une structure [**de \_ limites de quota**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) qui reçoit des informations sur les quotas pour l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-186">A pointer to a [**QUOTA\_LIMITS**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) structure that receives information about the quotas for the logged on user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ec6d-187">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ec6d-187">Return value</span></span>

<span data-ttu-id="7ec6d-188">Si la fonction est réussie, la fonction retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-188">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="7ec6d-189">Si la fonction échoue, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-189">If the function fails, it returns zero.</span></span> <span data-ttu-id="7ec6d-190">Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7ec6d-190">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec6d-191">Remarques</span><span class="sxs-lookup"><span data-stu-id="7ec6d-191">Remarks</span></span>

<span data-ttu-id="7ec6d-192">Le type de connexion **\_ \_ réseau LOGON32 Logon** est plus rapide, mais il présente les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ec6d-192">The **LOGON32\_LOGON\_NETWORK** logon type is fastest, but it has the following limitations:</span></span>

-   <span data-ttu-id="7ec6d-193">La fonction retourne un [*jeton d’emprunt d’identité*](../secgloss/i-gly.md), et non un jeton principal.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-193">The function returns an [*impersonation token*](../secgloss/i-gly.md), not a primary token.</span></span> <span data-ttu-id="7ec6d-194">Vous ne pouvez pas utiliser ce jeton directement dans la fonction [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="7ec6d-194">You cannot use this token directly in the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="7ec6d-195">Toutefois, vous pouvez appeler la fonction [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) pour convertir le jeton en jeton principal, puis l’utiliser dans **CreateProcessAsUser**.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-195">However, you can call the [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) function to convert the token to a primary token, and then use it in **CreateProcessAsUser**.</span></span>
-   <span data-ttu-id="7ec6d-196">Si vous convertissez le jeton en jeton principal et que vous l’utilisez dans [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) pour démarrer un processus, le nouveau processus ne peut pas accéder à d’autres ressources réseau, telles que des serveurs distants ou des imprimantes, par le biais du redirecteur.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-196">If you convert the token to a primary token and use it in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) to start a process, the new process cannot access other network resources, such as remote servers or printers, through the redirector.</span></span> <span data-ttu-id="7ec6d-197">Une exception est que, si la ressource réseau n’est pas contrôlée par l’accès, le nouveau processus peut y accéder.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-197">An exception is that if the network resource is not access controlled, then the new process will be able to access it.</span></span>

<span data-ttu-id="7ec6d-198">Le compte spécifié par *lpszUsername* doit disposer des droits de compte nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-198">The account specified by *lpszUsername* must have the necessary account rights.</span></span> <span data-ttu-id="7ec6d-199">Par exemple, pour ouvrir une session sur un utilisateur avec l’indicateur **\_ \_ interactif d’ouverture de session LOGON32** , l’utilisateur (ou un groupe auquel l’utilisateur appartient) doit avoir le droit de compte de **\_ \_ \_ nom d’ouverture de session interactive se** .</span><span class="sxs-lookup"><span data-stu-id="7ec6d-199">For example, to log on a user with the **LOGON32\_LOGON\_INTERACTIVE** flag, the user (or a group to which the user belongs) must have the **SE\_INTERACTIVE\_LOGON\_NAME** account right.</span></span> <span data-ttu-id="7ec6d-200">Pour obtenir la liste des droits de compte qui affectent les différentes opérations d’ouverture de session, consultez [droits d’accès à un objet de compte](../secmgmt/account-object-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="7ec6d-200">For a list of the account rights that affect the various logon operations, see [Account Object Access Rights](../secmgmt/account-object-access-rights.md).</span></span>

<span data-ttu-id="7ec6d-201">Un utilisateur est considéré comme connecté s’il existe au moins un jeton.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-201">A user is considered logged on if at least one token exists.</span></span> <span data-ttu-id="7ec6d-202">Si vous appelez [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) , puis que vous fermez le jeton, l’utilisateur est toujours connecté jusqu’à ce que le processus (et tous les processus enfants) se termine.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-202">If you call [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) and then close the token, the user is still logged on until the process (and all child processes) have ended.</span></span>

<span data-ttu-id="7ec6d-203">Si le paramètre facultatif *pTokenGroups* est fourni, LSA n’ajoutera pas automatiquement le SID local ou le SID d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-203">If the optional *pTokenGroups* parameter is supplied, LSA will not add either the local SID or the logon SID automatically.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec6d-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ec6d-204">Requirements</span></span>



| <span data-ttu-id="7ec6d-205">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ec6d-205">Requirement</span></span> | <span data-ttu-id="7ec6d-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ec6d-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec6d-207">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ec6d-207">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec6d-208">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-208">Windows Vista \[desktop apps only\]</span></span><br/>                                                                        |
| <span data-ttu-id="7ec6d-209">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ec6d-209">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec6d-210">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ec6d-210">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="7ec6d-211">Version</span><span class="sxs-lookup"><span data-stu-id="7ec6d-211">Version</span></span><br/>                  | <span data-ttu-id="7ec6d-212">LogonUserExExW est également disponible onWindows Server 2003 ou Windows XPwith la version de distribution générale.</span><span class="sxs-lookup"><span data-stu-id="7ec6d-212">LogonUserExExW is also available onWindows Server 2003 or Windows XPwith the General Distribution Release.</span></span><br/> |
| <span data-ttu-id="7ec6d-213">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ec6d-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ec6d-214"><dt>Winbasep. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-214"><dt>Winbasep.h</dt></span></span> </dl>                                 |
| <span data-ttu-id="7ec6d-215">DLL</span><span class="sxs-lookup"><span data-stu-id="7ec6d-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ec6d-216"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ec6d-216"><dt>Advapi32.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7ec6d-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ec6d-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec6d-218">Access Control client/serveur</span><span class="sxs-lookup"><span data-stu-id="7ec6d-218">Client/Server Access Control</span></span>](../secauthz/client-server-access-control.md)
</dt> <dt>

[<span data-ttu-id="7ec6d-219">Fonctions de Access Control client/serveur</span><span class="sxs-lookup"><span data-stu-id="7ec6d-219">Client/Server Access Control Functions</span></span>](../secauthz/authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="7ec6d-220">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="7ec6d-220">**CloseHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[<span data-ttu-id="7ec6d-221">**CreateProcessAsUser**</span><span class="sxs-lookup"><span data-stu-id="7ec6d-221">**CreateProcessAsUser**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[<span data-ttu-id="7ec6d-222">**DuplicateTokenEx**</span><span class="sxs-lookup"><span data-stu-id="7ec6d-222">**DuplicateTokenEx**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[<span data-ttu-id="7ec6d-223">**ImpersonateLoggedOnUser**</span><span class="sxs-lookup"><span data-stu-id="7ec6d-223">**ImpersonateLoggedOnUser**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[<span data-ttu-id="7ec6d-224">**LogonUserEx**</span><span class="sxs-lookup"><span data-stu-id="7ec6d-224">**LogonUserEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[<span data-ttu-id="7ec6d-225">**limites de QUOTA \_**</span><span class="sxs-lookup"><span data-stu-id="7ec6d-225">**QUOTA\_LIMITS**</span></span>](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
