---
description: Une application COM+ est essentiellement une construction déclarative qui vous permet de configurer un nombre quelconque de composants en commun. Par exemple, vous pouvez configurer les composants d’une application avec une stratégie de sécurité commune.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configuration des applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516771"
---
# <a name="configuring-com-applications"></a><span data-ttu-id="3e484-104">Configuration des applications COM+</span><span class="sxs-lookup"><span data-stu-id="3e484-104">Configuring COM+ Applications</span></span>

<span data-ttu-id="3e484-105">Une application COM+ est essentiellement une construction déclarative qui vous permet de configurer un nombre quelconque de composants en commun.</span><span class="sxs-lookup"><span data-stu-id="3e484-105">A COM+ application is essentially a declarative construct that enables you to configure any number of components in common.</span></span> <span data-ttu-id="3e484-106">Par exemple, vous pouvez configurer les composants d’une application avec une stratégie de sécurité commune.</span><span class="sxs-lookup"><span data-stu-id="3e484-106">For example, you can configure the components in an application with a common security policy.</span></span>

<span data-ttu-id="3e484-107">La configuration est un élément essentiel du processus de développement pour les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="3e484-107">Configuration is an essential part of the development process for COM+ applications.</span></span> <span data-ttu-id="3e484-108">La façon dont vous configurez une application détermine la façon dont COM+ fournit des services pour celle-ci et comment elle se comporte quand elle est exécutée.</span><span class="sxs-lookup"><span data-stu-id="3e484-108">How you configure an application will determine how COM+ will provide services for it and how it behaves when running.</span></span>

<span data-ttu-id="3e484-109">Vous pouvez configurer des applications COM+ à l’aide de l’outil d’administration Services de composants ou des objets et interfaces d’administration pouvant faire l’objet d’un script qui fournissent la fonctionnalité sous-jacente de l’outil d’administration.</span><span class="sxs-lookup"><span data-stu-id="3e484-109">You can configure COM+ applications using either the Component Services administration tool or the scriptable administration objects and interfaces that provide the underlying functionality of the administration tool.</span></span> <span data-ttu-id="3e484-110">Pour plus d’informations sur l’exécution de l’administration par script, consultez automatisation de l' [administration com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="3e484-110">For details on performing scripted administration, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

<span data-ttu-id="3e484-111">Vous pouvez configurer des éléments aux niveaux suivants dans les applications COM+ :</span><span class="sxs-lookup"><span data-stu-id="3e484-111">You can configure elements at the following levels within COM+ applications:</span></span>

-   [<span data-ttu-id="3e484-112">Paramètres au niveau de l’application</span><span class="sxs-lookup"><span data-stu-id="3e484-112">Application-Level Settings</span></span>](#application-level-settings)
-   [<span data-ttu-id="3e484-113">Paramètres au niveau du composant (au niveau de la classe)</span><span class="sxs-lookup"><span data-stu-id="3e484-113">Component-Level (Class-Level) Settings</span></span>](#component-level-class-level-settings)
-   [<span data-ttu-id="3e484-114">Paramètre au niveau de l’interface</span><span class="sxs-lookup"><span data-stu-id="3e484-114">Interface-Level Setting</span></span>](#interface-level-setting)
-   [<span data-ttu-id="3e484-115">Paramètre au niveau de la méthode</span><span class="sxs-lookup"><span data-stu-id="3e484-115">Method-Level Setting</span></span>](#method-level-setting)
-   [<span data-ttu-id="3e484-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e484-116">Related topics</span></span>](#related-topics)

<span data-ttu-id="3e484-117">La façon dont vous installez les composants dans une application peut affecter la façon dont vous pouvez les configurer.</span><span class="sxs-lookup"><span data-stu-id="3e484-117">How you install components into an application can affect how you can configure them.</span></span> <span data-ttu-id="3e484-118">Vous devez toujours installer les composants dans des applications COM+ (au lieu de les importer).</span><span class="sxs-lookup"><span data-stu-id="3e484-118">You should always install components into COM+ applications (as opposed to importing them).</span></span> <span data-ttu-id="3e484-119">L’installation des composants les enregistre entièrement, ainsi que les interfaces et les bibliothèques de types, dans la base de données d’inscription de classe COM+ (RegDB) afin que vous puissiez les configurer.</span><span class="sxs-lookup"><span data-stu-id="3e484-119">Installing components will fully register them, along with interfaces and type libraries, in the COM+ class registration database (RegDB) so that you can configure them.</span></span>

## <a name="application-level-settings"></a><span data-ttu-id="3e484-120">Paramètres de Application-Level</span><span class="sxs-lookup"><span data-stu-id="3e484-120">Application-Level Settings</span></span>



| <span data-ttu-id="3e484-121">Attribut</span><span class="sxs-lookup"><span data-stu-id="3e484-121">Attribute</span></span>                                                                                        | <span data-ttu-id="3e484-122">Description</span><span class="sxs-lookup"><span data-stu-id="3e484-122">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e484-123">Activation</span><span class="sxs-lookup"><span data-stu-id="3e484-123">Activation</span></span>](context-activation.md)<br/>                                                  | <span data-ttu-id="3e484-124">Spécifie le type d’application : application serveur ou application de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3e484-124">Specifies application type: either server application or library application.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="3e484-125">Activation des vérifications d’accès</span><span class="sxs-lookup"><span data-stu-id="3e484-125">Enabling access checks</span></span>](enabling-access-checks-for-an-application.md)<br/>               | <span data-ttu-id="3e484-126">Active et désactive la vérification de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="3e484-126">Turns security checking on and off.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="3e484-127">Niveau de sécurité</span><span class="sxs-lookup"><span data-stu-id="3e484-127">Security level</span></span>](setting-a-security-level-for-access-checks.md)<br/>                      | <span data-ttu-id="3e484-128">Spécifie que les contrôles d’accès seront effectués au niveau du processus (niveaux de contrôle d’accès générés à partir des rôles) ou à la fois au niveau du processus et au niveau du composant (sécurité complète basée sur les rôles).</span><span class="sxs-lookup"><span data-stu-id="3e484-128">Specifies that access checks will be performed at the process level (access-checking levels generated from roles) or both at process and at component levels (full role-based security).</span></span><br/> |
| [<span data-ttu-id="3e484-129">Niveau d'authentification</span><span class="sxs-lookup"><span data-stu-id="3e484-129">Authentication level</span></span>](setting-an-authentication-level-for-a-server-application.md)<br/>  | <span data-ttu-id="3e484-130">Définit le niveau d’authentification utilisé pour les appels dans l’application.</span><span class="sxs-lookup"><span data-stu-id="3e484-130">Sets the authentication level used on calls into the application.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="3e484-131">Niveau d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="3e484-131">Impersonation level</span></span>](setting-an-impersonation-level.md)<br/>                             | <span data-ttu-id="3e484-132">Définit le niveau d’emprunt d’identité utilisé pour les appels à d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="3e484-132">Sets the impersonation level used on calls to other applications.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="3e484-133">Queuing</span><span class="sxs-lookup"><span data-stu-id="3e484-133">Queuing</span></span>](creating-queuable-components.md)<br/>                                           | <span data-ttu-id="3e484-134">Spécifie que les composants de l’application utiliseront les services de mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="3e484-134">Specifies that application components will use queuing services.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="3e484-135">Activer CRM</span><span class="sxs-lookup"><span data-stu-id="3e484-135">Enable CRM</span></span>](configuring-com--crm-components.md)<br/>                                     | <span data-ttu-id="3e484-136">Permet l’utilisation de gestionnaires de ressources de compensation.</span><span class="sxs-lookup"><span data-stu-id="3e484-136">Enables use of Compensating Resource Managers.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="3e484-137">Exécuter l’application en tant que service</span><span class="sxs-lookup"><span data-stu-id="3e484-137">Run application as a service</span></span>](com--applications-running-as-service-applications.md)<br/> | <span data-ttu-id="3e484-138">Configure et implémente une application serveur COM+ en tant que service NT.</span><span class="sxs-lookup"><span data-stu-id="3e484-138">Configures and implements a COM+ server application as an NT service.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="3e484-139">Service SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="3e484-139">COM+ SOAP service</span></span>](com--soap-service.md)<br/>                                            | <span data-ttu-id="3e484-140">Expose une application COM+ en tant que service Web XML.</span><span class="sxs-lookup"><span data-stu-id="3e484-140">Exposes a COM+ application as an XML web service.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="3e484-141">Regroupement d’applications</span><span class="sxs-lookup"><span data-stu-id="3e484-141">Application pooling</span></span>](com--application-pooling.md)<br/>                                   | <span data-ttu-id="3e484-142">Ajoute l’extensibilité pour les processus monothread et s’intègre au service de recyclage des applications COM+.</span><span class="sxs-lookup"><span data-stu-id="3e484-142">Adds scalability for single-threaded processes and integrates with the COM+ Application Recycling service.</span></span><br/>                                                                               |
| [<span data-ttu-id="3e484-143">Recyclage d’applications</span><span class="sxs-lookup"><span data-stu-id="3e484-143">Application recycling</span></span>](com--application-recycling.md)<br/>                               | <span data-ttu-id="3e484-144">Augmente la stabilité de l’application en arrêtant en douceur un processus associé à une application et en le redémarrant.</span><span class="sxs-lookup"><span data-stu-id="3e484-144">Increases application stability by gracefully shutting down a process associated with an application and restarting it.</span></span><br/>                                                                  |
| [<span data-ttu-id="3e484-145">Vidage de processus</span><span class="sxs-lookup"><span data-stu-id="3e484-145">Process dumping</span></span>](what-s-new-in-com--1-5.md)<br/>                                         | <span data-ttu-id="3e484-146">Vide la totalité de l’état d’un processus sans l’arrêter, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="3e484-146">Dumps the entire state of a process without terminating it, for debugging purposes.</span></span><br/>                                                                                                      |
| <span data-ttu-id="3e484-147">Arrêt du processus serveur</span><span class="sxs-lookup"><span data-stu-id="3e484-147">Server process shutdown</span></span><br/>                                                               | <span data-ttu-id="3e484-148">Arrête un processus après une période d’inactivité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3e484-148">Shuts down a process after a specified idle period.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="3e484-149">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3e484-149">Permissions</span></span><br/>                                                                           | <span data-ttu-id="3e484-150">Désactive les modifications apportées aux paramètres de configuration, y compris la suppression.</span><span class="sxs-lookup"><span data-stu-id="3e484-150">Disables changes to configuration settings, including deletion.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="3e484-151">Identité de sécurité</span><span class="sxs-lookup"><span data-stu-id="3e484-151">Security identity</span></span><br/>                                                                     | <span data-ttu-id="3e484-152">Spécifie l’identité sous laquelle l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="3e484-152">Specifies the identity under which the application runs.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="3e484-153">Lancer dans le débogueur</span><span class="sxs-lookup"><span data-stu-id="3e484-153">Launch in debugger</span></span><br/>                                                                    | <span data-ttu-id="3e484-154">Spécifie que l’application sera lancée dans un débogueur, avec les paramètres de ligne de commande spécifiés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3e484-154">Specifies that the application will be launched in a debugger, with user-specified command-line settings.</span></span><br/>                                                                                |
| <span data-ttu-id="3e484-155">Activer la prise en charge de 3 Go</span><span class="sxs-lookup"><span data-stu-id="3e484-155">Enable 3GB support</span></span><br/>                                                                    | <span data-ttu-id="3e484-156">Permet l’utilisation de l’espace d’adressage de mémoire de processus étendu.</span><span class="sxs-lookup"><span data-stu-id="3e484-156">Enables use of extended process memory address space.</span></span><br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a><span data-ttu-id="3e484-157">Paramètres de Component-Level (au niveau de la classe)</span><span class="sxs-lookup"><span data-stu-id="3e484-157">Component-Level (Class-Level) Settings</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e484-158">Attribut</span><span class="sxs-lookup"><span data-stu-id="3e484-158">Attribute</span></span></th>
<th><span data-ttu-id="3e484-159">Description</span><span class="sxs-lookup"><span data-stu-id="3e484-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e484-160"><a href="configuring-transactions.md">Transactions</a></span><span class="sxs-lookup"><span data-stu-id="3e484-160"><a href="configuring-transactions.md">Transactions</a></span></span><br/></td>
<td><span data-ttu-id="3e484-161">Définit les spécifications automatiques des transactions désactivées, non prises en charge, prises en charge, obligatoires ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="3e484-161">Sets automatic transaction requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e484-162"><a href="setting-the-synchronization-attribute.md">Synchronisation</a></span><span class="sxs-lookup"><span data-stu-id="3e484-162"><a href="setting-the-synchronization-attribute.md">Synchronization</a></span></span><br/></td>
<td><span data-ttu-id="3e484-163">Définit les exigences de synchronisation désactivées, non prises en charge, prises en charge, obligatoires ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="3e484-163">Sets synchronization requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e484-164"><a href="enabling-jit-activation-for-a-component.md">Activation juste-à-temps</a></span><span class="sxs-lookup"><span data-stu-id="3e484-164"><a href="enabling-jit-activation-for-a-component.md">JIT Activation</a></span></span><br/></td>
<td><span data-ttu-id="3e484-165">Active l’activation juste-à-temps.</span><span class="sxs-lookup"><span data-stu-id="3e484-165">Enables just-in-time activation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e484-166"><a href="configuring-a-component-to-be-pooled.md">Mise en pool d’objets</a></span><span class="sxs-lookup"><span data-stu-id="3e484-166"><a href="configuring-a-component-to-be-pooled.md">Object pooling</a></span></span><br/></td>
<td><span data-ttu-id="3e484-167">Active le regroupement d’objets.</span><span class="sxs-lookup"><span data-stu-id="3e484-167">Enables object pooling.</span></span> <span data-ttu-id="3e484-168">La taille minimale et maximale du pool et les valeurs de délai d’attente des objets sont configurables.</span><span class="sxs-lookup"><span data-stu-id="3e484-168">Minimum and maximum pool size and object time-out values are configurable.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e484-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Construction d’objets</a></span><span class="sxs-lookup"><span data-stu-id="3e484-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Object construction</a></span></span><br/></td>
<td><span data-ttu-id="3e484-170">Active la construction d’objets paramétrables avec une chaîne de constructeur spécifiée administrativement.</span><span class="sxs-lookup"><span data-stu-id="3e484-170">Enables parameterized object construction with an administratively specified constructor string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3e484-171">La chaîne du constructeur ne doit pas être utilisée pour stocker des informations sensibles à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="3e484-171">The constructor string should not be used to store security-sensitive information.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e484-172"><a href="enabling-access-checks-at-the-component-level.md">Contrôles d’accès au niveau du composant</a></span><span class="sxs-lookup"><span data-stu-id="3e484-172"><a href="enabling-access-checks-at-the-component-level.md">Component-level access checks</a></span></span><br/></td>
<td><span data-ttu-id="3e484-173">Active ou désactive la vérification de la sécurité basée sur les rôles au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="3e484-173">Turns on or off component-level role-based security checking.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e484-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Attribution de rôle déclarative</a></span><span class="sxs-lookup"><span data-stu-id="3e484-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Declarative role assignment</a></span></span><br/></td>
<td><span data-ttu-id="3e484-175">Active l’attribution explicite des rôles au composant.</span><span class="sxs-lookup"><span data-stu-id="3e484-175">Enables explicit assignment of roles to the component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e484-176"><a href="persistent-client-side-failures.md">Classe d’exceptions de mise en file d’attente</a></span><span class="sxs-lookup"><span data-stu-id="3e484-176"><a href="persistent-client-side-failures.md">Queuing exception class</a></span></span><br/></td>
<td><span data-ttu-id="3e484-177">Indique une classe d’exception pour la gestion des échecs côté client.</span><span class="sxs-lookup"><span data-stu-id="3e484-177">Indicates an exception class for handling client-side failures.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e484-178"><a href="com--instrumentation-concepts.md">Statistiques et événements d’instrumentation</a></span><span class="sxs-lookup"><span data-stu-id="3e484-178"><a href="com--instrumentation-concepts.md">Instrumentation events and statistics</a></span></span><br/></td>
<td><span data-ttu-id="3e484-179">Active la création de rapports détaillés sur les événements système et les statistiques d’objets.</span><span class="sxs-lookup"><span data-stu-id="3e484-179">Enables detailed system event and object statistics reporting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e484-180"><a href="context-activation.md">Contexte d’activation</a></span><span class="sxs-lookup"><span data-stu-id="3e484-180"><a href="context-activation.md">Activation context</a></span></span><br/></td>
<td><span data-ttu-id="3e484-181">Active l’activation forcée d’un objet dans le contexte de l’appelant ou le contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="3e484-181">Enables forced activation of an object in the caller's context or default context.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e484-182"><a href="what-s-new-in-com--1-5.md">Création de composants privés</a></span><span class="sxs-lookup"><span data-stu-id="3e484-182"><a href="what-s-new-in-com--1-5.md">Creating private components</a></span></span><br/></td>
<td><span data-ttu-id="3e484-183">Marque le composant comme privé pour l’application.</span><span class="sxs-lookup"><span data-stu-id="3e484-183">Marks component as private to the application.</span></span> <span data-ttu-id="3e484-184">Un composant privé peut être vu et activé uniquement par d’autres composants de la même application.</span><span class="sxs-lookup"><span data-stu-id="3e484-184">A private component can be seen and activated only by other components in the same application.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a><span data-ttu-id="3e484-185">Paramètre Interface-Level</span><span class="sxs-lookup"><span data-stu-id="3e484-185">Interface-Level Setting</span></span>



| <span data-ttu-id="3e484-186">Attribut</span><span class="sxs-lookup"><span data-stu-id="3e484-186">Attribute</span></span>                                                                                           | <span data-ttu-id="3e484-187">Description</span><span class="sxs-lookup"><span data-stu-id="3e484-187">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e484-188">Mis en file d'attente.</span><span class="sxs-lookup"><span data-stu-id="3e484-188">Queued</span></span>](creating-queuable-components.md)<br/>                                               | <span data-ttu-id="3e484-189">Indique une interface de mise en file d’attente, définie dans IDL.</span><span class="sxs-lookup"><span data-stu-id="3e484-189">Indicates a queuable interface, defined in IDL.</span></span><br/>                                                                       |
| [<span data-ttu-id="3e484-190">Attribution de rôle déclarative</span><span class="sxs-lookup"><span data-stu-id="3e484-190">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="3e484-191">Active l’attribution explicite des rôles à l’interface, ainsi que les rôles hérités implicitement à partir du niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="3e484-191">Enables explicit assignment of roles to the interface as well as implicitly inherited roles from the component level.</span></span><br/> |



 

## <a name="method-level-setting"></a><span data-ttu-id="3e484-192">Paramètre Method-Level</span><span class="sxs-lookup"><span data-stu-id="3e484-192">Method-Level Setting</span></span>



| <span data-ttu-id="3e484-193">Attribut</span><span class="sxs-lookup"><span data-stu-id="3e484-193">Attribute</span></span>                                                                                           | <span data-ttu-id="3e484-194">Description</span><span class="sxs-lookup"><span data-stu-id="3e484-194">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e484-195">Terminé automatiquement</span><span class="sxs-lookup"><span data-stu-id="3e484-195">Auto-done</span></span>](enabling-auto-done-for-a-method.md)<br/>                                         | <span data-ttu-id="3e484-196">Désactive automatiquement l’objet sur le retour de la méthode et vote dans la transaction.</span><span class="sxs-lookup"><span data-stu-id="3e484-196">Automatically deactivates object on method return and votes in transaction.</span></span><br/>                                                       |
| [<span data-ttu-id="3e484-197">Attribution de rôle déclarative</span><span class="sxs-lookup"><span data-stu-id="3e484-197">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="3e484-198">Active l’attribution explicite des rôles à la méthode ainsi que les rôles hérités implicitement des niveaux interface et composant.</span><span class="sxs-lookup"><span data-stu-id="3e484-198">Enables explicit assignment of roles to the method as well as implicitly inherited roles from the interface and component levels.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3e484-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e484-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e484-200">Automatisation de l’administration COM+</span><span class="sxs-lookup"><span data-stu-id="3e484-200">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="3e484-201">Création d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="3e484-201">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="3e484-202">Déploiement d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="3e484-202">Deploying COM+ Applications</span></span>](deploying-com--applications.md)
</dt> </dl>

 

 




