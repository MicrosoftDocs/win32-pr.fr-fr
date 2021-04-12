---
title: Access Control (plateforme de filtrage Windows)
description: Dans la plateforme de filtrage Windows (WFP), le service de moteur de filtrage de base (BFE) implémente le modèle de contrôle d’accès Windows standard basé sur les jetons d’accès et les descripteurs de sécurité.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104321370"
---
# <a name="access-control-windows-filtering-platform"></a><span data-ttu-id="47e8b-103">Access Control (plateforme de filtrage Windows)</span><span class="sxs-lookup"><span data-stu-id="47e8b-103">Access Control (Windows Filtering Platform)</span></span>

<span data-ttu-id="47e8b-104">Dans la plateforme de filtrage Windows (WFP), le service de moteur de filtrage de base (BFE) implémente le [modèle de contrôle d’accès Windows](/windows/desktop/SecAuthZ/access-control-model) standard basé sur les jetons d’accès et les descripteurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="47e8b-104">In Windows Filtering Platform (WFP), the Base Filtering Engine (BFE) service implements the standard [Windows access control model](/windows/desktop/SecAuthZ/access-control-model) based on access tokens and security descriptors.</span></span>

## <a name="access-control-model"></a><span data-ttu-id="47e8b-105">Modèle de Access Control</span><span class="sxs-lookup"><span data-stu-id="47e8b-105">Access Control Model</span></span>

<span data-ttu-id="47e8b-106">Des descripteurs de sécurité peuvent être spécifiés lors de l’ajout de nouveaux objets WFP, tels que des filtres et des sous-couches.</span><span class="sxs-lookup"><span data-stu-id="47e8b-106">Security descriptors can be specified when adding new WFP objects, such as filters and sub-layers.</span></span> <span data-ttu-id="47e8b-107">Les descripteurs de sécurité sont gérés à l’aide des fonctions de gestion WFP **Fwpm \* GetSecurityInfo0** et **Fwpm \* SetSecurityInfo0**, où \* *\** _ correspond au nom de l’objet WFP.</span><span class="sxs-lookup"><span data-stu-id="47e8b-107">Security descriptors are managed using the WFP management functions **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0**, where \**\** _ stands for the WFP object's name.</span></span> <span data-ttu-id="47e8b-108">Ces fonctions sont sémantiquement identiques aux fonctions Windows [_ *GetSecurityInfo* \*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) et [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="47e8b-108">These functions are semantically identical to the Windows [_ *GetSecurityInfo*\*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

> [!Note]  
> <span data-ttu-id="47e8b-109">Les fonctions **Fwpm \* SetSecurityInfo0** ne peuvent pas être appelées à partir d’une transaction explicite.</span><span class="sxs-lookup"><span data-stu-id="47e8b-109">The **Fwpm\*SetSecurityInfo0** functions cannot be called from within an explicit transaction.</span></span>

 

> [!Note]  
> <span data-ttu-id="47e8b-110">Les **fonctions \* SetSecurityInfo0 Fwpm** peuvent uniquement être appelées à partir d’une session dynamique s’ils sont utilisés pour gérer un objet dynamique créé au cours de la même session.</span><span class="sxs-lookup"><span data-stu-id="47e8b-110">The **Fwpm\*SetSecurityInfo0** functions can only be called from within a dynamic session if they are being used to manage a dynamic object created within the same session.</span></span>

 

<span data-ttu-id="47e8b-111">Le descripteur de sécurité par défaut pour le moteur de filtre (l’objet moteur racine dans le diagramme ci-dessous) est le suivant.</span><span class="sxs-lookup"><span data-stu-id="47e8b-111">The default security descriptor for the filter engine (the root Engine object in the diagram below) is as follows.</span></span>

-   <span data-ttu-id="47e8b-112">Accordez des droits d’accès **génériques \_ tous** (GA) au groupe Administrateurs intégré.</span><span class="sxs-lookup"><span data-stu-id="47e8b-112">Grant **GENERIC\_ALL** (GA) access rights to the built-in Administrators group.</span></span>
-   <span data-ttu-id="47e8b-113">Octroie des droits d’accès génériques **\_ en** **\_ écriture** générique ( **EG \_** ) aux opérateurs de configuration de réseau.</span><span class="sxs-lookup"><span data-stu-id="47e8b-113">Grant **GENERIC\_READ** (GR) **GENERIC\_WRITE** (GW) **GENERIC\_EXECUTE** (GX) access rights to network configuration operators.</span></span>
-   <span data-ttu-id="47e8b-114">Accordez des droits d’accès **GRGWGX** aux identificateurs de sécurité de service (SSID) suivants : mpssvc (pare-feu Windows), NapAgent (agent de protection d’accès réseau), policyagent (agent de stratégie IPSec), RPCSS (appel de procédure distante) et WdiServiceHost (hôte de service de diagnostic).</span><span class="sxs-lookup"><span data-stu-id="47e8b-114">Grant **GRGWGX** access rights to the following service security identifiers (SSIDs): MpsSvc (Windows Firewall), NapAgent (Network Access Protection Agent), PolicyAgent (IPsec Policy Agent), RpcSs (Remote Procedure Call), and WdiServiceHost (Diagnostic Service Host).</span></span>
-   <span data-ttu-id="47e8b-115">Accordez la classification **FWPM \_ ACTRL \_ Open** et **FWPM \_ ACTRL \_** à tout le monde.</span><span class="sxs-lookup"><span data-stu-id="47e8b-115">Grant **FWPM\_ACTRL\_OPEN** and **FWPM\_ACTRL\_CLASSIFY** to everyone.</span></span> <span data-ttu-id="47e8b-116">(Il s’agit de droits d’accès spécifiques à WFP, décrits dans le tableau ci-dessous.)</span><span class="sxs-lookup"><span data-stu-id="47e8b-116">(These are WFP-specific access rights, described in table below.)</span></span>

<span data-ttu-id="47e8b-117">Les descripteurs de sécurité par défaut restants sont dérivés de l’héritage.</span><span class="sxs-lookup"><span data-stu-id="47e8b-117">The remaining default security descriptors are derived through inheritance.</span></span>

<span data-ttu-id="47e8b-118">Certains contrôles d’accès, par exemple, pour les appels de fonction **Fwpm \* Add0**, **Fwpm \* CreateEnumHandle0**, **Fwpm \* SubscribeChanges0** , ne peuvent pas être effectués au niveau de l’objet individuel.</span><span class="sxs-lookup"><span data-stu-id="47e8b-118">There are some access checks, such as for **Fwpm\*Add0**, **Fwpm\*CreateEnumHandle0**, **Fwpm\*SubscribeChanges0** function calls, that cannot be done at the individual object level.</span></span> <span data-ttu-id="47e8b-119">Pour ces fonctions, il existe des objets conteneurs pour chaque type d’objet.</span><span class="sxs-lookup"><span data-stu-id="47e8b-119">For these functions, there are container objects for each object type.</span></span> <span data-ttu-id="47e8b-120">Pour les types d’objet standard (par exemple, fournisseurs, légendes, filtres), les fonctions **Fwpm \* GetSecurityInfo0** et **Fwpm \* SetSecurityInfo0** existantes sont surchargées, de sorte qu’un paramètre **GUID** null identifie le conteneur associé.</span><span class="sxs-lookup"><span data-stu-id="47e8b-120">For the standard object types (for example, providers, callouts, filters), the existing **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0** functions are overloaded, such that a null **GUID** parameter identifies the associated container.</span></span> <span data-ttu-id="47e8b-121">Pour les autres types d’objets (par exemple, les événements réseau et les associations de sécurité IPsec), il existe des fonctions explicites pour la gestion des informations de sécurité du conteneur.</span><span class="sxs-lookup"><span data-stu-id="47e8b-121">For the other object types (for example, network events and IPsec security associations), there are explicit functions for managing the container's security information.</span></span>

<span data-ttu-id="47e8b-122">BFE prend en charge l’héritage automatique des entrées de contrôle d’accès (DACL) de liste de Access Control discrétionnaire.</span><span class="sxs-lookup"><span data-stu-id="47e8b-122">BFE supports automatic inheritance of Discretionary Access Control List (DACL) access control entries (ACEs).</span></span> <span data-ttu-id="47e8b-123">BFE ne prend pas en charge les ACE du système Access Control List (SACL).</span><span class="sxs-lookup"><span data-stu-id="47e8b-123">BFE does not support System Access Control List (SACL) ACEs.</span></span> <span data-ttu-id="47e8b-124">Les objets héritent des ACE de leur conteneur.</span><span class="sxs-lookup"><span data-stu-id="47e8b-124">Objects inherit ACEs from their container.</span></span> <span data-ttu-id="47e8b-125">Les conteneurs héritent des ACE du moteur de filtre.</span><span class="sxs-lookup"><span data-stu-id="47e8b-125">Containers inherit ACEs from the filter engine.</span></span> <span data-ttu-id="47e8b-126">Les chemins de propagation sont indiqués dans le diagramme ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="47e8b-126">The propagation paths are shown in the diagram below.</span></span>

![Diagramme qui affiche les chemins d’accès de propagation de l’ACE, commençant par’Engine'.](images/access-control.jpg)

<span data-ttu-id="47e8b-128">Pour les types d’objet standard, BFE applique tous les droits d’accès génériques et standard.</span><span class="sxs-lookup"><span data-stu-id="47e8b-128">For the standard object types, BFE enforces all the generic and standard access rights.</span></span> <span data-ttu-id="47e8b-129">De plus, WFP définit les droits d’accès spécifiques suivants.</span><span class="sxs-lookup"><span data-stu-id="47e8b-129">In addition, WFP defines the following specific access rights.</span></span>



| <span data-ttu-id="47e8b-130">Droit d’accès à WFP</span><span class="sxs-lookup"><span data-stu-id="47e8b-130">WFP Access Right</span></span>                                                                                                                        | <span data-ttu-id="47e8b-131">Description</span><span class="sxs-lookup"><span data-stu-id="47e8b-131">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e8b-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**</span><span class="sxs-lookup"><span data-stu-id="47e8b-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span><br/>                                       | <span data-ttu-id="47e8b-133">Obligatoire pour ajouter un objet à un conteneur.</span><span class="sxs-lookup"><span data-stu-id="47e8b-133">Required to add an object to a container.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="47e8b-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Ajouter un \_ lien**</span><span class="sxs-lookup"><span data-stu-id="47e8b-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>                       | <span data-ttu-id="47e8b-135">Requis pour créer une association à un objet.</span><span class="sxs-lookup"><span data-stu-id="47e8b-135">Required to create an association to an object.</span></span> <span data-ttu-id="47e8b-136">Par exemple, pour ajouter un filtre qui fait référence à une légende, l’appelant doit disposer d’un lien ajouter un \_ accès à la légende.</span><span class="sxs-lookup"><span data-stu-id="47e8b-136">For example, to add a filter that references a callout, the caller must have ADD\_LINK access to the callout.</span></span><br/> |
| <span data-ttu-id="47e8b-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="47e8b-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span><br/>    | <span data-ttu-id="47e8b-138">Requis pour commencer une transaction de lecture explicite.</span><span class="sxs-lookup"><span data-stu-id="47e8b-138">Required to begin an explicit read transaction.</span></span><br/>                                                                                                               |
| <span data-ttu-id="47e8b-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="47e8b-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span><br/> | <span data-ttu-id="47e8b-140">Requis pour commencer une transaction d’écriture explicite.</span><span class="sxs-lookup"><span data-stu-id="47e8b-140">Required to begin an explicit write transaction.</span></span><br/>                                                                                                              |
| <span data-ttu-id="47e8b-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_classification FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="47e8b-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span><br/>                        | <span data-ttu-id="47e8b-142">Requis pour classer par rapport à une couche en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="47e8b-142">Required to classify against a user-mode layer.</span></span><br/>                                                                                                               |
| <span data-ttu-id="47e8b-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL, \_ énumération**</span><span class="sxs-lookup"><span data-stu-id="47e8b-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span><br/>                                    | <span data-ttu-id="47e8b-144">Requis pour énumérer les objets dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="47e8b-144">Required to enumerate the objects in a container.</span></span> <span data-ttu-id="47e8b-145">Toutefois, l’énumérateur retourne uniquement les objets auxquels l’appelant a \_ \_ accès en lecture FWPM ACTRL.</span><span class="sxs-lookup"><span data-stu-id="47e8b-145">However, the enumerator only returns objects to which the caller has FWPM\_ACTRL\_READ access.</span></span><br/>              |
| <span data-ttu-id="47e8b-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**</span><span class="sxs-lookup"><span data-stu-id="47e8b-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span><br/>                                    | <span data-ttu-id="47e8b-147">Requis pour ouvrir une session avec BFE.</span><span class="sxs-lookup"><span data-stu-id="47e8b-147">Required to open a session with BFE.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="47e8b-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="47e8b-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span><br/>                                    | <span data-ttu-id="47e8b-149">Requis pour lire les propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="47e8b-149">Required to read an object's properties.</span></span><br/>                                                                                                                      |
| <span data-ttu-id="47e8b-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_statistiques de \_ lecture FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="47e8b-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span><br/>                 | <span data-ttu-id="47e8b-151">Requis pour lire les statistiques.</span><span class="sxs-lookup"><span data-stu-id="47e8b-151">Required to read statistics.</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="47e8b-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**abonnement à FWPM \_ ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="47e8b-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span><br/>                     | <span data-ttu-id="47e8b-153">Requis pour s’abonner aux notifications.</span><span class="sxs-lookup"><span data-stu-id="47e8b-153">Required to subscribe for notifications.</span></span> <span data-ttu-id="47e8b-154">Les abonnés reçoivent uniquement des notifications pour les objets auxquels ils disposent d’un \_ \_ accès en lecture FWPM ACTRL.</span><span class="sxs-lookup"><span data-stu-id="47e8b-154">Subscribers will only receive notifications for objects to which they have FWPM\_ACTRL\_READ access.</span></span><br/>                 |
| <span data-ttu-id="47e8b-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**</span><span class="sxs-lookup"><span data-stu-id="47e8b-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span><br/>                                 | <span data-ttu-id="47e8b-156">Requis pour définir les options du moteur.</span><span class="sxs-lookup"><span data-stu-id="47e8b-156">Required to set engine options.</span></span><br/>                                                                                                                               |



 

<span data-ttu-id="47e8b-157">BFE ignore toutes les vérifications d’accès pour les appelants en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="47e8b-157">BFE skips all access checks for kernel-mode callers.</span></span>

<span data-ttu-id="47e8b-158">Pour empêcher les administrateurs de se verrouiller eux-mêmes, les membres du groupe Administrateurs intégré bénéficient toujours de l’autorisation **FWPM \_ ACTRL \_ Open** sur l’objet moteur.</span><span class="sxs-lookup"><span data-stu-id="47e8b-158">In order to prevent administrators from locking themselves out of BFE, members of the built-in administrators group are always granted **FWPM\_ACTRL\_OPEN** to the engine object.</span></span> <span data-ttu-id="47e8b-159">Ainsi, un administrateur peut récupérer l’accès en suivant les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="47e8b-159">Thus, an administrator can regain access through the following steps.</span></span>

-   <span data-ttu-id="47e8b-160">Activez le privilège **se \_ prendre possession du \_ \_ nom** .</span><span class="sxs-lookup"><span data-stu-id="47e8b-160">Enable the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="47e8b-161">Appelez [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="47e8b-161">Call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span> <span data-ttu-id="47e8b-162">L’appel a lieu car l’appelant est membre des administrateurs intégrés.</span><span class="sxs-lookup"><span data-stu-id="47e8b-162">The call succeeds because the caller is a member of Built-in Administrators.</span></span>
-   <span data-ttu-id="47e8b-163">Prendre possession de l’objet moteur.</span><span class="sxs-lookup"><span data-stu-id="47e8b-163">Take ownership of the engine object.</span></span> <span data-ttu-id="47e8b-164">Cela est dû au fait que l’appelant a le privilège **se \_ prendre \_ possession du \_ nom** .</span><span class="sxs-lookup"><span data-stu-id="47e8b-164">This succeeds because the caller has the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="47e8b-165">Mettez à jour la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="47e8b-165">Update the DACL.</span></span> <span data-ttu-id="47e8b-166">Cela est dû au fait que le propriétaire a toujours un accès en écriture à la **\_ DAC**</span><span class="sxs-lookup"><span data-stu-id="47e8b-166">This succeeds because the owner always has **WRITE\_DAC** access</span></span>

<span data-ttu-id="47e8b-167">Dans la mesure où BFE prend en charge son propre audit personnalisé, il ne génère pas d’audits d’accès aux objets génériques.</span><span class="sxs-lookup"><span data-stu-id="47e8b-167">Since BFE supports its own custom auditing, it does not generate generic object access audits.</span></span> <span data-ttu-id="47e8b-168">Par conséquent, la liste SACL est ignorée.</span><span class="sxs-lookup"><span data-stu-id="47e8b-168">Thus, the SACL is ignored.</span></span>

## <a name="wfp-required-access-rights"></a><span data-ttu-id="47e8b-169">Droits d’accès requis pour WFP</span><span class="sxs-lookup"><span data-stu-id="47e8b-169">WFP Required Access Rights</span></span>

<span data-ttu-id="47e8b-170">Le tableau ci-dessous montre les droits d’accès requis par les fonctions WFP pour accéder à différents objets de plateforme de filtrage.</span><span class="sxs-lookup"><span data-stu-id="47e8b-170">The table below shows the access rights required by the WFP functions in order to access various filtering platform objects.</span></span> <span data-ttu-id="47e8b-171">Les **\* *fonctions FwpmFilter _ sont répertoriées comme exemple pour accéder aux objets standard. Toutes les autres fonctions qui accèdent aux objets standard suivent le* \*** modèle d’accès aux fonctions _ FwpmFilter.</span><span class="sxs-lookup"><span data-stu-id="47e8b-171">The **FwpmFilter\**_ functions are listed as an example for accessing the standard objects. All the other functions that access standard objects follow the _\* FwpmFilter\**\* functions access model.</span></span>



<span data-ttu-id="47e8b-172">Fonction</span><span class="sxs-lookup"><span data-stu-id="47e8b-172">Function</span></span>

<span data-ttu-id="47e8b-173">Objet vérifié</span><span class="sxs-lookup"><span data-stu-id="47e8b-173">Object Checked</span></span>

<span data-ttu-id="47e8b-174">Accès obligatoire</span><span class="sxs-lookup"><span data-stu-id="47e8b-174">Access Required</span></span>

[<span data-ttu-id="47e8b-175">**FwpmEngineOpen0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-175">**FwpmEngineOpen0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

<span data-ttu-id="47e8b-176">Moteur</span><span class="sxs-lookup"><span data-stu-id="47e8b-176">Engine</span></span>

<span data-ttu-id="47e8b-177">**FWPM \_ ACTRL \_ Open**</span><span class="sxs-lookup"><span data-stu-id="47e8b-177">**FWPM\_ACTRL\_OPEN**</span></span>

[<span data-ttu-id="47e8b-178">**FwpmEngineGetOption0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-178">**FwpmEngineGetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

<span data-ttu-id="47e8b-179">Moteur</span><span class="sxs-lookup"><span data-stu-id="47e8b-179">Engine</span></span>

<span data-ttu-id="47e8b-180">**FWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="47e8b-180">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="47e8b-181">**FwpmEngineSetOption0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-181">**FwpmEngineSetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

<span data-ttu-id="47e8b-182">Moteur</span><span class="sxs-lookup"><span data-stu-id="47e8b-182">Engine</span></span>

<span data-ttu-id="47e8b-183">**FWPM \_ ACTRL \_ Write**</span><span class="sxs-lookup"><span data-stu-id="47e8b-183">**FWPM\_ACTRL\_WRITE**</span></span>

[<span data-ttu-id="47e8b-184">**FwpmSessionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-184">**FwpmSessionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

<span data-ttu-id="47e8b-185">Moteur</span><span class="sxs-lookup"><span data-stu-id="47e8b-185">Engine</span></span>

<span data-ttu-id="47e8b-186">**FWPM \_ ACTRL, \_ énumération**</span><span class="sxs-lookup"><span data-stu-id="47e8b-186">**FWPM\_ACTRL\_ENUM**</span></span>

[<span data-ttu-id="47e8b-187">**FwpmTransactionBegin0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-187">**FwpmTransactionBegin0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

<span data-ttu-id="47e8b-188">Moteur</span><span class="sxs-lookup"><span data-stu-id="47e8b-188">Engine</span></span>

<span data-ttu-id="47e8b-189">**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**  &  **FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="47e8b-189">**FWPM\_ACTRL\_BEGIN\_READ\_TXN** & **FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>

[<span data-ttu-id="47e8b-190">**FwpmFilterAdd0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-190">**FwpmFilterAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

<span data-ttu-id="47e8b-191">Fournisseur de conteneurs</span><span class="sxs-lookup"><span data-stu-id="47e8b-191">Container Provider</span></span><br/> <span data-ttu-id="47e8b-192">Couche</span><span class="sxs-lookup"><span data-stu-id="47e8b-192">Layer</span></span><br/> <span data-ttu-id="47e8b-193">Sub-Layer</span><span class="sxs-lookup"><span data-stu-id="47e8b-193">Sub-Layer</span></span><br/> <span data-ttu-id="47e8b-194">Légende</span><span class="sxs-lookup"><span data-stu-id="47e8b-194">Callout</span></span><br/> <span data-ttu-id="47e8b-195">Contexte du fournisseur</span><span class="sxs-lookup"><span data-stu-id="47e8b-195">Provider Context</span></span><br/>

<span data-ttu-id="47e8b-196">**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ Ajouter un \_ lien**</span><span class="sxs-lookup"><span data-stu-id="47e8b-196">**FWPM\_ACTRL\_ADDFWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="47e8b-197">**FWPM \_ ACTRL \_ Ajouter un \_ lien**</span><span class="sxs-lookup"><span data-stu-id="47e8b-197">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="47e8b-198">**FWPM \_ ACTRL \_ Ajouter un \_ lien**</span><span class="sxs-lookup"><span data-stu-id="47e8b-198">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="47e8b-199">**FWPM \_ ACTRL \_ Ajouter un \_ lien**</span><span class="sxs-lookup"><span data-stu-id="47e8b-199">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="47e8b-200">**FWPM \_ ACTRL \_ Ajouter un \_ lien**</span><span class="sxs-lookup"><span data-stu-id="47e8b-200">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>

<span data-ttu-id="47e8b-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="47e8b-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span></span><br/>

<span data-ttu-id="47e8b-202">Filtrer</span><span class="sxs-lookup"><span data-stu-id="47e8b-202">Filter</span></span>

<span data-ttu-id="47e8b-203">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="47e8b-203">**DELETE**</span></span>

<span data-ttu-id="47e8b-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span><span class="sxs-lookup"><span data-stu-id="47e8b-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span></span><br/>

<span data-ttu-id="47e8b-205">Filtrer</span><span class="sxs-lookup"><span data-stu-id="47e8b-205">Filter</span></span>

<span data-ttu-id="47e8b-206">**FWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="47e8b-206">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="47e8b-207">**FwpmFilterCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-207">**FwpmFilterCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

<span data-ttu-id="47e8b-208">Filtre de conteneur</span><span class="sxs-lookup"><span data-stu-id="47e8b-208">Container Filter</span></span><br/>

<span data-ttu-id="47e8b-209">**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="47e8b-209">**FWPM\_ACTRL\_ENUMFWPM\_ACTRL\_READ**</span></span><br/>

[<span data-ttu-id="47e8b-210">**FwpmFilterSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-210">**FwpmFilterSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

<span data-ttu-id="47e8b-211">Conteneur</span><span class="sxs-lookup"><span data-stu-id="47e8b-211">Container</span></span>

<span data-ttu-id="47e8b-212">**abonnement à FWPM \_ ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="47e8b-212">**FWPM\_ACTRL\_SUBSCRIBE**</span></span>

[<span data-ttu-id="47e8b-213">**FwpmFilterSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-213">**FwpmFilterSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

<span data-ttu-id="47e8b-214">Conteneur</span><span class="sxs-lookup"><span data-stu-id="47e8b-214">Container</span></span>

<span data-ttu-id="47e8b-215">**FWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="47e8b-215">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="47e8b-216">**IPsecGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-216">**IPsecGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

<span data-ttu-id="47e8b-217">BD IPsec SA</span><span class="sxs-lookup"><span data-stu-id="47e8b-217">IPsec SA DB</span></span>

<span data-ttu-id="47e8b-218">**\_statistiques de \_ lecture FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="47e8b-218">**FWPM\_ACTRL\_READ\_STATS**</span></span>

<span data-ttu-id="47e8b-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span><span class="sxs-lookup"><span data-stu-id="47e8b-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span></span><br/> [<span data-ttu-id="47e8b-220">**IPsecSaContextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-220">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [<span data-ttu-id="47e8b-221">**IPsecSaContextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-221">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

<span data-ttu-id="47e8b-222">BD IPsec SA</span><span class="sxs-lookup"><span data-stu-id="47e8b-222">IPsec SA DB</span></span>

<span data-ttu-id="47e8b-223">**FWPM \_ ACTRL \_ Add**</span><span class="sxs-lookup"><span data-stu-id="47e8b-223">**FWPM\_ACTRL\_ADD**</span></span>

<span data-ttu-id="47e8b-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span><span class="sxs-lookup"><span data-stu-id="47e8b-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span></span><br/>

<span data-ttu-id="47e8b-225">BD IPsec SA</span><span class="sxs-lookup"><span data-stu-id="47e8b-225">IPsec SA DB</span></span>

<span data-ttu-id="47e8b-226">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="47e8b-226">**DELETE**</span></span>

[<span data-ttu-id="47e8b-227">**IPsecSaContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-227">**IPsecSaContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

<span data-ttu-id="47e8b-228">BD IPsec SA</span><span class="sxs-lookup"><span data-stu-id="47e8b-228">IPsec SA DB</span></span>

<span data-ttu-id="47e8b-229">**FWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="47e8b-229">**FWPM\_ACTRL\_READ**</span></span>

<span data-ttu-id="47e8b-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span><span class="sxs-lookup"><span data-stu-id="47e8b-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span></span><br/>

<span data-ttu-id="47e8b-231">BD IPsec SA</span><span class="sxs-lookup"><span data-stu-id="47e8b-231">IPsec SA DB</span></span>

<span data-ttu-id="47e8b-232">**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="47e8b-232">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="47e8b-233">**IkeextGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-233">**IkeextGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

<span data-ttu-id="47e8b-234">BD IKE SA</span><span class="sxs-lookup"><span data-stu-id="47e8b-234">IKE SA DB</span></span>

<span data-ttu-id="47e8b-235">**\_statistiques de \_ lecture FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="47e8b-235">**FWPM\_ACTRL\_READ\_STATS**</span></span>

[<span data-ttu-id="47e8b-236">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-236">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

<span data-ttu-id="47e8b-237">BD IKE SA</span><span class="sxs-lookup"><span data-stu-id="47e8b-237">IKE SA DB</span></span>

<span data-ttu-id="47e8b-238">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="47e8b-238">**DELETE**</span></span>

[<span data-ttu-id="47e8b-239">**IkeextSaGetById0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-239">**IkeextSaGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

<span data-ttu-id="47e8b-240">BD IKE SA</span><span class="sxs-lookup"><span data-stu-id="47e8b-240">IKE SA DB</span></span>

<span data-ttu-id="47e8b-241">**FWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="47e8b-241">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="47e8b-242">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-242">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

<span data-ttu-id="47e8b-243">BD IKE SA</span><span class="sxs-lookup"><span data-stu-id="47e8b-243">IKE SA DB</span></span>

<span data-ttu-id="47e8b-244">**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="47e8b-244">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="47e8b-245">**FwpmNetEventCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="47e8b-245">**FwpmNetEventCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

<span data-ttu-id="47e8b-246">Conteneur</span><span class="sxs-lookup"><span data-stu-id="47e8b-246">Container</span></span>

<span data-ttu-id="47e8b-247">**FWPM \_ ACTRL, \_ énumération**</span><span class="sxs-lookup"><span data-stu-id="47e8b-247">**FWPM\_ACTRL\_ENUM**</span></span>

<span data-ttu-id="47e8b-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="47e8b-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span></span><br/>

<span data-ttu-id="47e8b-249">Aucune vérification d’accès supplémentaire au-delà de celles pour les filtres individuels et les contextes de fournisseur</span><span class="sxs-lookup"><span data-stu-id="47e8b-249">No additional access checks beyond those for the individual filters and provider contexts</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="47e8b-250">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47e8b-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47e8b-251">**Droits d’accès standard**</span><span class="sxs-lookup"><span data-stu-id="47e8b-251">**Standard Access Rights**</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="47e8b-252">Modèle de contrôle d’accès Windows</span><span class="sxs-lookup"><span data-stu-id="47e8b-252">Windows access control model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[<span data-ttu-id="47e8b-253">**Identificateurs des droits d’accès à la plateforme de filtrage Windows**</span><span class="sxs-lookup"><span data-stu-id="47e8b-253">**Windows Filtering Platform Access Rights Identifiers**</span></span>](access-right-identifiers.md)
</dt> </dl>

 

