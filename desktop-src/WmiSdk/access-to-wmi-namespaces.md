---
description: WMI utilise un descripteur de sécurité Windows standard pour contrôler l’accès aux espaces de noms WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Accès aux espaces de noms WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952869"
---
# <a name="access-to-wmi-namespaces"></a><span data-ttu-id="2a536-103">Accès aux espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="2a536-103">Access to WMI Namespaces</span></span>

<span data-ttu-id="2a536-104">WMI utilise un *descripteur de sécurité* Windows standard pour contrôler l’accès aux espaces de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="2a536-104">WMI uses a standard Windows *security descriptor* to control access to WMI namespaces.</span></span> <span data-ttu-id="2a536-105">Quand vous vous connectez à WMI, par le biais du moniker « winmgmts » WMI ou d’un appel à [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) ou [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), vous vous connectez à un espace de noms spécifique.</span><span class="sxs-lookup"><span data-stu-id="2a536-105">When you connect to WMI, either through the WMI "winmgmts" moniker or a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) or [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), you connect to a specific namespace.</span></span>

<span data-ttu-id="2a536-106">Les informations suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="2a536-106">The following information is discussed in this topic:</span></span>

-   [<span data-ttu-id="2a536-107">Sécurité de l’espace de noms WMI</span><span class="sxs-lookup"><span data-stu-id="2a536-107">WMI Namespace Security</span></span>](#wmi-namespace-security)
-   [<span data-ttu-id="2a536-108">Audit de l’espace de noms WMI</span><span class="sxs-lookup"><span data-stu-id="2a536-108">WMI Namespace Auditing</span></span>](#wmi-namespace-auditing)
-   [<span data-ttu-id="2a536-109">Types d’événements d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="2a536-109">Types of Namespace Events</span></span>](#types-of-namespace-events)
-   [<span data-ttu-id="2a536-110">Paramètres d’accès à l’espace de noms</span><span class="sxs-lookup"><span data-stu-id="2a536-110">Namespace Access Settings</span></span>](#namespace-access-settings)
-   [<span data-ttu-id="2a536-111">Autorisations par défaut sur les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="2a536-111">Default Permissions on WMI Namespaces</span></span>](#default-permissions-on-wmi-namespaces)
-   [<span data-ttu-id="2a536-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a536-112">Related topics</span></span>](#related-topics)

## <a name="wmi-namespace-security"></a><span data-ttu-id="2a536-113">Sécurité de l’espace de noms WMI</span><span class="sxs-lookup"><span data-stu-id="2a536-113">WMI Namespace Security</span></span>

<span data-ttu-id="2a536-114">WMI gère la sécurité des espaces de noms en comparant le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) de l’utilisateur qui se connecte à l’espace de noms avec le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2a536-114">WMI maintains namespace security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user connecting to the namespace with the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the namespace.</span></span> <span data-ttu-id="2a536-115">Pour plus d’informations sur la sécurité Windows, consultez [accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-115">For more information about Windows security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="2a536-116">Sachez que, à partir de Windows Vista, le [contrôle de compte d’utilisateur (UAC, User Account Control)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) affecte l’accès aux données WMI et ce qui peut être configuré avec le [*contrôle WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-116">Be aware that, starting with Windows Vista, [User Account Control (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="2a536-117">Pour plus d’informations, consultez [autorisations par défaut sur les espaces de noms WMI](#default-permissions-on-wmi-namespaces) et [le contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-117">For more information, see [Default Permissions on WMI Namespaces](#default-permissions-on-wmi-namespaces) and [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="2a536-118">L’accès aux espaces de noms WMI est également affecté lorsque la connexion provient d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="2a536-118">Access to WMI namespaces is also affected when the connection is from a remote computer.</span></span> <span data-ttu-id="2a536-119">Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md), [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md)et [connexion via le pare-feu Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="2a536-119">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md), [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md), and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span>

<span data-ttu-id="2a536-120">Les fournisseurs doivent s’appuyer sur le paramètre d’emprunt d’identité de la connexion pour déterminer si le script ou l’application cliente doit recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="2a536-120">Providers must rely on the impersonation setting for the connection to determine if the client script or application should receive data.</span></span> <span data-ttu-id="2a536-121">Pour plus d’informations sur les scripts et les applications clientes, consultez Définition de la [sécurité des processus d’application cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-121">For more information about script and client applications, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="2a536-122">Pour plus d’informations sur l’emprunt d’identité du [*fournisseur*](gloss-p.md) , consultez [développement d’un fournisseur WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-122">For more information about [*provider*](gloss-p.md) impersonation, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

## <a name="wmi-namespace-auditing"></a><span data-ttu-id="2a536-123">Audit de l’espace de noms WMI</span><span class="sxs-lookup"><span data-stu-id="2a536-123">WMI Namespace Auditing</span></span>

<span data-ttu-id="2a536-124">WMI utilise les [*listes de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) de l’espace de noms pour auditer l’activité de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2a536-124">WMI uses the namespace [*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) to audit namespace activity.</span></span> <span data-ttu-id="2a536-125">Pour activer l’audit des espaces de noms WMI, utilisez l’onglet **sécurité** du [*contrôle WMI*](gloss-w.md) pour modifier les paramètres d’audit de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2a536-125">To enable auditing of WMI namespaces, use the **Security** tab on the [*WMI Control*](gloss-w.md) to change the auditing settings for the namespace.</span></span>

<span data-ttu-id="2a536-126">L’audit n’est pas activé lors de l’installation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2a536-126">Auditing is not enabled during the installation of the operating system.</span></span> <span data-ttu-id="2a536-127">Pour activer l’audit, cliquez sur l’onglet **audit** dans la fenêtre **sécurité** standard.</span><span class="sxs-lookup"><span data-stu-id="2a536-127">To enable auditing, click the **Auditing** tab in the standard **Security** window.</span></span> <span data-ttu-id="2a536-128">Vous pouvez ensuite ajouter une entrée d’audit.</span><span class="sxs-lookup"><span data-stu-id="2a536-128">Then you can add an auditing entry.</span></span>

<span data-ttu-id="2a536-129">Stratégie de groupe de l’ordinateur local doit être défini pour autoriser l’audit.</span><span class="sxs-lookup"><span data-stu-id="2a536-129">Group Policy for the local computer must be set to allow auditing.</span></span> <span data-ttu-id="2a536-130">Vous pouvez activer l’audit en exécutant le composant logiciel enfichable MMC gpedit. msc et en définissant **audit Object Access** sous **Configuration ordinateur** paramètres Windows paramètres de  >    >  **sécurité**  >  **stratégies locales**  >  **stratégie d’audit**.</span><span class="sxs-lookup"><span data-stu-id="2a536-130">You can enable auditing by running the Gpedit.msc MMC snap-in and setting **Audit Object Access** under **Computer Configuration** > **Windows Settings** > **Security Settings** > **Local Policies** > **Audit Policy**.</span></span>

<span data-ttu-id="2a536-131">Une entrée d’audit modifie la liste SACL de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2a536-131">An auditing entry edits the SACL of the namespace.</span></span> <span data-ttu-id="2a536-132">Lorsque vous ajoutez une entrée d’audit, il s’agit d’un utilisateur, d’un groupe, d’un ordinateur ou d’un principal de sécurité intégré.</span><span class="sxs-lookup"><span data-stu-id="2a536-132">When you add an auditing entry, it is either a user, group, computer, or built-in security principal.</span></span> <span data-ttu-id="2a536-133">Après avoir ajouté l’entrée, vous pouvez définir les opérations d’accès qui entraînent des événements du journal de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2a536-133">After adding the entry, you can set the access operations that result in Security Log events.</span></span> <span data-ttu-id="2a536-134">Par exemple, pour les utilisateurs authentifiés de groupe, vous pouvez cliquer sur exécuter des méthodes.</span><span class="sxs-lookup"><span data-stu-id="2a536-134">For example, for the group Authenticated Users, you can click Execute Methods.</span></span> <span data-ttu-id="2a536-135">Ce paramètre génère des événements de journal de sécurité chaque fois qu’un membre du groupe utilisateurs authentifiés exécute une méthode dans cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2a536-135">This setting results in Security Log events whenever a member of the Authenticated Users group executes a method in that namespace.</span></span> <span data-ttu-id="2a536-136">L’ID d’événement pour les événements WMI est 4662.</span><span class="sxs-lookup"><span data-stu-id="2a536-136">The Event ID for WMI events is 4662.</span></span>

<span data-ttu-id="2a536-137">Votre compte doit être dans le groupe administrateurs et s’exécuter sous un privilège élevé pour modifier les paramètres d’audit.</span><span class="sxs-lookup"><span data-stu-id="2a536-137">Your account must be in the Administrators group and running under elevated privilege to change the auditing settings.</span></span> <span data-ttu-id="2a536-138">Le compte administrateur intégré peut également modifier la sécurité ou l’audit d’un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2a536-138">The built-in Administrator account can also change the security or auditing for a namespace.</span></span> <span data-ttu-id="2a536-139">Pour plus d’informations sur l’exécution en mode élevé, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-139">For more information about running in elevated mode, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="2a536-140">L’audit WMI génère des événements de réussite ou d’échec pour les tentatives d’accès aux espaces de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="2a536-140">WMI auditing generates success or failure events for attempts to access WMI namespaces.</span></span> <span data-ttu-id="2a536-141">Le service n’audite pas la réussite ou l’échec des opérations du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2a536-141">The service does not audit the success or failure of provider operations.</span></span> <span data-ttu-id="2a536-142">Par exemple, lorsqu’un script se connecte à WMI et à un espace de noms, il peut échouer, car le compte sous lequel le script s’exécute n’a pas accès à cet espace de noms ou peut tenter une opération, telle que la modification de la liste DACL, qui n’est pas accordée.</span><span class="sxs-lookup"><span data-stu-id="2a536-142">For example, when a script connects to WMI and a namespace, it may fail because the account under which the script is running does not have access to that the namespace or may attempt an operation, such as editing the DACL, that is not granted.</span></span>

<span data-ttu-id="2a536-143">Si vous exécutez sous un compte dans le groupe administrateurs, vous pouvez afficher les événements d’audit de l’espace de noms dans l’interface utilisateur **Observateur d’événements** .</span><span class="sxs-lookup"><span data-stu-id="2a536-143">If you are running under an account in the Administrators group, you can view the namespace auditing events in the **Event Viewer** user interface.</span></span>

## <a name="types-of-namespace-events"></a><span data-ttu-id="2a536-144">Types d’événements d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="2a536-144">Types of Namespace Events</span></span>

<span data-ttu-id="2a536-145">WMI effectue le suivi des types d’événements suivants dans le journal des événements de sécurité :</span><span class="sxs-lookup"><span data-stu-id="2a536-145">WMI traces the following types of events in the Security Event Log:</span></span>

-   <span data-ttu-id="2a536-146">Succès de l’audit</span><span class="sxs-lookup"><span data-stu-id="2a536-146">Audit Success</span></span>

    <span data-ttu-id="2a536-147">L’opération doit réussir deux étapes pour une réussite d’audit.</span><span class="sxs-lookup"><span data-stu-id="2a536-147">The operation must successfully complete two steps for an Audit Success.</span></span> <span data-ttu-id="2a536-148">Tout d’abord, WMI accorde l’accès à l’application cliente ou au script en fonction du SID du client et de la liste DACL des espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="2a536-148">First, WMI grants access to the client application or script based on the client SID and the namespace DACL.</span></span> <span data-ttu-id="2a536-149">Deuxièmement, l’opération demandée correspond aux droits d’accès dans la liste SACL d’espaces de noms pour cet utilisateur ou ce groupe.</span><span class="sxs-lookup"><span data-stu-id="2a536-149">Second, the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

-   <span data-ttu-id="2a536-150">Échec de l’audit</span><span class="sxs-lookup"><span data-stu-id="2a536-150">Audit Failure</span></span>

    <span data-ttu-id="2a536-151">WMI refuse l’accès à l’espace de noms, mais l’opération demandée correspond aux droits d’accès dans la liste SACL d’espaces de noms pour cet utilisateur ou ce groupe.</span><span class="sxs-lookup"><span data-stu-id="2a536-151">WMI denies access to the namespace, but the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

## <a name="namespace-access-settings"></a><span data-ttu-id="2a536-152">Paramètres d’accès à l’espace de noms</span><span class="sxs-lookup"><span data-stu-id="2a536-152">Namespace Access Settings</span></span>

<span data-ttu-id="2a536-153">Vous pouvez afficher les droits d’accès à l’espace de noms pour différents comptes sur le contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="2a536-153">You can view the namespace access rights for various accounts on the WMI Control.</span></span> <span data-ttu-id="2a536-154">Ces constantes sont décrites dans [**constantes de droits d’accès à l’espace de noms**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-154">These constants are described in [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span> <span data-ttu-id="2a536-155">Vous pouvez modifier l’accès à un espace de noms WMI à l’aide du contrôle WMI ou par programme.</span><span class="sxs-lookup"><span data-stu-id="2a536-155">You can change the access to a WMI namespace using the WMI Control or programmatically.</span></span> <span data-ttu-id="2a536-156">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-156">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="2a536-157">Les audits WMI changent dans toutes les autorisations d’accès répertoriées dans la liste suivante, à l’exception de l’autorisation Remote Enable.</span><span class="sxs-lookup"><span data-stu-id="2a536-157">WMI audits changes in all of the access permissions listed in the following list except for the Remote Enable permission.</span></span> <span data-ttu-id="2a536-158">Les modifications sont enregistrées en tant que succès ou échec de l’audit correspondant à l’autorisation Modifier la sécurité.</span><span class="sxs-lookup"><span data-stu-id="2a536-158">The changes are logged as audit success or failure corresponding to the Edit Security permission.</span></span>

<dl> <dt>

<span data-ttu-id="2a536-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Méthodes Execute</span><span class="sxs-lookup"><span data-stu-id="2a536-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Execute Methods</span></span>
</dt> <dd>

<span data-ttu-id="2a536-160">Permet à l’utilisateur d’exécuter des méthodes définies sur des classes WMI.</span><span class="sxs-lookup"><span data-stu-id="2a536-160">Permits the user to execute methods defined on WMI classes.</span></span> <span data-ttu-id="2a536-161">Correspond à la constante d’autorisation d’accès d' **\_ \_ exécution de la méthode WBEM** .</span><span class="sxs-lookup"><span data-stu-id="2a536-161">Corresponds to the **WBEM\_METHOD\_EXECUTE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="2a536-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Écriture complète</span><span class="sxs-lookup"><span data-stu-id="2a536-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Full Write</span></span>
</dt> <dd>

<span data-ttu-id="2a536-163">Autorise l’accès complet en lecture, écriture et suppression aux classes WMI et aux instances de classe, statiques et dynamiques.</span><span class="sxs-lookup"><span data-stu-id="2a536-163">Permits full read, write, and delete access to WMI classes and class instances, both static and dynamic.</span></span> <span data-ttu-id="2a536-164">Correspond à la constante d’autorisation d’accès au **\_ \_ REP Full Write \_ REP** .</span><span class="sxs-lookup"><span data-stu-id="2a536-164">Corresponds to the **WBEM\_FULL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="2a536-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Écriture partielle</span><span class="sxs-lookup"><span data-stu-id="2a536-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Partial Write</span></span>
</dt> <dd>

<span data-ttu-id="2a536-166">Autorise l’accès en écriture aux instances de classe WMI statiques.</span><span class="sxs-lookup"><span data-stu-id="2a536-166">Permits write access to static WMI class instances.</span></span> <span data-ttu-id="2a536-167">Correspond à la constante d’autorisation d’accès de la **\_ \_ \_ Représentation partielle WBEM** .</span><span class="sxs-lookup"><span data-stu-id="2a536-167">Corresponds to the **WBEM\_PARTIAL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="2a536-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Écriture du fournisseur</span><span class="sxs-lookup"><span data-stu-id="2a536-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Provider Write</span></span>
</dt> <dd>

<span data-ttu-id="2a536-169">Autorise l’accès en écriture aux instances de classe WMI dynamiques.</span><span class="sxs-lookup"><span data-stu-id="2a536-169">Permits write access to dynamic WMI class instances.</span></span> <span data-ttu-id="2a536-170">Correspond à la constante d’autorisation d’accès du **\_ \_ fournisseur d’écriture WBEM** .</span><span class="sxs-lookup"><span data-stu-id="2a536-170">Corresponds to the **WBEM\_WRITE\_PROVIDER** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="2a536-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Activer le compte</span><span class="sxs-lookup"><span data-stu-id="2a536-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Enable Account</span></span>
</dt> <dd>

<span data-ttu-id="2a536-172">Autorise l’accès en lecture aux instances de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="2a536-172">Permits read access to WMI class instances.</span></span> <span data-ttu-id="2a536-173">Correspond à la constante d’autorisation d’accès **WBEM \_ Enable** .</span><span class="sxs-lookup"><span data-stu-id="2a536-173">Corresponds to the **WBEM\_ENABLE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="2a536-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Activation à distance</span><span class="sxs-lookup"><span data-stu-id="2a536-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote Enable</span></span>
</dt> <dd>

<span data-ttu-id="2a536-175">Autorise l’accès à l’espace de noms par les ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="2a536-175">Permits access to the namespace by remote computers.</span></span> <span data-ttu-id="2a536-176">Correspond à la constante d’autorisation d’accès **\_ à \_ distance WBEM** .</span><span class="sxs-lookup"><span data-stu-id="2a536-176">Corresponds to the **WBEM\_REMOTE\_ACCESS** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="2a536-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Sécurité de lecture</span><span class="sxs-lookup"><span data-stu-id="2a536-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Read Security</span></span>
</dt> <dd>

<span data-ttu-id="2a536-178">Autorise l’accès en lecture seule aux paramètres DACL.</span><span class="sxs-lookup"><span data-stu-id="2a536-178">Permits read-only access to DACL settings.</span></span> <span data-ttu-id="2a536-179">Correspond à la constante d’autorisation d’accès au **\_ contrôle de lecture** .</span><span class="sxs-lookup"><span data-stu-id="2a536-179">Corresponds to the **READ\_CONTROL** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="2a536-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Modifier la sécurité</span><span class="sxs-lookup"><span data-stu-id="2a536-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Edit Security</span></span>
</dt> <dd>

<span data-ttu-id="2a536-181">Autorise l’accès en écriture aux paramètres DACL.</span><span class="sxs-lookup"><span data-stu-id="2a536-181">Permits write access to DACL settings.</span></span> <span data-ttu-id="2a536-182">Correspond à la constante d’autorisation **Write \_ DAC** Access.</span><span class="sxs-lookup"><span data-stu-id="2a536-182">Corresponds to the **WRITE\_DAC** access permission constant.</span></span>

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a><span data-ttu-id="2a536-183">Autorisations par défaut sur les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="2a536-183">Default Permissions on WMI Namespaces</span></span>

<span data-ttu-id="2a536-184">Les groupes de sécurité par défaut sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2a536-184">The default security groups are:</span></span>

-   <span data-ttu-id="2a536-185">Utilisateurs authentifiés</span><span class="sxs-lookup"><span data-stu-id="2a536-185">Authenticated Users</span></span>
-   <span data-ttu-id="2a536-186">SERVICE LOCAL</span><span class="sxs-lookup"><span data-stu-id="2a536-186">LOCAL SERVICE</span></span>
-   <span data-ttu-id="2a536-187">SERVICE RÉSEAU</span><span class="sxs-lookup"><span data-stu-id="2a536-187">NETWORK SERVICE</span></span>
-   <span data-ttu-id="2a536-188">Administrateurs (sur l’ordinateur local)</span><span class="sxs-lookup"><span data-stu-id="2a536-188">Administrators (on the local computer)</span></span>

<span data-ttu-id="2a536-189">Les autorisations d’accès par défaut pour les utilisateurs authentifiés, le SERVICE LOCAL et le SERVICE réseau sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a536-189">The default access permissions for the Authenticated Users, LOCAL SERVICE, and NETWORK SERVICE are:</span></span>

-   <span data-ttu-id="2a536-190">Méthodes d’exécution</span><span class="sxs-lookup"><span data-stu-id="2a536-190">Execute Methods</span></span>
-   <span data-ttu-id="2a536-191">Écriture complète</span><span class="sxs-lookup"><span data-stu-id="2a536-191">Full Write</span></span>
-   <span data-ttu-id="2a536-192">Activer le compte</span><span class="sxs-lookup"><span data-stu-id="2a536-192">Enable Account</span></span>

<span data-ttu-id="2a536-193">Les comptes du groupe administrateurs disposent de tous les droits nécessaires, y compris la modification des descripteurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2a536-193">Accounts in the Administrators group have all rights available to them, including editing security descriptors.</span></span> <span data-ttu-id="2a536-194">Toutefois, en raison du contrôle de compte d’utilisateur (UAC), le contrôle WMI ou le script doit s’exécuter avec un niveau de sécurité élevé.</span><span class="sxs-lookup"><span data-stu-id="2a536-194">However, because of User Account Control (UAC), the WMI Control or the script must be running at elevated security.</span></span> <span data-ttu-id="2a536-195">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-195">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="2a536-196">Parfois, un script ou une application doit activer un privilège d’administrateur, tel que **SeSecurityPrivilege**, pour effectuer une opération.</span><span class="sxs-lookup"><span data-stu-id="2a536-196">Sometimes a script or application must enable an administrator privilege, such as **SeSecurityPrivilege**, to carry out an operation.</span></span> <span data-ttu-id="2a536-197">Par exemple, un script peut exécuter la méthode [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) de la [**classe Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) sans **SeSecurityPrivilege** et obtenir les informations de sécurité dans la liste de contrôle d' [*accès discrétionnaire (DACL, Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)de l’objet Printer.</span><span class="sxs-lookup"><span data-stu-id="2a536-197">For example, a script can execute the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class without **SeSecurityPrivilege** and get the security information in the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) of the printer object [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="2a536-198">Toutefois, les informations SACL ne sont pas renvoyées au script, sauf si le privilège **SeSecurityPrivilege** est disponible et activé pour le compte.</span><span class="sxs-lookup"><span data-stu-id="2a536-198">However, the SACL information is not returned to the script unless the **SeSecurityPrivilege** privilege is available and enabled for the account.</span></span> <span data-ttu-id="2a536-199">Si le compte ne dispose pas du privilège disponible, il ne peut pas être activé.</span><span class="sxs-lookup"><span data-stu-id="2a536-199">If the account does not have the privilege available, then it cannot be enabled.</span></span> <span data-ttu-id="2a536-200">Pour plus d’informations, consultez [exécution d’opérations privilégiées](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="2a536-200">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a536-201">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a536-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a536-202">À propos de WMI</span><span class="sxs-lookup"><span data-stu-id="2a536-202">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
