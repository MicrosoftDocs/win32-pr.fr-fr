---
description: L’infrastructure VSS requiert que les demandeurs VSS, tels que les applications de sauvegarde, puissent fonctionner à la fois comme clients COM et comme serveur.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Considérations relatives à la sécurité pour les demandeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318981"
---
# <a name="security-considerations-for-requesters"></a><span data-ttu-id="5550a-103">Considérations relatives à la sécurité pour les demandeurs</span><span class="sxs-lookup"><span data-stu-id="5550a-103">Security Considerations for Requesters</span></span>

<span data-ttu-id="5550a-104">L’infrastructure VSS requiert que les demandeurs VSS, tels que les applications de sauvegarde, puissent fonctionner à la fois comme clients COM et comme serveur.</span><span class="sxs-lookup"><span data-stu-id="5550a-104">The VSS infrastructure requires VSS requesters, such as backup applications, to be able to function both as COM clients and as a server.</span></span>

<span data-ttu-id="5550a-105">Lorsqu’il joue le rôle de serveur, un demandeur expose un ensemble d’interfaces de rappel COM qui peuvent être appelées à partir de processus externes (tels que des Writers ou le service VSS).</span><span class="sxs-lookup"><span data-stu-id="5550a-105">When acting as a server, a requester exposes a set of COM callback interfaces that can be invoked from external processes (such as writers or the VSS service).</span></span> <span data-ttu-id="5550a-106">Par conséquent, les demandeurs doivent gérer en toute sécurité les clients COM qui sont en mesure d’effectuer des appels COM entrants dans son processus.</span><span class="sxs-lookup"><span data-stu-id="5550a-106">Therefore, requesters need to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="5550a-107">De même, les demandeurs peuvent agir comme un client COM pour les API COM fournies par un enregistreur VSS ou par le service VSS.</span><span class="sxs-lookup"><span data-stu-id="5550a-107">Similarly, requesters can act as a COM client for the COM APIs supplied by a VSS writer or by the VSS service.</span></span> <span data-ttu-id="5550a-108">Les paramètres de sécurité spécifiques au demandeur doivent autoriser les appels COM sortants du demandeur à ces autres processus.</span><span class="sxs-lookup"><span data-stu-id="5550a-108">The requester-specific security settings must allow outgoing COM calls from the requester to these other processes.</span></span>

<span data-ttu-id="5550a-109">Le mécanisme le plus simple pour gérer les problèmes de sécurité d’un demandeur consiste à sélectionner correctement le compte d’utilisateur sous lequel il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="5550a-109">The simplest mechanism for managing a requester's security issues involves proper selection of the user account under which it runs.</span></span>

<span data-ttu-id="5550a-110">Un demandeur doit généralement s’exécuter sous un utilisateur membre du groupe administrateurs ou opérateurs de sauvegarde, ou bien s’exécuter en tant que compte système local.</span><span class="sxs-lookup"><span data-stu-id="5550a-110">A requester typically needs to run under a user that is a member of either the Administrators group or the Backup Operators group, or run as the Local System account.</span></span>

<span data-ttu-id="5550a-111">Par défaut, lorsqu’un demandeur agit comme un client COM, s’il ne s’exécute pas sous ces comptes, tout appel COM est automatiquement rejeté avec **E \_ ACCESSDENIED**, sans même avoir à accéder à l’implémentation de la méthode com.</span><span class="sxs-lookup"><span data-stu-id="5550a-111">By default, when a requester is acting as a COM client, if it does not run under these accounts, any COM call is automatically rejected with **E\_ACCESSDENIED**, without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="5550a-112">Désactivation de la gestion des exceptions COM</span><span class="sxs-lookup"><span data-stu-id="5550a-112">Disabling COM Exception Handling</span></span>

<span data-ttu-id="5550a-113">Lors du développement d’un demandeur, définissez l’exception COM COMGLB \_ exception \_ ne \_ handle d’options globales pour désactiver la gestion des exceptions com.</span><span class="sxs-lookup"><span data-stu-id="5550a-113">When developing a requester, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="5550a-114">Il est important de le faire, car la gestion des exceptions COM peut masquer les erreurs irrécupérables dans une application VSS.</span><span class="sxs-lookup"><span data-stu-id="5550a-114">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="5550a-115">L’erreur masquée peut rendre le processus dans un état instable et imprévisible, ce qui peut entraîner des altérations et des blocages.</span><span class="sxs-lookup"><span data-stu-id="5550a-115">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="5550a-116">Pour plus d’informations sur cet indicateur, consultez [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="5550a-116">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-requester-default-com-access-check-permission"></a><span data-ttu-id="5550a-117">Définition de l’autorisation de vérification de l’accès COM par défaut du demandeur</span><span class="sxs-lookup"><span data-stu-id="5550a-117">Setting Requester Default COM Access Check Permission</span></span>

<span data-ttu-id="5550a-118">Les demandeurs doivent savoir que lorsque leur processus agit comme un serveur (par exemple, en autorisant les enregistreurs à modifier le document des composants de sauvegarde), ils doivent autoriser les appels entrants d’autres participants VSS, tels que les enregistreurs ou le service VSS.</span><span class="sxs-lookup"><span data-stu-id="5550a-118">Requesters need to be aware that when their process acts as a server (for example, allowing writers to modify the Backup Components Document), they must allow incoming calls from other VSS participants, such as writers or the VSS service.</span></span>

<span data-ttu-id="5550a-119">Toutefois, par défaut, un processus Windows autorise uniquement les clients COM qui s’exécutent sous la même session de connexion (le SID SELF) ou s’exécutent sous le compte système local.</span><span class="sxs-lookup"><span data-stu-id="5550a-119">However, by default, a Windows process will allow only COM clients that are running under the same logon session (the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="5550a-120">Il s’agit d’un problème potentiel, car ces paramètres par défaut ne sont pas adaptés à l’infrastructure VSS.</span><span class="sxs-lookup"><span data-stu-id="5550a-120">This is a potential problem because these defaults are not adequate for the VSS infrastructure.</span></span> <span data-ttu-id="5550a-121">Par exemple, les enregistreurs peuvent s’exécuter en tant que compte d’utilisateur « opérateur de sauvegarde » qui n’est pas dans la même session de connexion que le processus du demandeur ou un compte système local.</span><span class="sxs-lookup"><span data-stu-id="5550a-121">For example, writers might run as a "Backup Operator" user account that is neither in the same logon session as the requester process nor a Local System account.</span></span>

<span data-ttu-id="5550a-122">Pour gérer ce type de problème, chaque processus serveur COM peut exercer un contrôle accru sur le fait qu’un client RPC ou COM est autorisé à exécuter une méthode COM implémentée par le serveur (demandeur dans ce cas) en utilisant [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir une autorisation de vérification de l’accès com par défaut au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="5550a-122">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method implemented by the server (a requester in this case) by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide "Default COM Access Check Permission".</span></span>

<span data-ttu-id="5550a-123">Les demandeurs peuvent explicitement effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5550a-123">Requesters can explicitly do the following:</span></span>

-   <span data-ttu-id="5550a-124">Autorisez l’accès de tous les processus à appeler le processus du demandeur.</span><span class="sxs-lookup"><span data-stu-id="5550a-124">Allow all processes access to call into the requester process.</span></span>

    <span data-ttu-id="5550a-125">Cette option peut être adaptée à la grande majorité des demandeurs et est utilisée par d’autres serveurs COM. par exemple, tous les services Windows basés sur SVCHOST utilisent déjà cette option, comme tous les services COM+ par défaut.</span><span class="sxs-lookup"><span data-stu-id="5550a-125">This option may be adequate for the vast majority of requesters, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="5550a-126">Autoriser tous les processus à effectuer des appels COM entrants n’est pas nécessairement une faille de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5550a-126">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="5550a-127">Un demandeur agissant comme un serveur COM, comme tous les autres serveurs COM, conserve toujours l’option permettant d’autoriser ses clients sur chaque méthode COM implémentée dans son processus.</span><span class="sxs-lookup"><span data-stu-id="5550a-127">A requester acting as a COM server, like all other COM servers, always retains the option to authorize its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="5550a-128">Notez que les rappels COM internes implémentés par VSS sont sécurisés par défaut.</span><span class="sxs-lookup"><span data-stu-id="5550a-128">Note that internal COM callbacks implemented by VSS are secured by default.</span></span>

    <span data-ttu-id="5550a-129">Pour permettre à tous les processus d’accéder à COM à un demandeur, vous pouvez passer un descripteur de sécurité **null** comme premier paramètre de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="5550a-129">To allow all processes COM access to a requester, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="5550a-130">(Notez que **CoInitializeSecurity** doit être appelé au plus une fois pour l’ensemble du processus.</span><span class="sxs-lookup"><span data-stu-id="5550a-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="5550a-131">Pour plus d’informations sur les appels **CoInitializeSecurity** , consultez la documentation com ou MSDN.)</span><span class="sxs-lookup"><span data-stu-id="5550a-131">Please see the COM documentation or MSDN for more information on **CoInitializeSecurity** calls.)</span></span>

    <span data-ttu-id="5550a-132">L’exemple de code suivant montre comment un demandeur doit appeler [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) dans Windows 8 et windows server 2012 et versions ultérieures, afin d’être compatible avec VSS pour les partages de fichiers distants (VSS) :</span><span class="sxs-lookup"><span data-stu-id="5550a-132">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 and Windows Server 2012 and later, in order to be compatible with VSS for remote file shares (RVSS):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="5550a-133">Lors de la définition explicite de la sécurité de niveau COM d’un demandeur avec [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5550a-133">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="5550a-134">Définissez le niveau d’authentification sur au moins l' **\_ \_ \_ \_ \_ intégrité PKT au niveau** de l’authentification RPC C.</span><span class="sxs-lookup"><span data-stu-id="5550a-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**.</span></span> <span data-ttu-id="5550a-135">Pour une meilleure sécurité, envisagez d’utiliser la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C**.</span><span class="sxs-lookup"><span data-stu-id="5550a-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="5550a-136">Définissez le niveau d’emprunt d’identité sur le niveau d’emprunt d' **\_ \_ \_ \_ identité RPC C IMP**.</span><span class="sxs-lookup"><span data-stu-id="5550a-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span>
    -   <span data-ttu-id="5550a-137">Définissez les fonctionnalités de sécurité de masquage sur **EOAC \_ statique**.</span><span class="sxs-lookup"><span data-stu-id="5550a-137">Set the cloaking security capabilities to **EOAC\_STATIC**.</span></span> <span data-ttu-id="5550a-138">Pour plus d’informations sur le masquage de la sécurité, consultez [masquage](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="5550a-138">For more information about cloaking security, see [Cloaking](../com/cloaking.md).</span></span>

    <span data-ttu-id="5550a-139">L’exemple de code suivant montre comment un demandeur doit appeler [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) dans Windows 7 et windows Server 2008 R2 et versions antérieures (ou dans Windows 8 et windows server 2012 et versions ultérieures, si la compatibilité VSS n’est pas nécessaire) :</span><span class="sxs-lookup"><span data-stu-id="5550a-139">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 and Windows Server 2008 R2 and earlier (or in Windows 8 and Windows Server 2012 and later, if RVSS compatibility is not needed):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="5550a-140">Lors de la définition explicite de la sécurité de niveau COM d’un demandeur avec [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5550a-140">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="5550a-141">Définissez le niveau d’authentification au moins **au \_ niveau de \_ \_ \_ connexion RPC C Authn**.</span><span class="sxs-lookup"><span data-stu-id="5550a-141">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span> <span data-ttu-id="5550a-142">Pour une meilleure sécurité, envisagez d’utiliser la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C**.</span><span class="sxs-lookup"><span data-stu-id="5550a-142">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="5550a-143">Définissez le niveau d’emprunt d’identité sur **RPC \_ C \_ IMP \_ Level \_ identifier** , sauf si le processus du demandeur doit autoriser l’emprunt d’identité pour des appels RPC ou com spécifiques qui ne sont pas liés à VSS.</span><span class="sxs-lookup"><span data-stu-id="5550a-143">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the requester process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="5550a-144">Autorisez uniquement l’accès aux processus spécifiés pour appeler le processus du demandeur.</span><span class="sxs-lookup"><span data-stu-id="5550a-144">Allow only specified processes access to call into the requester process.</span></span>

    <span data-ttu-id="5550a-145">Un serveur COM (tel qu’un demandeur) qui appelle [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) avec un descripteur de sécurité non **null** comme premier paramètre peut utiliser le descripteur pour se configurer lui-même pour accepter les appels entrants uniquement des utilisateurs qui appartiennent à un ensemble spécifique de comptes.</span><span class="sxs-lookup"><span data-stu-id="5550a-145">A COM server (such as a requester) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor as the first parameter can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="5550a-146">Un demandeur doit s’assurer que les clients COM s’exécutant sous des utilisateurs valides sont autorisés à appeler son processus.</span><span class="sxs-lookup"><span data-stu-id="5550a-146">A requester must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="5550a-147">Un demandeur qui spécifie un descripteur de sécurité dans le premier paramètre doit autoriser les utilisateurs suivants à effectuer des appels entrants dans le processus du demandeur :</span><span class="sxs-lookup"><span data-stu-id="5550a-147">A requester that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="5550a-148">Système Local</span><span class="sxs-lookup"><span data-stu-id="5550a-148">Local System</span></span>
    -   <span data-ttu-id="5550a-149">Service local</span><span class="sxs-lookup"><span data-stu-id="5550a-149">Local Service</span></span>

        <span data-ttu-id="5550a-150">**Windows XP :** Cette valeur n’est pas prise en charge avant Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5550a-150">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="5550a-151">Service réseau</span><span class="sxs-lookup"><span data-stu-id="5550a-151">Network Service</span></span>

        <span data-ttu-id="5550a-152">**Windows XP :** Cette valeur n’est pas prise en charge avant Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5550a-152">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="5550a-153">Membres du groupe Administrateurs local</span><span class="sxs-lookup"><span data-stu-id="5550a-153">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="5550a-154">Membres du groupe opérateurs de sauvegarde local</span><span class="sxs-lookup"><span data-stu-id="5550a-154">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="5550a-155">Utilisateurs spéciaux spécifiés dans l’emplacement du Registre ci-dessous, avec « 1 » comme \_ valeur de Registre DWORD</span><span class="sxs-lookup"><span data-stu-id="5550a-155">Special users that are specified in the registry location below, with "1" as their REG\_DWORD value</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a><span data-ttu-id="5550a-156">Contrôle explicite de l’accès d’un compte d’utilisateur à un demandeur</span><span class="sxs-lookup"><span data-stu-id="5550a-156">Explicitly Controlling User Account Access to a Requester</span></span>

<span data-ttu-id="5550a-157">Dans certains cas, la restriction de l’accès à un demandeur à des processus s’exécutant en tant que système local, ou sous les groupes Administrateurs locaux ou opérateurs de sauvegarde locaux, peut être trop restrictive.</span><span class="sxs-lookup"><span data-stu-id="5550a-157">There are cases where restricting access to a requester to processes running as Local System, or under the local Administrators or local Backup Operators groups, may be too restrictive.</span></span>

<span data-ttu-id="5550a-158">Par exemple, il se peut que le processus d’un demandeur spécifié ne doive normalement pas être exécuté sous un compte d’administrateur ou d’opérateur de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="5550a-158">For example, a specified requester process might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="5550a-159">Pour des raisons de sécurité, il est préférable de ne pas promouvoir artificiellement les privilèges de processus pour prendre en charge VSS.</span><span class="sxs-lookup"><span data-stu-id="5550a-159">For security reasons, it would be best not to artificially promote the processes privileges to support VSS.</span></span>

<span data-ttu-id="5550a-160">Dans ces cas, vous devez modifier la clé de Registre HKEY VssAccessControl VSS du système de l' **\_ \_ ordinateur local** \\  \\  \\  \\  \\  pour indiquer à VSS qu’un utilisateur spécifié peut exécuter un demandeur VSS en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="5550a-160">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS requester.</span></span>

<span data-ttu-id="5550a-161">Sous cette clé, vous devez créer une sous-clé portant le même nom que le compte auquel l’accès doit être accordé ou refusé.</span><span class="sxs-lookup"><span data-stu-id="5550a-161">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="5550a-162">Cette sous-clé doit être définie sur l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5550a-162">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="5550a-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="5550a-163">Value</span></span> | <span data-ttu-id="5550a-164">Signification</span><span class="sxs-lookup"><span data-stu-id="5550a-164">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="5550a-165">0</span><span class="sxs-lookup"><span data-stu-id="5550a-165">0</span></span>     | <span data-ttu-id="5550a-166">Refusez à l’utilisateur l’accès à votre rédacteur et au demandeur.</span><span class="sxs-lookup"><span data-stu-id="5550a-166">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="5550a-167">1</span><span class="sxs-lookup"><span data-stu-id="5550a-167">1</span></span>     | <span data-ttu-id="5550a-168">Accordez à l’utilisateur l’accès à votre rédacteur.</span><span class="sxs-lookup"><span data-stu-id="5550a-168">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="5550a-169">2</span><span class="sxs-lookup"><span data-stu-id="5550a-169">2</span></span>     | <span data-ttu-id="5550a-170">Accordez à l’utilisateur l’accès à votre demandeur.</span><span class="sxs-lookup"><span data-stu-id="5550a-170">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="5550a-171">3</span><span class="sxs-lookup"><span data-stu-id="5550a-171">3</span></span>     | <span data-ttu-id="5550a-172">Accordez à l’utilisateur l’accès à votre rédacteur et au demandeur.</span><span class="sxs-lookup"><span data-stu-id="5550a-172">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="5550a-173">L’exemple suivant accorde l’accès au compte « MyDomain \\ myuser » :</span><span class="sxs-lookup"><span data-stu-id="5550a-173">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="5550a-174">Ce mécanisme peut également être utilisé pour empêcher explicitement un utilisateur autorisé à exécuter un demandeur VSS.</span><span class="sxs-lookup"><span data-stu-id="5550a-174">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS requester.</span></span> <span data-ttu-id="5550a-175">L’exemple suivant permet de restreindre l’accès à partir du \\ compte « administrateur ThatDomain » :</span><span class="sxs-lookup"><span data-stu-id="5550a-175">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="5550a-176">L’administrateur ThatDomain de l’utilisateur \\ ne peut pas exécuter un demandeur VSS.</span><span class="sxs-lookup"><span data-stu-id="5550a-176">The user ThatDomain\\Administrator would not be able to run a VSS requester.</span></span>

## <a name="performing-a-file-backup-of-the-system-state"></a><span data-ttu-id="5550a-177">Exécution d’une sauvegarde de fichiers de l’état du système</span><span class="sxs-lookup"><span data-stu-id="5550a-177">Performing a File Backup of the System State</span></span>

<span data-ttu-id="5550a-178">Si un demandeur effectue une sauvegarde de l’état du système en sauvegardant des fichiers individuels au lieu d’utiliser une image de volume pour la sauvegarde, il doit appeler les fonctions [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) et [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) pour énumérer les liens physiques des fichiers qui se trouvent dans les répertoires suivants :</span><span class="sxs-lookup"><span data-stu-id="5550a-178">If a requester performs system-state backup by backing up individual files instead of using a volume image for the backup, it must call the [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions to enumerate hard links on files that are located in the following directories:</span></span>

-   <span data-ttu-id="5550a-179">Windows \\ system32 \\ WDI \\ perftrack</span><span class="sxs-lookup"><span data-stu-id="5550a-179">Windows\\system32\\WDI\\perftrack</span></span>\\
-   <span data-ttu-id="5550a-180">Windows \\ WINSXS</span><span class="sxs-lookup"><span data-stu-id="5550a-180">Windows\\WINSXS</span></span>\\

<span data-ttu-id="5550a-181">Ces répertoires sont accessibles uniquement par les membres du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="5550a-181">These directories can only be accessed by members of the Administrators group.</span></span> <span data-ttu-id="5550a-182">Pour cette raison, un tel demandeur doit s’exécuter sous le compte système ou un compte d’utilisateur membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="5550a-182">For this reason, such a requester must run under the system account or a user account that is a member of the Administrators group.</span></span>

<span data-ttu-id="5550a-183">**Windows XP et Windows Server 2003 :** Les fonctions [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) et [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) ne sont pas prises en charge jusqu’à Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5550a-183">**Windows XP and Windows Server 2003:** The [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions are not supported until Windows Vista and Windows Server 2008.</span></span>

 

 
