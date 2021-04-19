---
description: L’infrastructure VSS exige que les processus d’écriture fonctionnent à la fois comme clients COM et comme serveurs.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Considérations relatives à la sécurité pour les Writers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524603"
---
# <a name="security-considerations-for-writers"></a><span data-ttu-id="8a9ac-103">Considérations relatives à la sécurité pour les Writers</span><span class="sxs-lookup"><span data-stu-id="8a9ac-103">Security Considerations for Writers</span></span>

<span data-ttu-id="8a9ac-104">L’infrastructure VSS exige que les processus d’écriture fonctionnent à la fois comme clients COM et comme serveurs.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-104">The VSS infrastructure requires writer processes to be able to function both as COM clients and as servers.</span></span>

<span data-ttu-id="8a9ac-105">Lorsqu’ils agissent en tant que serveurs, les enregistreurs VSS exposent des interfaces COM (par exemple, les gestionnaires d’événements VSS tels que [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) [**) et**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)reçoivent des appels com entrants à partir de processus VSS (tels que les demandeurs et le service VSS) ou des appels RPC à partir de processus externes à VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-105">When acting as servers, VSS writers expose COM interfaces (for example, the VSS event handlers such as [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) and receive incoming COM calls from VSS processes (such as requesters and the VSS service) or RPC calls from processes that are external to VSS, typically when these processes generate VSS events (for example, when a requester calls [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).</span></span> <span data-ttu-id="8a9ac-106">Par conséquent, un enregistreur VSS doit gérer en toute sécurité les clients COM qui sont en mesure d’effectuer des appels COM entrants dans son processus.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-106">Therefore, a VSS writer needs to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="8a9ac-107">De même, les enregistreurs VSS peuvent également agir en tant que clients COM, en effectuant des appels COM sortants vers des rappels fournis par l’infrastructure VSS ou des appels RPC à des processus qui sont externes à VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-107">Similarly, VSS writers may also act as COM clients, making outgoing COM calls to callbacks supplied by the VSS infrastructure or RPC calls to processes that are external to VSS.</span></span> <span data-ttu-id="8a9ac-108">Ces rappels fournis par une application de sauvegarde ou par le service VSS permettent à l’enregistreur d’effectuer des tâches telles que la mise à jour du document des composants de sauvegarde par le biais de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .</span><span class="sxs-lookup"><span data-stu-id="8a9ac-108">These callbacks that are provided either by a backup application or by the VSS service allow the writer to perform tasks such as updating the Backup Components Document through the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface.</span></span> <span data-ttu-id="8a9ac-109">Par conséquent, les paramètres de sécurité VSS doivent permettre aux rédacteurs d’effectuer des appels COM sortants dans d’autres processus VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-109">Therefore, VSS security settings must allow writers to make outgoing COM calls into other VSS processes.</span></span>

<span data-ttu-id="8a9ac-110">Le mécanisme le plus simple pour gérer les problèmes de sécurité de l’enregistreur implique la sélection appropriée du compte d’utilisateur sous lequel il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-110">The simplest mechanism for managing writer security issues involves the proper selection of the user account under which it runs.</span></span> <span data-ttu-id="8a9ac-111">Un enregistreur doit généralement s’exécuter sous un utilisateur membre du groupe administrateurs ou opérateurs de sauvegarde, ou il doit être exécuté en tant que compte système local.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-111">A writer typically needs to run under a user who is a member of either the Administrators group or the Backup Operators group, or it needs to run as the Local System account.</span></span>

<span data-ttu-id="8a9ac-112">Par défaut, lorsqu’un enregistreur agit en tant que client COM, s’il ne s’exécute pas sous ces comptes, tout appel COM qu’il effectue est automatiquement rejeté avec **E \_ ACCESSDENIED** sans même avoir à accéder à l’implémentation de la méthode com.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-112">By default, when a writer is acting as a COM client, if it does not run under these accounts, any COM call it makes is automatically rejected with **E\_ACCESSDENIED** without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="8a9ac-113">Désactivation de la gestion des exceptions COM</span><span class="sxs-lookup"><span data-stu-id="8a9ac-113">Disabling COM Exception Handling</span></span>

<span data-ttu-id="8a9ac-114">Lors du développement d’un enregistreur, définissez l' \_ exception com COMGLB exception \_ ne \_ gérer l’indicateur global options pour désactiver la gestion des exceptions com.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-114">When developing a writer, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="8a9ac-115">Il est important de le faire, car la gestion des exceptions COM peut masquer les erreurs irrécupérables dans une application VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-115">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="8a9ac-116">L’erreur masquée peut rendre le processus dans un état instable et imprévisible, ce qui peut entraîner des altérations et des blocages.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-116">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="8a9ac-117">Pour plus d’informations sur cet indicateur, consultez [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="8a9ac-117">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-writer-default-com-access-check-permission"></a><span data-ttu-id="8a9ac-118">Autorisation de vérification de l’accès COM par défaut du générateur de paramètres</span><span class="sxs-lookup"><span data-stu-id="8a9ac-118">Setting Writer Default COM Access Check Permission</span></span>

<span data-ttu-id="8a9ac-119">Les rédacteurs doivent savoir que lorsque leurs processus agissent comme un serveur (par exemple, pour gérer les événements VSS), ils doivent autoriser les appels entrants d’autres participants VSS, tels que les demandeurs ou le service VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-119">Writers need to be aware that when their processes act as a server (for example, to handle VSS events), they must allow incoming calls from other VSS participants, such as requesters or the VSS service.</span></span>

<span data-ttu-id="8a9ac-120">Toutefois, par défaut, un processus autorise uniquement les clients COM qui s’exécutent sous la même session de connexion (auto-SID) ou s’exécutant sous le compte système local.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-120">However, by default, a process will allow only COM clients that are running under the same logon session the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="8a9ac-121">Il s’agit d’un problème potentiel, car ces valeurs par défaut ne sont pas suffisantes pour prendre en charge l’infrastructure VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-121">This is a potential problem because these defaults are not sufficient to support the VSS infrastructure.</span></span> <span data-ttu-id="8a9ac-122">Par exemple, les demandeurs peuvent s’exécuter comme un compte d’utilisateur « opérateur de sauvegarde » qui n’est pas dans la même session de connexion que le processus d’écriture ou un compte système local.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-122">For example, requesters may run as a "Backup Operator" user account that is neither in the same logon session as the writer process nor a Local System account.</span></span>

<span data-ttu-id="8a9ac-123">Pour gérer ce type de problème, chaque processus serveur COM peut exercer un contrôle accru sur le fait qu’un client RPC ou COM est autorisé à exécuter une méthode COM que le serveur (un enregistreur dans ce cas) implémente à l’aide de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir une autorisation de vérification de l’accès com par défaut au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-123">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method the server (a writer in this case) implements by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide default COM access check permission.</span></span>

<span data-ttu-id="8a9ac-124">Les Writers peuvent explicitement effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a9ac-124">Writers can explicitly do the following:</span></span>

-   <span data-ttu-id="8a9ac-125">Autorisez l’accès de tous les processus à appeler le processus d’écriture.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-125">Allow all processes access to call into the writer process.</span></span>

    <span data-ttu-id="8a9ac-126">Cette option peut être adaptée à de nombreux enregistreurs et est utilisée par d’autres serveurs COM. par exemple, tous les services Windows basés sur SVCHOST utilisent déjà cette option, comme tous les services COM+ par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-126">This option may be adequate for many writers, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="8a9ac-127">Autoriser tous les processus à effectuer des appels COM entrants n’est pas nécessairement une faille de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-127">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="8a9ac-128">Un enregistreur agissant comme un serveur COM, comme tous les autres serveurs COM, conserve toujours la possibilité d’autoriser ses clients sur chaque méthode COM implémentée dans son processus.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-128">A writer acting as a COM server, like all other COM servers, always retains the option of authorizing its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="8a9ac-129">Pour permettre à tous les processus d’accéder à COM à un writer, vous pouvez passer un descripteur de sécurité **null** comme premier paramètre de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="8a9ac-129">To allow all processes COM access to a writer, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="8a9ac-130">(Notez que **CoInitializeSecurity** doit être appelé au plus une fois pour l’ensemble du processus.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="8a9ac-131">Pour plus d’informations sur la fonction **CoInitializeSecurity**, consultez la documentation com.)</span><span class="sxs-lookup"><span data-stu-id="8a9ac-131">Please see the COM documentation for more details on **CoInitializeSecurity**.)</span></span>

    <span data-ttu-id="8a9ac-132">Voici un exemple de code qui comprend un appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span><span class="sxs-lookup"><span data-stu-id="8a9ac-132">The following is a code example that includes a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span></span>

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    <span data-ttu-id="8a9ac-133">Lors de la définition explicite de la sécurité de niveau COM d’un writer avec [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a9ac-133">When explicitly setting a writer's COM-level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="8a9ac-134">Définissez le niveau d’authentification au moins **au \_ niveau de \_ \_ \_ connexion RPC C Authn**.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span>

        <span data-ttu-id="8a9ac-135">Pour une meilleure sécurité, envisagez d’utiliser la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C**.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

    -   <span data-ttu-id="8a9ac-136">Définissez le niveau d’emprunt d’identité sur **RPC \_ C \_ IMP \_ Level \_ identifier** , sauf si le processus de l’enregistreur doit autoriser l’emprunt d’identité pour des appels RPC ou com spécifiques qui ne sont pas liés à VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the writer process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="8a9ac-137">Autorise uniquement les processus spécifiés à accéder au processus d’écriture.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-137">Allow only specified processes access to call into the writer process.</span></span>

    <span data-ttu-id="8a9ac-138">Un serveur COM (tel qu’un enregistreur) qui appelle [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) avec un descripteur de sécurité non **null** peut utiliser le descripteur pour se configurer lui-même pour accepter des appels entrants uniquement à partir d’utilisateurs appartenant à un ensemble spécifique de comptes.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-138">A COM server (such as a writer) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="8a9ac-139">Un enregistreur doit s’assurer que les clients COM s’exécutant sous des utilisateurs valides sont autorisés à appeler son processus.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-139">A writer must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="8a9ac-140">Un enregistreur qui spécifie un descripteur de sécurité dans le premier paramètre doit autoriser les utilisateurs suivants à effectuer des appels entrants dans le processus du demandeur :</span><span class="sxs-lookup"><span data-stu-id="8a9ac-140">A writer that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="8a9ac-141">Système Local</span><span class="sxs-lookup"><span data-stu-id="8a9ac-141">Local System</span></span>
    -   <span data-ttu-id="8a9ac-142">Membres du groupe Administrateurs local</span><span class="sxs-lookup"><span data-stu-id="8a9ac-142">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="8a9ac-143">Membres du groupe opérateurs de sauvegarde local</span><span class="sxs-lookup"><span data-stu-id="8a9ac-143">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="8a9ac-144">Compte sous lequel le writer s’exécute</span><span class="sxs-lookup"><span data-stu-id="8a9ac-144">The account under which the writer is running</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a><span data-ttu-id="8a9ac-145">Contrôle explicite de l’accès d’un compte d’utilisateur à un enregistreur</span><span class="sxs-lookup"><span data-stu-id="8a9ac-145">Explicitly Controlling User Account Access to a Writer</span></span>

<span data-ttu-id="8a9ac-146">Dans certains cas, la restriction de l’accès à un enregistreur aux processus qui s’exécutent en tant que système local, ou sous les groupes locaux administrateurs locaux ou opérateurs de sauvegarde locaux, peut être trop restrictive.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-146">There are cases where restricting access to a writer to processes running as Local System, or under the local Administrators or local Backup Operators local groups, may be too restrictive.</span></span>

<span data-ttu-id="8a9ac-147">Par exemple, un processus d’écriture (peut-être un enregistreur tiers non-système) peut ne pas avoir besoin d’être exécuté sous un compte d’administrateur ou d’opérateur de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-147">For example, a writer process (perhaps a third-party non-system writer) might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="8a9ac-148">Pour des raisons de sécurité, il est préférable de ne pas promouvoir artificiellement les privilèges du processus pour prendre en charge VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-148">For security reasons, it would be best not to artificially promote the process's privileges to support VSS.</span></span>

<span data-ttu-id="8a9ac-149">Dans ce cas, vous devez modifier la clé de Registre HKEY VssAccessControl VSS de la clé de Registre **HKEY \_ local \_ machine** \\ **System** \\  \\  \\  \\  pour indiquer à VSS qu’un utilisateur spécifié peut exécuter un enregistreur VSS en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-149">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS writer.</span></span>

<span data-ttu-id="8a9ac-150">Sous cette clé, vous devez créer une sous-clé portant le même nom que le compte auquel l’accès doit être accordé ou refusé.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-150">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="8a9ac-151">Cette sous-clé doit être définie sur l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-151">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="8a9ac-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a9ac-152">Value</span></span> | <span data-ttu-id="8a9ac-153">Signification</span><span class="sxs-lookup"><span data-stu-id="8a9ac-153">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="8a9ac-154">0</span><span class="sxs-lookup"><span data-stu-id="8a9ac-154">0</span></span>     | <span data-ttu-id="8a9ac-155">Refusez à l’utilisateur l’accès à votre rédacteur et au demandeur.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-155">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="8a9ac-156">1</span><span class="sxs-lookup"><span data-stu-id="8a9ac-156">1</span></span>     | <span data-ttu-id="8a9ac-157">Accordez à l’utilisateur l’accès à votre rédacteur.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-157">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="8a9ac-158">2</span><span class="sxs-lookup"><span data-stu-id="8a9ac-158">2</span></span>     | <span data-ttu-id="8a9ac-159">Accordez à l’utilisateur l’accès à votre demandeur.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-159">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="8a9ac-160">3</span><span class="sxs-lookup"><span data-stu-id="8a9ac-160">3</span></span>     | <span data-ttu-id="8a9ac-161">Accordez à l’utilisateur l’accès à votre rédacteur et au demandeur.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-161">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="8a9ac-162">L’exemple suivant accorde l’accès au compte « MyDomain \\ myuser » :</span><span class="sxs-lookup"><span data-stu-id="8a9ac-162">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="8a9ac-163">Ce mécanisme peut également être utilisé pour empêcher explicitement un utilisateur autrement autorisé d’exécuter un enregistreur VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-163">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS writer.</span></span> <span data-ttu-id="8a9ac-164">L’exemple suivant permet de restreindre l’accès à partir du \\ compte « administrateur ThatDomain » :</span><span class="sxs-lookup"><span data-stu-id="8a9ac-164">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

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

<span data-ttu-id="8a9ac-165">L’administrateur ThatDomain de l’utilisateur \\ ne peut pas exécuter un enregistreur VSS.</span><span class="sxs-lookup"><span data-stu-id="8a9ac-165">The user ThatDomain\\Administrator would not be able to run a VSS writer.</span></span>

 

 
