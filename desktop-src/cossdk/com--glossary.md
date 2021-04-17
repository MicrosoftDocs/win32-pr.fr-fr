---
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Glossaire COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483160"
---
# <a name="com-glossary"></a><span data-ttu-id="75f63-103">Glossaire COM+</span><span class="sxs-lookup"><span data-stu-id="75f63-103">COM+ Glossary</span></span>

<dl> <dt>

<span data-ttu-id="75f63-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**jeton d’accès**</span><span class="sxs-lookup"><span data-stu-id="75f63-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**access token**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-105">Objet qui décrit le contexte de sécurité d’un processus ou d’un thread.</span><span class="sxs-lookup"><span data-stu-id="75f63-105">An object that describes the security context of a process or thread.</span></span> <span data-ttu-id="75f63-106">Les informations contenues dans un jeton incluent l’identité et les privilèges du compte d’utilisateur associé au processus ou au thread.</span><span class="sxs-lookup"><span data-stu-id="75f63-106">The information in a token includes the identity and privileges of the user account associated with the process or thread.</span></span> <span data-ttu-id="75f63-107">Lorsqu’un utilisateur ouvre une session, le système vérifie le mot de passe de l’utilisateur en le comparant avec les informations stockées dans une base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="75f63-107">When a user logs on, the system verifies the user's password by comparing it with information stored in a security database.</span></span> <span data-ttu-id="75f63-108">Si le mot de passe est authentifié, le système génère un jeton d’accès.</span><span class="sxs-lookup"><span data-stu-id="75f63-108">If the password is authenticated, the system produces an access token.</span></span> <span data-ttu-id="75f63-109">Chaque processus exécuté pour le compte de cet utilisateur dispose d’une copie de ce jeton d’accès.</span><span class="sxs-lookup"><span data-stu-id="75f63-109">Every process executed on behalf of this user has a copy of this access token.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Propriétés ACID**</span><span class="sxs-lookup"><span data-stu-id="75f63-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID properties**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-111">Acronyme de pionnier de traitement des transactions pour atomicité, cohérence, isolation et durabilité.</span><span class="sxs-lookup"><span data-stu-id="75f63-111">Acronym coined by transaction processing pioneers for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="75f63-112">Ces propriétés garantissent un comportement prévisible, renforçant le rôle des transactions en tant que propositions « tout ou rien » conçues pour fournir des résultats cohérents et prévisibles dans un environnement distribué lorsque des défaillances indépendantes peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="75f63-112">These properties ensure predictable behavior, reinforcing the role of transactions as all-or-none propositions designed to provide consistent and predictable results in a distributed environment when independent failures can occur.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**actionne**</span><span class="sxs-lookup"><span data-stu-id="75f63-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-114">Chaîne d’événements qui entraîne la création d’un objet COM et le retour d’un pointeur valide vers une interface sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="75f63-114">The chain of events that results in the creation of a COM object and the return of a valid pointer to an interface on that object.</span></span> <span data-ttu-id="75f63-115">Dans COM+, un objet est activé soit dans son propre contexte, soit dans celui de son créateur (un objet qui a demandé l’objet en cours d’activation).</span><span class="sxs-lookup"><span data-stu-id="75f63-115">In COM+, an object gets activated either in its own context or in that of its creator (an object that has requested the object being activated).</span></span> <span data-ttu-id="75f63-116">Les services COM+ s’appuient sur l’activation appropriée d’un objet en fonction de la configuration de l’objet.</span><span class="sxs-lookup"><span data-stu-id="75f63-116">COM+ services rely on appropriate activation of an object based on the object's configuration.</span></span> <span data-ttu-id="75f63-117">Au cours de l’activation, le système détermine le contexte dans lequel l’objet s’exécute, initialise les propriétés de contexte, vérifie les autorisations d’accès et établit une identité de sécurité.</span><span class="sxs-lookup"><span data-stu-id="75f63-117">In the course of activation, the system determines the context in which the object runs, initializes the context properties, checks access permissions, and establishes a security identity.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**sécurité d’activation**</span><span class="sxs-lookup"><span data-stu-id="75f63-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**activation security**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-119">Forme de protection de sécurité qui détermine qui peut lancer un serveur.</span><span class="sxs-lookup"><span data-stu-id="75f63-119">A form of security protection that determines who can launch a server.</span></span> <span data-ttu-id="75f63-120">La sécurité d’activation est automatiquement appliquée par le gestionnaire de contrôle des services (SCM) d’un ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="75f63-120">Activation security is automatically applied by the Service Control Manager (SCM) of a particular computer.</span></span> <span data-ttu-id="75f63-121">Lors de la réception d’une demande d’activation d’un objet par un client, le SCM vérifie la demande par rapport aux informations d’activation de sécurité stockées dans son registre.</span><span class="sxs-lookup"><span data-stu-id="75f63-121">Upon receipt of a request from a client to activate an object, the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="75f63-122">La sécurité d’activation est également vérifiée pour les activations du même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="75f63-122">Activation security is also checked for same-computer activations.</span></span> <span data-ttu-id="75f63-123">Également appelé *lancement sécurité*.</span><span class="sxs-lookup"><span data-stu-id="75f63-123">Also called *launch security*.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**type d’activation**</span><span class="sxs-lookup"><span data-stu-id="75f63-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**activation type**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-125">Catégorie d’activation pour une application COM+ qui indique si l’application s’exécute dans ou en dehors de l’espace de processus de son client (selon qu’il s’agit d’une application de bibliothèque ou de serveur, respectivement) et si l’application s’exécute en tant que service.</span><span class="sxs-lookup"><span data-stu-id="75f63-125">Activation category for a COM+ application that indicates whether the application runs in or out of its client's process space (depending on whether it's a library or server application, respectively) as well as whether the application runs as a service.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**bas**</span><span class="sxs-lookup"><span data-stu-id="75f63-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**activity**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-127">Dans COM+, il s’agit d’un thread logique comprenant une ou plusieurs transactions et contenant une collection de composants regroupés dans une application COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-127">In COM+, a logical thread comprising one or more transactions and containing a collection of components that are grouped into a COM+ application.</span></span> <span data-ttu-id="75f63-128">Chaque objet COM appartient à une activité.</span><span class="sxs-lookup"><span data-stu-id="75f63-128">Every COM object belongs to one activity.</span></span> <span data-ttu-id="75f63-129">L’association entre un objet et une activité ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="75f63-129">The association between an object and an activity cannot be changed.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**processus de modèle cloisonné**</span><span class="sxs-lookup"><span data-stu-id="75f63-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**apartment model process**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-131">Processus qui a au moins deux cloisonnements à thread unique et aucun cloisonnement multithread.</span><span class="sxs-lookup"><span data-stu-id="75f63-131">A process that has two or more single-threaded apartments and no multithreaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy d’application**</span><span class="sxs-lookup"><span data-stu-id="75f63-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**application proxy**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-133">Ensemble de fichiers contenant des informations d’inscription permettant à un client d’accéder à distance à une application serveur COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-133">A set of files containing registration information that allows a client to remotely access a COM+ server application.</span></span> <span data-ttu-id="75f63-134">Lorsqu’il est installé sur un ordinateur client, un fichier de proxy d’application écrit les informations relatives à l’application serveur sur l’ordinateur client. le client peut ensuite accéder à distance à l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="75f63-134">When installed on a client computer, an application proxy file writes information about the server application to the client computer; the client can then remotely access the server application.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**identification**</span><span class="sxs-lookup"><span data-stu-id="75f63-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**authentication**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-136">Le processus de sécurité consistant à déterminer qu’un appelant d’une application est réellement celui qu’il dit, c’est qu’il vérifie l’authenticité d’une revendication d’identité.</span><span class="sxs-lookup"><span data-stu-id="75f63-136">The security process of determining that a caller of an application is actually who it says it is—verifying the authenticity of an identity claim.</span></span> <span data-ttu-id="75f63-137">Pour les applications COM+, l’authentification peut être activée et configurée de manière administrative, après quoi elle fonctionne de façon transparente pour l’application.</span><span class="sxs-lookup"><span data-stu-id="75f63-137">For COM+ applications, authentication can be turned on and configured administratively, after which it works transparently to the application.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**l'**</span><span class="sxs-lookup"><span data-stu-id="75f63-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**authorization**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-139">Processus de sécurité permettant de déterminer si un appelant d’une application est autorisé à faire ce qu’il demande.</span><span class="sxs-lookup"><span data-stu-id="75f63-139">The security process of determining whether a caller of an application is authorized to do what it is asking to do.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**mise en cache de Resource Manager**</span><span class="sxs-lookup"><span data-stu-id="75f63-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**caching resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-141">Gestionnaire de ressources qui agit comme serveur frontal d’un autre gestionnaire de ressources et qui met en cache les informations localement, ce qui réduit le coût d’accès à la ressource sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="75f63-141">A resource manager that acts as a front-end to another resource manager and that caches information locally, reducing the cost of accessing the underlying resource.</span></span> <span data-ttu-id="75f63-142">Contrairement à un gestionnaire de ressources conventionnel, un gestionnaire de ressources de mise en cache ne participe pas à la récupération car il ne stocke jamais de manière permanente les données sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="75f63-142">Unlike a conventional resource manager, a caching resource manager does not participate in recovery because it never permanently stores the underlying data.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**sécurité de l’appel**</span><span class="sxs-lookup"><span data-stu-id="75f63-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**call security**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-144">Forme de protection de sécurité qui permet de contrôler l’accès aux méthodes d’un objet serveur après le lancement d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="75f63-144">A form of security protection that helps control access to a server object's methods after a server has been launched.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**classe (COM)**</span><span class="sxs-lookup"><span data-stu-id="75f63-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**class (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-146">Implémentation concrète nommée d’une ou de plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="75f63-146">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="75f63-147">Une classe COM est identifiée par un CLSID et, parfois, un ProgID.</span><span class="sxs-lookup"><span data-stu-id="75f63-147">A COM class is identified by a CLSID and, sometimes, a ProgID.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**masquer**</span><span class="sxs-lookup"><span data-stu-id="75f63-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-149">Possibilité pour un serveur de masquer sa propre identité lors d’appels au nom d’un client.</span><span class="sxs-lookup"><span data-stu-id="75f63-149">A server's ability to mask its own identity when making calls on a client's behalf.</span></span> <span data-ttu-id="75f63-150">Lorsque le masquage est activé, les appels effectués par le serveur qui emprunte l’identité du client peuvent être effectués sous l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="75f63-150">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="75f63-151">Lorsque le masquage est désactivé, les appels par le serveur sont effectués sous l’identité du serveur.</span><span class="sxs-lookup"><span data-stu-id="75f63-151">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Application COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM+ application**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-153">Unité principale d’administration et de sécurité pour les services de composants.</span><span class="sxs-lookup"><span data-stu-id="75f63-153">The primary unit of administration and security for Component Services.</span></span> <span data-ttu-id="75f63-154">Une application COM+ est un groupe de composants COM qui exécutent généralement des fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="75f63-154">A COM+ application is a group of COM components that, generally, perform related functions.</span></span> <span data-ttu-id="75f63-155">Ces composants se composent davantage d’interfaces et de méthodes COM.</span><span class="sxs-lookup"><span data-stu-id="75f63-155">These components further consist of COM interfaces and methods.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Regroupement d’applications COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM+ Application Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-157">Fonctionnalité services de composants qui permet la mise à l’échelle des processus à thread unique et peut également vous aider à récupérer après des défaillances dans les processus uniques en fournissant d’autres processus en cours d’exécution capables de gérer les activations.</span><span class="sxs-lookup"><span data-stu-id="75f63-157">A Component Services feature that allows single-threaded processes to scale and can also help you recover from failures in single processes by providing other running processes able to handle activations.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Recyclage des applications COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM+ Application Recycling**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-159">Fonctionnalité services de composants qui augmente considérablement la stabilité globale de vos applications en vous permettant d’arrêter en douceur un processus associé à une application et de la redémarrer.</span><span class="sxs-lookup"><span data-stu-id="75f63-159">A Component Services feature that significantly increases the overall stability of your applications by allowing you to gracefully shut down a process associated with an application and restart it.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catalogue COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM+ catalog**</span></span> 
</dt> <dd>

<span data-ttu-id="75f63-161">Magasin de données qui contient les données de configuration COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-161">The data store that holds COM+ configuration data.</span></span> <span data-ttu-id="75f63-162">Les performances des tâches d’administration COM+ nécessitent la lecture et l’écriture des données stockées dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="75f63-162">Performance of COM+ administration tasks requires reading and writing data stored in the catalog.</span></span> <span data-ttu-id="75f63-163">Le catalogue est accessible uniquement par le biais de l’outil d’administration Services de composants ou par le biais de la bibliothèque comadmin.</span><span class="sxs-lookup"><span data-stu-id="75f63-163">The catalog can be accessed only through the Component Services administrative tool or through the COMAdmin library.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Événements COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM+ Events**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-165">Les événements COM+ correspondent aux serveurs de publication et aux abonnés et les connecte à l’aide d’un système d’événements faiblement couplés.</span><span class="sxs-lookup"><span data-stu-id="75f63-165">COM+ Events matches and connects publishers and subscribers through a loosely coupled events system.</span></span> <span data-ttu-id="75f63-166">Un serveur de publication effectue l’appel de méthode pour initier un événement, et un abonné reçoit ces appels via le système d’événements plutôt que directement à partir du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="75f63-166">A publisher makes the method call to initiate an event, and a subscriber receives these calls through the event system rather than directly from the publisher.</span></span> <span data-ttu-id="75f63-167">Le service événements COM+ gère la liste des abonnés intéressés qui reçoivent les appels et dirige ces appels sans avoir besoin de connaître le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="75f63-167">The COM+ Events service maintains the list of interested subscribers who receive the calls and directs those calls without requiring the knowledge of the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Application de bibliothèque COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM+ library application**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-169">Application COM+ qui s’exécute dans le processus du client qui la crée.</span><span class="sxs-lookup"><span data-stu-id="75f63-169">A COM+ application that runs in the process of the client that creates it.</span></span> <span data-ttu-id="75f63-170">Les applications de bibliothèque peuvent utiliser la sécurité basée sur les rôles, mais ne prennent pas en charge l’accès à distance ou les composants en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="75f63-170">Library applications can use role-based security but do not support remote access or queued components.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Mise en pool d’objets COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM+ Object Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-172">Service automatique fourni par COM+ qui vous permet de configurer un composant pour que des instances de lui-même restent actives dans un pool, prêtes à être utilisées par n’importe quel client qui demande le composant.</span><span class="sxs-lookup"><span data-stu-id="75f63-172">An automatic service provided by COM+ that enables you to configure a component to have instances of itself kept active in a pool, ready to be used by any client that requests the component.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Partitions COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM+ Partitions**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-174">Service COM+ qui permet, sur un seul ordinateur, de créer des espaces d’exécution distincts pour les applications.</span><span class="sxs-lookup"><span data-stu-id="75f63-174">A COM+ service that enables, on a single computer, the creation of separate execution spaces for applications.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Jeux de partitions COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM+ partition sets**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-176">Groupe de partitions COM+ mappé à un ID d’utilisateur particulier dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="75f63-176">A group of COM+ partitions that is mapped to a particular user ID in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Composants en file d’attente COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM+ Queued Components**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-178">Service COM+, basé sur Microsoft Message Queuing, qui offre un moyen simple d’appeler et d’exécuter des composants de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="75f63-178">A COM+ service, based on Microsoft Message Queuing, that provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="75f63-179">Le traitement des messages peut se produire sans tenir compte de la disponibilité ou de l’accessibilité de l’expéditeur ou du destinataire.</span><span class="sxs-lookup"><span data-stu-id="75f63-179">Message processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Application serveur COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+ server application**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-181">Application COM+ qui s’exécute dans son propre processus.</span><span class="sxs-lookup"><span data-stu-id="75f63-181">A COM+ application that runs in its own process.</span></span> <span data-ttu-id="75f63-182">Les applications serveur peuvent prendre en charge tous les services COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-182">Server applications can support all COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**SOAP COM+**</span><span class="sxs-lookup"><span data-stu-id="75f63-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+ SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-184">Fonctionnalité services de composants qui vous permet d’exposer une application COM+ en tant que service Web XML.</span><span class="sxs-lookup"><span data-stu-id="75f63-184">A Component Services feature that allows you to expose a COM+ application as an XML web service.</span></span> <span data-ttu-id="75f63-185">Le protocole SOAP COM+ vous permet également d’utiliser un service Web XML en tant que composant COM.</span><span class="sxs-lookup"><span data-stu-id="75f63-185">COM+ SOAP also enables you to use an XML web service as a COM component.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Composant COM**</span><span class="sxs-lookup"><span data-stu-id="75f63-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM component**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-187">Unité binaire de code qui comprend le code d’empaquetage et d’inscription et qui crée des objets COM.</span><span class="sxs-lookup"><span data-stu-id="75f63-187">A binary unit of code that includes packaging and registration code and that creates COM objects.</span></span> <span data-ttu-id="75f63-188">Toutes les applications COM+ comportent un ou plusieurs composants COM.</span><span class="sxs-lookup"><span data-stu-id="75f63-188">All COM+ applications consist of one or more COM components.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**arborescence de validation**</span><span class="sxs-lookup"><span data-stu-id="75f63-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**commit tree**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-190">Dans un système de transactions distribuées, la représentation conceptuelle d’une transaction est basée sur les relations hiérarchiques entre les gestionnaires de transactions individuels participant à une transaction distribuée.</span><span class="sxs-lookup"><span data-stu-id="75f63-190">In a distributed transaction system, the conceptual representation of a transaction as based on the hierarchical relationships between individual transaction managers participating in a distributed transaction.</span></span> <span data-ttu-id="75f63-191">Les gestionnaires de ressources inscrits dans cette hiérarchie sont associés aux gestionnaires de transactions.</span><span class="sxs-lookup"><span data-stu-id="75f63-191">Included in that hierarchy are the enlisted resource managers associated with the transaction managers.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Objet COM**</span><span class="sxs-lookup"><span data-stu-id="75f63-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-193">Dans le modèle de programmation COM, structure de programmation encapsulant à la fois les données et les fonctionnalités, qui sont définies et allouées en tant qu’unité unique et pour lesquelles le seul accès public s’effectue via les interfaces de la structure de programmation.</span><span class="sxs-lookup"><span data-stu-id="75f63-193">In the COM programming model, a programming structure encapsulating both data and functionality, which are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="75f63-194">Un objet COM doit prendre en charge, au minimum, l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , qui maintient l’existence de l’objet pendant son utilisation et fournit l’accès aux autres interfaces de l’objet.</span><span class="sxs-lookup"><span data-stu-id="75f63-194">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Gestionnaire des ressources de compensation (CRM)**</span><span class="sxs-lookup"><span data-stu-id="75f63-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Compensating Resource Manager (CRM)**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-196">Fonctionnalité COM+ qui permet aux ressources non transactionnelles de participer à une transaction de validation en deux phases avec le Distributed Transaction Coordinator Microsoft (DTC).</span><span class="sxs-lookup"><span data-stu-id="75f63-196">A COM+ feature that enables non-transactional resources to participate in a two-phase commit transaction with the Microsoft Distributed Transaction Coordinator (DTC).</span></span> <span data-ttu-id="75f63-197">En règle générale, les gestionnaires de ressources ne fournissent pas les fonctionnalités d’isolation des gestionnaires de ressources complets, mais ils fournissent une atomicité et une durabilité transactionnelles en écrivant dans un journal.</span><span class="sxs-lookup"><span data-stu-id="75f63-197">Typically, CRMs do not provide the isolation capabilities of full resource managers, but they do provide transactional atomicity and durability by writing to a log.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Outil d’administration Services de composants**</span><span class="sxs-lookup"><span data-stu-id="75f63-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Component Services administrative tool**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-199">Composant logiciel enfichable d’interface utilisateur permettant aux administrateurs et aux développeurs de créer, de configurer et de gérer des applications COM+, ainsi que d’administrer les transactions distribuées et les bases de données résidant en mémoire.</span><span class="sxs-lookup"><span data-stu-id="75f63-199">A user-interface snap-in through which administrators and developers can create, configure, and maintain COM+ applications, as well as administer distributed transactions and memory-resident databases.</span></span> <span data-ttu-id="75f63-200">L’outil d’administration Services de composants peut également être utilisé pour afficher des événements système et gérer des services système locaux sur l’ordinateur sur lequel l’outil est installé.</span><span class="sxs-lookup"><span data-stu-id="75f63-200">The Component Services administrative tool can also be used to view system events and manage system services local to the computer on which the tool is installed.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modèle conceptuel**</span><span class="sxs-lookup"><span data-stu-id="75f63-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**conceptual model**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-202">La première étape de la phase de conception de l’application COM+, où le développeur définit les problèmes d’entreprise à résoudre et détermine les composants et services requis.</span><span class="sxs-lookup"><span data-stu-id="75f63-202">The first step in the COM+ application design phase, where the developer defines the business problems to be solved and decides what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**d’accès concurrentiel**</span><span class="sxs-lookup"><span data-stu-id="75f63-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**concurrency**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-204">Capacité de plusieurs transactions ou processus à accéder aux mêmes données en même temps.</span><span class="sxs-lookup"><span data-stu-id="75f63-204">The ability of more than one transaction or process to access the same data at the same time.</span></span> <span data-ttu-id="75f63-205">COM+ gère généralement l’accès concurrentiel par le biais de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="75f63-205">COM+ generally manages concurrency through synchronization.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**composant configuré**</span><span class="sxs-lookup"><span data-stu-id="75f63-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**configured component**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-207">Composant COM qui a été installé dans une application COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-207">A COM component that has been installed into a COM+ application.</span></span> <span data-ttu-id="75f63-208">Une fois installé, le composant est configuré dans le catalogue COM+ pour utiliser les services COM+ disponibles.</span><span class="sxs-lookup"><span data-stu-id="75f63-208">After it is installed, the component is configured within the COM+ catalog to make use of the available COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**contexte**</span><span class="sxs-lookup"><span data-stu-id="75f63-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-210">Ensemble de propriétés au moment de l’exécution associées à un ou plusieurs objets COM utilisés pour fournir des services pour ces objets.</span><span class="sxs-lookup"><span data-stu-id="75f63-210">A set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span> <span data-ttu-id="75f63-211">Chaque objet COM s’exécute dans un contexte unique de l’activation à la désactivation (toujours dans le même cloisonnement).</span><span class="sxs-lookup"><span data-stu-id="75f63-211">Every COM object runs in a single context from activation to deactivation (always within the same apartment).</span></span> <span data-ttu-id="75f63-212">Initialisé lorsqu’un objet est activé, les propriétés de contexte, telles que les propriétés de contexte de sécurité, représentent les besoins d’un objet au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="75f63-212">Initialized when an object is activated, context properties, such as security context properties, represent the run-time needs of an object.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**couche données**</span><span class="sxs-lookup"><span data-stu-id="75f63-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**data tier**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-214">Dans le modèle d’architecture à trois niveaux pour les applications d’entreprise, la couche d’accès au SGBD, accessible par le biais du niveau intermédiaire ou de la couche des services d’entreprise, et à l’occasion de la couche présentation ou de la couche services utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75f63-214">In the three-tier architecture model for business applications, the DBMS access layer, which can be accessed through the middle tier, or business services layer, and on occasion through the presentation tier, or user services layer.</span></span> <span data-ttu-id="75f63-215">La couche données se compose de composants d’accès aux données (plutôt que de connexions SGBD brutes) pour faciliter le partage des ressources et permettre la configuration des clients sans installer les bibliothèques SGBD et les pilotes ODBC sur chaque client.</span><span class="sxs-lookup"><span data-stu-id="75f63-215">The data tier consists of data access components (rather than raw DBMS connections) to aid in resource sharing and to allow clients to be configured without installing the DBMS libraries and ODBC drivers on each client.</span></span> <span data-ttu-id="75f63-216">Également appelée *couche des services de données*.</span><span class="sxs-lookup"><span data-stu-id="75f63-216">Also called *data services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**Fatal**</span><span class="sxs-lookup"><span data-stu-id="75f63-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**deadlock**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-218">Dans les applications multithread, problème de threading qui se produit lorsque chaque membre d’un ensemble de threads attend un autre membre de l’ensemble.</span><span class="sxs-lookup"><span data-stu-id="75f63-218">In multithreaded applications, a threading problem that occurs when each member of a set of threads is waiting for another member of the set.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**délégation**</span><span class="sxs-lookup"><span data-stu-id="75f63-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**delegation**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-220">Forme d’emprunt d’identité qui autorise un serveur à agir au nom d’un client, ce qui permet au serveur d’emprunter l’identité de clients sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="75f63-220">A form of impersonation that authorizes a server to act on a client's behalf, giving the server the ability to impersonate clients over the network.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transaction distribuée**</span><span class="sxs-lookup"><span data-stu-id="75f63-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**distributed transaction**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-222">Transaction impliquant plusieurs gestionnaires de ressources, qui peuvent se trouver sur des ordinateurs identiques ou différents.</span><span class="sxs-lookup"><span data-stu-id="75f63-222">A transaction that involves multiple resource managers, which can be on the same or different computers.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span><span class="sxs-lookup"><span data-stu-id="75f63-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-224">Service système qui gère les transactions et les communications liées aux transactions qui sont réparties sur deux ou plusieurs gestionnaires de ressources sur un ou plusieurs systèmes afin de garantir des transactions ACID correctes.</span><span class="sxs-lookup"><span data-stu-id="75f63-224">A system service that manages transactions and transaction-related communications that are distributed across two or more resource managers on one or more systems to ensure correct ACID transactions.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**masquage dynamique**</span><span class="sxs-lookup"><span data-stu-id="75f63-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**dynamic cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-226">Forme de masquage où l’identité du client d’origine est détectée comme jeton d’accès au thread du serveur sur chaque appel de méthode au serveur en aval.</span><span class="sxs-lookup"><span data-stu-id="75f63-226">A form of cloaking where the original client identity is discovered as the server thread access token on each method call to the downstream server.</span></span> <span data-ttu-id="75f63-227">Bien que l’identité présentée puisse être déterminée dynamiquement, la surcharge requise pour le faire peut être considérablement plus coûteuse.</span><span class="sxs-lookup"><span data-stu-id="75f63-227">Although the identity that is presented can be determined dynamically, the overhead required to do this can be considerably more expensive.</span></span> <span data-ttu-id="75f63-228">Pour les applications COM+, la configuration par défaut est pour la fonctionnalité de voilage dynamique, car elle offre la flexibilité qui est généralement requise dans les circonstances qui nécessitent l’utilisation de l’emprunt d’identité en premier lieu.</span><span class="sxs-lookup"><span data-stu-id="75f63-228">For COM+ applications, the default configuration is for dynamic cloaking capability because it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**objet Enumerator**</span><span class="sxs-lookup"><span data-stu-id="75f63-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**enumerator object**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-230">Permet l’énumération des éléments dans une collection.</span><span class="sxs-lookup"><span data-stu-id="75f63-230">Enables enumeration of items in a collection.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**événement**</span><span class="sxs-lookup"><span data-stu-id="75f63-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**event**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-232">Action reconnue par un objet, par exemple en cliquant sur la souris ou en appuyant sur une touche, et pour laquelle vous pouvez écrire du code pour répondre.</span><span class="sxs-lookup"><span data-stu-id="75f63-232">An action recognized by an object, such as clicking the mouse or pressing a key, and for which you can write code to respond.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**Event, objet de classe**</span><span class="sxs-lookup"><span data-stu-id="75f63-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**event class object**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-234">Composant configuré qui fournit un enregistrement persistant dans le système d’événement COM+ pour décrire les serveurs de publication et les interfaces de déclenchement associées à ces serveurs de publication.</span><span class="sxs-lookup"><span data-stu-id="75f63-234">A configured component that provides a persistent record in the COM+ event system to describe the publishers and the firing interfaces associated with those publishers.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**méthode d’événement**</span><span class="sxs-lookup"><span data-stu-id="75f63-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**event method**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-236">Méthode dans une interface COM+ qui identifie un événement COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-236">A method in a COM+ interface that identifies a COM+ event.</span></span> <span data-ttu-id="75f63-237">Les méthodes d’événement doivent être nommées de manière unique et ne peuvent contenir que des paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="75f63-237">Event methods must be uniquely named and can contain only input parameters.</span></span> <span data-ttu-id="75f63-238">La valeur de retour doit être un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="75f63-238">The return value must be an **HRESULT**.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**objet d’événement**</span><span class="sxs-lookup"><span data-stu-id="75f63-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**event object**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-240">Objet COM qui peut signaler un ou plusieurs threads qu’un événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="75f63-240">A COM object that can signal one or more threads that an event has occurred.</span></span> <span data-ttu-id="75f63-241">Tout thread dans un processus peut créer un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="75f63-241">Any thread within a process can create an event object.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**titre**</span><span class="sxs-lookup"><span data-stu-id="75f63-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**exception**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-243">Condition ou erreur anormale qui se produit pendant l’exécution d’un programme et qui requiert l’exécution de logiciels en dehors du déroulement normal du contrôle.</span><span class="sxs-lookup"><span data-stu-id="75f63-243">An abnormal condition or error that occurs during the execution of a program and that requires the execution of software outside the normal flow of control.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**échec**</span><span class="sxs-lookup"><span data-stu-id="75f63-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**failover**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-245">Dans un système réseau en cluster, processus de déplacement d’une ressource surchargée ou ayant échoué (par exemple, un serveur, un lecteur de disque ou un réseau) vers son composant de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="75f63-245">In a cluster network system, the process of relocating an overloaded or failed resource—such as a server, a disk drive, or a network—to its backup component.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**processus à threads libres**</span><span class="sxs-lookup"><span data-stu-id="75f63-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**free-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-247">Processus qui a un cloisonnement multithread et aucun cloisonnement à thread unique.</span><span class="sxs-lookup"><span data-stu-id="75f63-247">A process that has a multithreaded apartment and no single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**coordinateur de validation globale**</span><span class="sxs-lookup"><span data-stu-id="75f63-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**global commit coordinator**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-249">Sur un système de transactions distribuées Microsoft Windows, le gestionnaire de transactions racine de l’arborescence de validation.</span><span class="sxs-lookup"><span data-stu-id="75f63-249">On a Microsoft Windows–based distributed transaction system, the root transaction manager of the commit tree.</span></span> <span data-ttu-id="75f63-250">Ce coordinateur prend la décision de valider ou d’abandonner une transaction donnée et n’est jamais incertaine.</span><span class="sxs-lookup"><span data-stu-id="75f63-250">This coordinator makes the decision to either commit or abort a given transaction and is never in doubt.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="75f63-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-252">Capacité d’un thread à s’exécuter dans un contexte de sécurité différent de celui du processus propriétaire du thread.</span><span class="sxs-lookup"><span data-stu-id="75f63-252">The ability of a thread to execute in a security context different from that of the process owning the thread.</span></span> <span data-ttu-id="75f63-253">Le thread serveur utilise un jeton d’accès qui représente les informations d’identification du client et, avec cela, il peut accéder aux ressources auxquelles le client peut accéder.</span><span class="sxs-lookup"><span data-stu-id="75f63-253">The server thread uses an access token representing the client's credentials, and with this, it can access resources that the client can access.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**niveau d’emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="75f63-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**impersonation level**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-255">Paramètre utilisé par le client pour accorder au serveur un niveau d’autorité particulier pour effectuer des actions au nom du client.</span><span class="sxs-lookup"><span data-stu-id="75f63-255">The setting used by the client to grant the server a particular level of authority to carry out actions on the client's behalf.</span></span> <span data-ttu-id="75f63-256">Dans COM+, cette valeur ne peut être définie que pour les applications serveur COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-256">In COM+, this can be set only for COM+ server applications.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interception**</span><span class="sxs-lookup"><span data-stu-id="75f63-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interception**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-258">Pour un objet activé dans un contexte donné, processus de gestion des appels à cet objet à partir de la limite du contexte.</span><span class="sxs-lookup"><span data-stu-id="75f63-258">For an object activated in a given context, the process of handling calls to that object from across the context boundary.</span></span> <span data-ttu-id="75f63-259">Les appels à travers le contexte sont gérés avec des proxies d’interface légère qui gèrent la médiation requise pour ajuster l’environnement d’exécution à partir d’un qui prend en charge l’appelant sur un autre qui prend en charge l’appelé.</span><span class="sxs-lookup"><span data-stu-id="75f63-259">Calls across context are handled with lightweight interface proxies that will handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**</span><span class="sxs-lookup"><span data-stu-id="75f63-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-261">Dans la programmation COM, collection de fonctions publiques associées qui fournissent l’accès à un objet COM.</span><span class="sxs-lookup"><span data-stu-id="75f63-261">In COM-based programming, a collection of related public functions that provide access to a COM object.</span></span> <span data-ttu-id="75f63-262">L’ensemble d’interfaces sur un objet COM compose un contrat qui spécifie comment les programmes et d’autres objets peuvent interagir avec l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="75f63-262">The set of interfaces on a COM object composes a contract that specifies how programs and other objects can interact with the COM object.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy d’interface**</span><span class="sxs-lookup"><span data-stu-id="75f63-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**interface proxy**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-264">Objet spécifique à l’interface qui empaquette (marshale) les paramètres de cette interface en préparation d’un appel de méthode distant et décompresse (démarshale) les valeurs de retour du stub d’interface.</span><span class="sxs-lookup"><span data-stu-id="75f63-264">An interface-specific object that packages (marshals) parameters for that interface in preparation for a remote method call and unpackages (unmarshals) the return values from the interface stub.</span></span> <span data-ttu-id="75f63-265">Un proxy s’exécute dans l’espace d’adressage de l’expéditeur et communique avec un stub correspondant dans l’espace d’adressage du destinataire.</span><span class="sxs-lookup"><span data-stu-id="75f63-265">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**stub d’interface**</span><span class="sxs-lookup"><span data-stu-id="75f63-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**interface stub**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-267">Objet spécifique à l’interface qui décompresse les paramètres marshalés, appelle la méthode requise, et les packages (Marshalers) retournent des valeurs à partir de la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="75f63-267">An interface-specific object that unpackages marshaled parameters, calls the required method, and packages (marshals) return values from the called method.</span></span> <span data-ttu-id="75f63-268">Le stub s’exécute dans l’espace d’adressage du destinataire et communique avec un proxy d’interface correspondant dans l’espace d’adressage de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="75f63-268">The stub runs in the receiver's address space and communicates with a corresponding interface proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**Objet Interior**</span><span class="sxs-lookup"><span data-stu-id="75f63-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**interior object**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-270">Dans une hiérarchie transactionnelle, tout objet sous l’objet racine.</span><span class="sxs-lookup"><span data-stu-id="75f63-270">In a transactional hierarchy, any object under the root object.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**activation juste-à-temps (JIT)**</span><span class="sxs-lookup"><span data-stu-id="75f63-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**just-in-time (JIT) activation**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-272">Service automatique fourni par COM+ qui autorise l’utilisation plus productive des ressources serveur inactives.</span><span class="sxs-lookup"><span data-stu-id="75f63-272">An automatic service provided by COM+ that allows idle server resources to be used more productively.</span></span> <span data-ttu-id="75f63-273">Lorsqu’un composant est configuré en tant que JIT activé, COM+ peut désactiver une instance de celui-ci lorsqu’un client contient encore une référence active à l’objet.</span><span class="sxs-lookup"><span data-stu-id="75f63-273">When a component is configured as JIT activated, COM+ can deactivate an instance of it while a client still holds an active reference to the object.</span></span> <span data-ttu-id="75f63-274">La prochaine fois que le client appelle une méthode sur l’objet, COM+ réactivera l’objet en toute transparence au client, juste à temps.</span><span class="sxs-lookup"><span data-stu-id="75f63-274">The next time the client calls a method on the object, COM+ will reactivate the object transparently to the client, just in time.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**composant hérité**</span><span class="sxs-lookup"><span data-stu-id="75f63-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**legacy component**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-276">Composant non configuré qui a été installé dans une application COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-276">An unconfigured component that has been installed into a COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**écouteur**</span><span class="sxs-lookup"><span data-stu-id="75f63-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**listener**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-278">Élément architectural du service de composants en file d’attente COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-278">An architectural element of the COM+ Queued Components service.</span></span> <span data-ttu-id="75f63-279">L’écouteur est un objet COM qui ouvre la file d’attente de messages associée à son application hôte et attend l’arrivée de messages.</span><span class="sxs-lookup"><span data-stu-id="75f63-279">The listener is a COM object that opens the message queue associated with its host application and waits for messages to arrive.</span></span> <span data-ttu-id="75f63-280">À mesure que les messages arrivent, l’écouteur distribue les threads qui traitent les messages.</span><span class="sxs-lookup"><span data-stu-id="75f63-280">As messages arrive, the listener dispatches threads that process messages.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modèle logique**</span><span class="sxs-lookup"><span data-stu-id="75f63-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logical model**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-282">Deuxième étape d’un processus de conception d’application COM+, où le modèle conceptuel est divisé en niveaux logiques de l’architecture à trois niveaux, comme suit : la couche présentation, ou les services utilisateur ; la couche intermédiaire, ou services professionnels ; et la couche données, ou services de données.</span><span class="sxs-lookup"><span data-stu-id="75f63-282">The second step in a COM+ application design process, where the conceptual model is broken out into the logical tiers of the three-tier architecture, as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**événement faiblement couplé**</span><span class="sxs-lookup"><span data-stu-id="75f63-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**loosely coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-284">Événement dont l’expéditeur (éditeur) et le récepteur (abonné) ne sont pas étroitement liés.</span><span class="sxs-lookup"><span data-stu-id="75f63-284">An event whose sender (publisher) and receiver (subscriber) are not closely bound.</span></span> <span data-ttu-id="75f63-285">Dans un système d’événement faiblement couplé, tel que les événements COM+, les informations d’événements provenant de différents serveurs de publication sont conservées dans un magasin d’événements.</span><span class="sxs-lookup"><span data-stu-id="75f63-285">In a loosely coupled event system, such as COM+ Events, event information from different publishers is persisted in an event store.</span></span> <span data-ttu-id="75f63-286">Les abonnés interrogent ce magasin et sélectionnent les événements qu’ils souhaitent recevoir.</span><span class="sxs-lookup"><span data-stu-id="75f63-286">Subscribers query this store and select the events that they want to receive.</span></span> <span data-ttu-id="75f63-287">La sélection des informations d’événement dans le magasin d’événements crée un abonnement.</span><span class="sxs-lookup"><span data-stu-id="75f63-287">Selecting event information from the event store creates a subscription.</span></span> <span data-ttu-id="75f63-288">Lorsqu’un événement se produit, le système d’événements recherche dans cette base de données et recherche les abonnés intéressés, crée un nouvel objet de chaque classe intéressée et appelle une méthode sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="75f63-288">When an event occurs, the event system looks in this database and finds the interested subscribers, creates a new object of each interested class, and calls a method on that object.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**</span><span class="sxs-lookup"><span data-stu-id="75f63-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-290">Processus d’empaquetage et d’empaquetage des paramètres de méthode d’interface à travers les limites de thread ou de processus pour qu’un appel de procédure distante puisse avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="75f63-290">The process of packaging and unpackaging interface method parameters across thread or process boundaries so that a remote procedure call can take place.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**message Mover**</span><span class="sxs-lookup"><span data-stu-id="75f63-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**message mover**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-292">Élément architectural du service de composants en file d’attente COM+ qui déplace les messages ayant échoué vers leur file d’attente d’entrée pour qu’ils puissent être retentés.</span><span class="sxs-lookup"><span data-stu-id="75f63-292">The architectural element of the COM+ Queued Components service that moves failed messages back to their input queue so that they can be retried.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**événement méta**</span><span class="sxs-lookup"><span data-stu-id="75f63-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-event**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-294">Type d’événement utilisé par le système d’événements COM+ pour notifier les abonnés intéressés chaque fois que des objets de classe d’événements ou des abonnements sont créés, modifiés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="75f63-294">A type of event used by the COM+ Events system to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**méthode**</span><span class="sxs-lookup"><span data-stu-id="75f63-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**method**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-296">Dans la programmation COM, processus effectué par un objet COM lorsqu’il reçoit un message.</span><span class="sxs-lookup"><span data-stu-id="75f63-296">In COM-based programming, a process performed by a COM object when it receives a message.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**niveau intermédiaire**</span><span class="sxs-lookup"><span data-stu-id="75f63-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**middle tier**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-298">Dans le modèle d’architecture à trois niveaux pour les applications d’entreprise, la couche comprenant la logique métier et les règles de données.</span><span class="sxs-lookup"><span data-stu-id="75f63-298">In the three-tier architecture model for business applications, the layer comprising the business logic and data rules.</span></span> <span data-ttu-id="75f63-299">Les composants qui composent la couche intermédiaire peuvent être utilisés pour appliquer des règles d’entreprise, telles que des algorithmes métier, des réglementations juridiques ou gouvernementales, et des règles de données, qui sont conçues pour maintenir la cohérence des structures de données dans des bases de données spécifiques ou multiples.</span><span class="sxs-lookup"><span data-stu-id="75f63-299">The components that make up the middle tier can be used to enforce business rules, such as business algorithms, legal or governmental regulations, and data rules, which are designed to keep the data structures consistent within either specific or multiple databases.</span></span> <span data-ttu-id="75f63-300">Étant donné que ces composants de couche intermédiaire ne sont pas liés à un client spécifique, ils peuvent être utilisés par toutes les applications et peuvent être déplacés vers différents emplacements en fonction du temps de réponse et que d’autres règles requièrent.</span><span class="sxs-lookup"><span data-stu-id="75f63-300">Because these middle-tier components are not tied to a specific client, they can be used by all applications and can be moved to different locations as response time and other rules require.</span></span> <span data-ttu-id="75f63-301">Également appelée *couche de services d’entreprise* ou *couche de logique métier*.</span><span class="sxs-lookup"><span data-stu-id="75f63-301">Also called *business services layer* or *business logic tier*.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**processus de modèle mixte**</span><span class="sxs-lookup"><span data-stu-id="75f63-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**mixed model process**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-303">Processus qui a un cloisonnement multithread et un ou plusieurs cloisonnements à thread unique.</span><span class="sxs-lookup"><span data-stu-id="75f63-303">A process that has a multithreaded apartment and one or more single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span><span class="sxs-lookup"><span data-stu-id="75f63-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-305">Nom qui identifie de façon unique un objet COM.</span><span class="sxs-lookup"><span data-stu-id="75f63-305">A name that uniquely identifies a COM object.</span></span> <span data-ttu-id="75f63-306">De la même façon qu’un chemin d’accès identifie un fichier dans le système de fichiers, un moniker identifie un objet COM dans l’espace de noms du répertoire.</span><span class="sxs-lookup"><span data-stu-id="75f63-306">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**fichier. msi**</span><span class="sxs-lookup"><span data-stu-id="75f63-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi file**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-308">Fichier créé par l’outil d’administration Services de composants lorsque vous exportez une application COM+ ou un proxy d’application pour l’installation sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="75f63-308">A file created by the Component Services administrative tool when you export a COM+ application or application proxy for installation on another computer.</span></span> <span data-ttu-id="75f63-309">Le fichier. msi peut être installé sur n’importe quel client Windows à l’aide de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="75f63-309">The .msi file can be installed on any Windows-based client using Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modèle multithread cloisonné**</span><span class="sxs-lookup"><span data-stu-id="75f63-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**multithreaded apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-311">Modèle Apartment dans lequel tous les threads du processus qui ont été initialisés en tant que threads libres résident dans un seul cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="75f63-311">An apartment model in which all the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span> <span data-ttu-id="75f63-312">Par conséquent, il n’est pas nécessaire d’effectuer un marshaling entre les threads.</span><span class="sxs-lookup"><span data-stu-id="75f63-312">Therefore, there is no need to marshal between threads.</span></span> <span data-ttu-id="75f63-313">Les threads n’ont pas besoin de récupérer et de distribuer les messages, car COM n’utilise pas les messages de fenêtre dans ce modèle.</span><span class="sxs-lookup"><span data-stu-id="75f63-313">The threads need not retrieve and dispatch messages because COM does not use window messages in this model.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transaction imbriquée**</span><span class="sxs-lookup"><span data-stu-id="75f63-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**nested transaction**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-315">Une transaction secondaire lancée à partir d’une limite de transaction primaire ou parente existante.</span><span class="sxs-lookup"><span data-stu-id="75f63-315">A secondary transaction initiated from within an existing primary or parent transaction boundary.</span></span> <span data-ttu-id="75f63-316">La transaction principale n’est pas validée tant que toutes ses transactions subordonnées ou imbriquées ne sont pas validées.</span><span class="sxs-lookup"><span data-stu-id="75f63-316">The primary transaction does not commit until all of its subordinate, or nested, transactions commit.</span></span> <span data-ttu-id="75f63-317">COM+ ne prend pas en charge les transactions imbriquées.</span><span class="sxs-lookup"><span data-stu-id="75f63-317">COM+ does not support nested transactions.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modèle de cloisonnement neutre**</span><span class="sxs-lookup"><span data-stu-id="75f63-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**neutral apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-319">Modèle de thread dans lequel les objets suivent les instructions pour les cloisonnements multithread, mais peuvent s’exécuter sur n’importe quel type de thread.</span><span class="sxs-lookup"><span data-stu-id="75f63-319">A threading model in which objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="75f63-320">Le modèle de cloisonnement neutre est le modèle de thread recommandé pour les composants COM et les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-320">The neutral apartment model is the recommended threading model for COM components and COM+ applications.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**objet persistant**</span><span class="sxs-lookup"><span data-stu-id="75f63-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**persistent object**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-322">Objet COM qui peut enregistrer son état interne lorsqu’il y est invité par un client et qui est conforme aux normes définies par COM par le biais desquelles les clients peuvent demander l’initialisation, le chargement et l’enregistrement d’objets dans un magasin de données (par exemple, un fichier plat, un stockage structuré ou la mémoire).</span><span class="sxs-lookup"><span data-stu-id="75f63-322">A COM object that can save its internal state when asked to do so by a client and that conforms to COM-defined standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="75f63-323">Il incombe au client de gérer l’emplacement où les données persistantes de l’objet sont stockées, mais pas le format des données.</span><span class="sxs-lookup"><span data-stu-id="75f63-323">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interface d’objet persistant**</span><span class="sxs-lookup"><span data-stu-id="75f63-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**persistent object interface**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-325">Interface COM implémentée par un objet persistant.</span><span class="sxs-lookup"><span data-stu-id="75f63-325">A COM interface implemented by a persistent object.</span></span> <span data-ttu-id="75f63-326">Les clients utilisent des interfaces d’objets persistants pour indiquer à ces objets persistants quand et où stocker leur état.</span><span class="sxs-lookup"><span data-stu-id="75f63-326">Clients use persistent object interfaces to tell those persistent objects when and where to store their state.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interface de notification de phase zéro**</span><span class="sxs-lookup"><span data-stu-id="75f63-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**phase zero notification interface**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-328">Interface COM+ qui permet aux applications de détecter lorsqu’une transaction est prête à passer à un protocole de validation en deux phases afin de pouvoir effectuer les opérations de notification nécessaires et communiquer avec le gestionnaire de transactions lorsque les opérations sont terminées.</span><span class="sxs-lookup"><span data-stu-id="75f63-328">COM+ interface that allows applications to detect when a transaction is ready to proceed with a two-phase commit protocol so that it can perform the necessary notification operations and communicate to the transaction manager when the operations have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modèle physique**</span><span class="sxs-lookup"><span data-stu-id="75f63-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**physical model**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-330">Troisième et dernière étape du processus de conception de l’application COM+, où le développeur détermine où les composants résident physiquement et comment ils doivent être codés.</span><span class="sxs-lookup"><span data-stu-id="75f63-330">The third and final step in the COM+ application design process, where the developer determines where the components reside physically and how they are to be coded.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**lecteur**</span><span class="sxs-lookup"><span data-stu-id="75f63-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**player**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-332">Élément architectural du service de composants en file d’attente COM+ qui récupère le message à partir d’une file d’attente, puis charge l’objet serveur et les stubs d’interface standard pour démarshaler les données et appeler les méthodes serveur.</span><span class="sxs-lookup"><span data-stu-id="75f63-332">The architectural element of the COM+ Queued Components service that retrieves the message from a queue and then loads the server object and the standard interface stubs to unmarshal data and invoke server methods.</span></span> <span data-ttu-id="75f63-333">Le lecteur démarshale le contexte de sécurité du client côté serveur, puis appelle le composant serveur et effectue les mêmes appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="75f63-333">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="75f63-334">Les appels de méthode ne sont pas lus par le joueur jusqu’à ce que le composant client se termine et que la transaction qui a enregistré la méthode appelle valids.</span><span class="sxs-lookup"><span data-stu-id="75f63-334">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**niveau de présentation**</span><span class="sxs-lookup"><span data-stu-id="75f63-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**presentation tier**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-336">Dans le modèle d’architecture à trois niveaux pour les applications métier, couche qui présente les données à l’utilisateur et permet éventuellement la manipulation de données et l’entrée de données.</span><span class="sxs-lookup"><span data-stu-id="75f63-336">In the three-tier architecture model for business applications, the layer that presents data to the user and optionally permits data manipulation and data entry.</span></span> <span data-ttu-id="75f63-337">Les deux principaux types d’interface utilisateur pour la couche présentation sont l’application traditionnelle et l’application Web.</span><span class="sxs-lookup"><span data-stu-id="75f63-337">The two main types of user interface for the presentation tier are the traditional application and the Web-based application.</span></span> <span data-ttu-id="75f63-338">Également appelée *couche des services utilisateur*.</span><span class="sxs-lookup"><span data-stu-id="75f63-338">Also called *user services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**jeton d’accès principal**</span><span class="sxs-lookup"><span data-stu-id="75f63-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**primary access token**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-340">Décrit le contexte de sécurité du compte d’utilisateur associé à un processus.</span><span class="sxs-lookup"><span data-stu-id="75f63-340">Describes the security context of the user account associated with a process.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**gestionnaire proxy**</span><span class="sxs-lookup"><span data-stu-id="75f63-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-342">Dans le marshaling standard, composant qui gère tous les proxies d’interface pour un seul objet.</span><span class="sxs-lookup"><span data-stu-id="75f63-342">In standard marshaling, a component that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**Pseudo-objet**</span><span class="sxs-lookup"><span data-stu-id="75f63-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-object**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-344">Type d’objet contenu, tel qu’une sélection d’utilisateur dans un document, une plage de cellules dans une feuille de calcul ou une plage de caractères dans un document texte.</span><span class="sxs-lookup"><span data-stu-id="75f63-344">A type of contained object, such as a user selection in a document, a range of cells in a spreadsheet, or a range of characters in a text document.</span></span> <span data-ttu-id="75f63-345">Ce type d’objet est appelé Pseudo-objet, car il n’est pas traité comme un objet distinct tant qu’un utilisateur n’a pas marqué la sélection.</span><span class="sxs-lookup"><span data-stu-id="75f63-345">This type of object is called a pseudo-object because it isn't treated as a distinct object until a user marks the selection.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publication**</span><span class="sxs-lookup"><span data-stu-id="75f63-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publisher**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-347">Expéditeur d’un événement.</span><span class="sxs-lookup"><span data-stu-id="75f63-347">The sender of an event.</span></span> <span data-ttu-id="75f63-348">Dans l’architecture des événements COM+, le serveur de publication effectue l’appel de méthode pour initialiser un événement.</span><span class="sxs-lookup"><span data-stu-id="75f63-348">In the COM+ Events architecture, the publisher makes the method call to initiate an event.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker de file d’attente**</span><span class="sxs-lookup"><span data-stu-id="75f63-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**queue moniker**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-350">Moniker utilisé pour activer un composant mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="75f63-350">The moniker used to activate a queued component.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**condition de concurrence critique**</span><span class="sxs-lookup"><span data-stu-id="75f63-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-352">Dans une application multithread, condition qui se produit lorsque plusieurs threads accèdent à un élément de données sans coordination, ce qui peut entraîner des résultats incohérents, selon le thread qui atteint d’abord l’élément de données.</span><span class="sxs-lookup"><span data-stu-id="75f63-352">In a multithreaded application, a condition that occurs when multiple threads access a data item without coordination, possibly causing inconsistent results, depending on which thread reaches the data item first.</span></span> <span data-ttu-id="75f63-353">COM fournit certaines fonctions spécifiquement conçues pour éviter les conditions de concurrence dans les serveurs hors processus.</span><span class="sxs-lookup"><span data-stu-id="75f63-353">COM supplies some functions specifically designed to help avoid race conditions in out-of-process servers.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**grave**</span><span class="sxs-lookup"><span data-stu-id="75f63-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**recorder**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-355">Élément architectural du service de composants en file d’attente COM+ qui marshale le contexte de sécurité du client en message et enregistre tous les appels de méthode pour un objet.</span><span class="sxs-lookup"><span data-stu-id="75f63-355">The architectural element of the COM+ Queued Components service that marshals the client's security context into a message and records all of the method calls for an object.</span></span> <span data-ttu-id="75f63-356">L’enregistreur est un gestionnaire proxy fourni par le système qui sélectionne les interfaces à partir des interfaces de mise en file d’attente dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-356">The recorder is a system-provided proxy manager that selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**distributeur de ressources**</span><span class="sxs-lookup"><span data-stu-id="75f63-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**resource dispenser**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-358">Dans le modèle de programmation COM+, composant qui gère l’état partagé non durable pour le compte des composants d’application au sein d’un processus.</span><span class="sxs-lookup"><span data-stu-id="75f63-358">In the COM+ programming model, a component that manages nondurable shared state on behalf of the application components within a process.</span></span> <span data-ttu-id="75f63-359">Les distributeurs de ressources sont similaires aux gestionnaires de ressources, mais sans garantie de durabilité.</span><span class="sxs-lookup"><span data-stu-id="75f63-359">Resource dispensers are similar to resource managers but without the guarantee of durability.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Gestionnaire de ressources**</span><span class="sxs-lookup"><span data-stu-id="75f63-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-361">Service qui gère les données persistantes ou durables dans les bases de données, les files d’attente de messages durables ou les systèmes de fichiers transactionnels.</span><span class="sxs-lookup"><span data-stu-id="75f63-361">A service that manages persistent or durable data in databases, durable message queues, or transactional file systems.</span></span> <span data-ttu-id="75f63-362">Il s’agit du gestionnaire de ressources qui sait comment stocker des données et effectuer une récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="75f63-362">It is the resource manager that knows how to store data and perform disaster recovery.</span></span> <span data-ttu-id="75f63-363">Les applications serveur COM+ utilisent des gestionnaires de ressources pour maintenir l’État durable d’une application, par exemple l’enregistrement d’un inventaire, les commandes en attente et les comptes clients.</span><span class="sxs-lookup"><span data-stu-id="75f63-363">COM+ server applications use resource managers to maintain the durable state of an application, such as the record of inventory on hand, pending orders, and accounts receivable.</span></span> <span data-ttu-id="75f63-364">Les gestionnaires de ressources travaillent en collaboration avec le Distributed Transaction Coordinator Microsoft (DTC) pour garantir l’atomicité et l’isolation à une application.</span><span class="sxs-lookup"><span data-stu-id="75f63-364">Resource managers work in cooperation with the Microsoft Distributed Transaction Coordinator (DTC) to guarantee atomicity and isolation to an application.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**sécurité basée sur les rôles**</span><span class="sxs-lookup"><span data-stu-id="75f63-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**role-based security**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-366">Service de sécurité COM+ fourni pour les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-366">A COM+ security service provided for COM+ applications.</span></span> <span data-ttu-id="75f63-367">Un rôle représente une catégorie d’utilisateurs définie pour une application COM+ en vue de déterminer les autorisations d’accès aux ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="75f63-367">A role represents a category of users defined for a COM+ application for the purpose of determining access permissions to the application's resources.</span></span> <span data-ttu-id="75f63-368">Les rôles sont assignés par un développeur à des composants, des interfaces et des méthodes.</span><span class="sxs-lookup"><span data-stu-id="75f63-368">Roles are assigned by a developer to components, interfaces, and methods.</span></span> <span data-ttu-id="75f63-369">Les utilisateurs sont affectés par un administrateur aux rôles appropriés, ce qui permet à un utilisateur d’un rôle donné d’accéder à toutes les ressources auxquelles ce rôle est attribué.</span><span class="sxs-lookup"><span data-stu-id="75f63-369">Users are assigned by an administrator to appropriate roles, enabling a user within a given role to access any resources to which that role is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**objet racine**</span><span class="sxs-lookup"><span data-stu-id="75f63-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**root object**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-371">Le premier objet d’une transaction, appelé la racine de la transaction, est toujours placé dans une nouvelle limite transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="75f63-371">The first object of a transaction, called the root of the transaction, and always placed in a new transactional boundary.</span></span> <span data-ttu-id="75f63-372">Il ne peut y avoir qu’un seul objet racine dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="75f63-372">There can be only one root object in a transaction.</span></span> <span data-ttu-id="75f63-373">Tous les autres objets de la hiérarchie transactionnelle sous l’objet racine sont appelés objets intérieurs.</span><span class="sxs-lookup"><span data-stu-id="75f63-373">All other objects in the transactional hierarchy under the root object are called interior objects.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**Gestionnaire de transactions racine**</span><span class="sxs-lookup"><span data-stu-id="75f63-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**root transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-375">Gestionnaire de transactions du système qui initie une transaction.</span><span class="sxs-lookup"><span data-stu-id="75f63-375">The transaction manager on the system that initiates a transaction.</span></span> <span data-ttu-id="75f63-376">La transaction n’est pas finalisée tant que le gestionnaire de transactions racine n’a pas déterminé l’état de la transaction (validé ou abandonné).</span><span class="sxs-lookup"><span data-stu-id="75f63-376">The transaction is not finalized until the root transaction manager determines the transaction's status (either committed or aborted).</span></span>

</dd> <dt>

<span data-ttu-id="75f63-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**sémaphore**</span><span class="sxs-lookup"><span data-stu-id="75f63-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semaphore**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-378">Objet de noyau utilisé pour arbitrer l’accès à une ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="75f63-378">A kernel object used to arbitrate access to a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Gestionnaire de contrôle des services (SCM)**</span><span class="sxs-lookup"><span data-stu-id="75f63-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**service control manager (SCM)**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-380">Processus Microsoft Windows Server qui gère tous les services dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="75f63-380">A Microsoft Windows server process that manages all the services in the Windows registry.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Gestionnaire de propriétés partagées (SPM)**</span><span class="sxs-lookup"><span data-stu-id="75f63-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**shared property manager (SPM)**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-382">Dans com+, un distributeur de ressources que vous pouvez utiliser pour partager un État non persistant entre plusieurs objets au sein d’un processus serveur.</span><span class="sxs-lookup"><span data-stu-id="75f63-382">In Com+, a resource dispenser that you can use to share nonpersistent state among multiple objects within a server process.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**processus monothread**</span><span class="sxs-lookup"><span data-stu-id="75f63-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**single-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-384">Processus qui se compose d’un seul thread cloisonné, qui, à son tour, est constitué d’un seul thread.</span><span class="sxs-lookup"><span data-stu-id="75f63-384">A process that consists of just one single-threaded apartment, which in turn consists of exactly one thread.</span></span> <span data-ttu-id="75f63-385">Tous les objets COM qui résident dans un cloisonnement à thread unique peuvent recevoir des appels de méthode à partir du seul thread qui appartient à ce cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="75f63-385">All COM objects that live in a single-threaded apartment can receive method calls from only the one thread that belongs to that apartment.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span><span class="sxs-lookup"><span data-stu-id="75f63-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-387">Protocole simple basé sur XML permettant d’échanger des informations structurées et de type sur le Web.</span><span class="sxs-lookup"><span data-stu-id="75f63-387">A simple, XML-based protocol for exchanging structured and type information on the Web.</span></span> <span data-ttu-id="75f63-388">Le protocole ne contient aucune sémantique d’application ou de transport, ce qui le rend hautement modulaire et extensible.</span><span class="sxs-lookup"><span data-stu-id="75f63-388">The protocol contains no application or transport semantics, which makes it highly modular and extensible.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**fractionner l’inscription**</span><span class="sxs-lookup"><span data-stu-id="75f63-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**split registration**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-390">Pour les composants qui sont déjà des composants COM existants et qui sont utilisés dans l’environnement des services COM+, la disposition d’inscription dans laquelle l’aspect COM de base de l’inscription est stocké dans le Registre Windows et les nouveaux services et attributs COM+ (par exemple, les composants en file d’attente) sont stockées dans la base de données d’inscription COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-390">For components that are already existing COM components and are used in the COM+ services environment, the registration arrangement in which the basic COM aspect of the registration is stored in the Windows registry and new COM+ services and attributes (for example, Queued Components) are stored in the COM+ Registration Database.</span></span> <span data-ttu-id="75f63-391">Chaque attribut de composant est stocké dans le Registre Windows ou dans la base de données d’inscription COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-391">Each component attribute is stored in either the Windows registry or the COM+ Registration Database.</span></span> <span data-ttu-id="75f63-392">Les nouveaux composants COM sont inscrits exclusivement dans la base de données d’inscription COM+, avec une certaine duplication dans le Registre Windows afin que les outils existants puissent les utiliser.</span><span class="sxs-lookup"><span data-stu-id="75f63-392">New COM components are registered exclusively in the COM+ Registration Database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**avec état**</span><span class="sxs-lookup"><span data-stu-id="75f63-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**stateful**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-394">D’un système ou d’un processus qui surveille tous les détails de l’état d’une activité à laquelle il participe.</span><span class="sxs-lookup"><span data-stu-id="75f63-394">Of or pertaining to a system or process that monitors all details of the state of an activity in which it participates.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**sans état**</span><span class="sxs-lookup"><span data-stu-id="75f63-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**stateless**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-396">D’un système ou d’un processus qui participe à l’activité sans surveiller tous les détails de son état.</span><span class="sxs-lookup"><span data-stu-id="75f63-396">Of or pertaining to a system or process that participates in activity without monitoring all details of its state.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**masquage statique**</span><span class="sxs-lookup"><span data-stu-id="75f63-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**static cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-398">Forme de masquage où l’identité du client d’origine peut être présentée une seule fois à un serveur en aval, en définissant l’identité du client d’origine une seule fois sur le proxy.</span><span class="sxs-lookup"><span data-stu-id="75f63-398">A form of cloaking where the original client identity can be presented once to a downstream server, setting the original client identity once on the proxy.</span></span> <span data-ttu-id="75f63-399">Cette identité cliente est présentée sous la forme d’un jeton de thread de serveur qui sera utilisé lors des appels de méthode suivants.</span><span class="sxs-lookup"><span data-stu-id="75f63-399">This client identity is presented as a server thread token that will be used on subsequent method calls.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**côté**</span><span class="sxs-lookup"><span data-stu-id="75f63-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**subscriber**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-401">Récepteur d’un événement.</span><span class="sxs-lookup"><span data-stu-id="75f63-401">The receiver of an event.</span></span> <span data-ttu-id="75f63-402">Dans l’architecture des événements COM+, l’abonné reçoit les appels émis par le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="75f63-402">In the COM+ Events architecture, the subscriber receives the calls made by the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**objet d’abonnement**</span><span class="sxs-lookup"><span data-stu-id="75f63-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**subscription object**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-404">Dans le système d’événements COM+, objet créé par un abonné pour demander et gérer la remise des événements.</span><span class="sxs-lookup"><span data-stu-id="75f63-404">In the COM+ Events system, an object created by a subscriber to request and manage the delivery of events.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchronisationméthode**</span><span class="sxs-lookup"><span data-stu-id="75f63-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchronization**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-406">Dans COM+, service qui passe du composant au composant et interdit à plusieurs appelants d’entrer le composant à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="75f63-406">In COM+, a service that flows from component to component and prohibits more than one caller from entering the component at any given time.</span></span> <span data-ttu-id="75f63-407">La synchronisation détermine quand les threads peuvent distribuer des appels à un objet.</span><span class="sxs-lookup"><span data-stu-id="75f63-407">Synchronization determines when threads can dispatch calls to an object.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**modèle architectural à trois niveaux**</span><span class="sxs-lookup"><span data-stu-id="75f63-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**three-tier architectural model**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-409">L’infrastructure fondamentale pour le modèle de conception logique, segmente les composants d’une application en trois niveaux de services comme suit : la couche présentation, ou les services utilisateur ; la couche intermédiaire, ou services professionnels ; et la couche données, ou services de données.</span><span class="sxs-lookup"><span data-stu-id="75f63-409">The fundamental framework for the logical design model, segments an application's components into three tiers of services as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span> <span data-ttu-id="75f63-410">Ces niveaux ne correspondent pas nécessairement à des emplacements physiques sur différents ordinateurs sur un réseau, mais plutôt à des couches logiques de l’application.</span><span class="sxs-lookup"><span data-stu-id="75f63-410">These tiers do not necessarily correspond to physical locations on various computers on a network, but rather to logical layers of the application.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**événement étroitement couplé**</span><span class="sxs-lookup"><span data-stu-id="75f63-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**tightly coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-412">Événement dont l’expéditeur (éditeur) et le récepteur (abonné) sont étroitement liés.</span><span class="sxs-lookup"><span data-stu-id="75f63-412">An event whose sender (publisher) and receiver (subscriber) are closely bound.</span></span> <span data-ttu-id="75f63-413">Dans un système d’événements étroitement couplé, le serveur de publication est fourni avec une interface sur laquelle appeler une méthode quand une modification se produit.</span><span class="sxs-lookup"><span data-stu-id="75f63-413">In a tightly coupled event system, the publisher is provided with an interface on which to call a method when a change occurs.</span></span> <span data-ttu-id="75f63-414">L’abonné sait à partir de quel éditeur demander une notification et les interfaces qui sont exposées.</span><span class="sxs-lookup"><span data-stu-id="75f63-414">The subscriber knows which publisher to request notification from and the interfaces that are exposed.</span></span> <span data-ttu-id="75f63-415">Un système d’événements étroitement couplé nécessite que le serveur de publication et l’abonné s’exécutent à tout moment.</span><span class="sxs-lookup"><span data-stu-id="75f63-415">A tightly coupled event system requires that both the publisher and the subscriber are running at all times.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**Journal des traces**</span><span class="sxs-lookup"><span data-stu-id="75f63-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**trace log**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-417">Fichier journal généré automatiquement par le Distributed Transaction Coordinator Microsoft qui affiche les données relatives à une ou plusieurs transactions distribuées.</span><span class="sxs-lookup"><span data-stu-id="75f63-417">A log file automatically generated by the Microsoft Distributed Transaction Coordinator that shows data related to one or more distributed transactions.</span></span> <span data-ttu-id="75f63-418">Des exemples de données dans un journal des traces sont l’ID de transaction, le temps de transaction et les messages indiquant le résultat de la transaction.</span><span class="sxs-lookup"><span data-stu-id="75f63-418">Examples of data in a trace log are transaction ID, transaction time, and messages indicating the transaction outcome.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**libellé**</span><span class="sxs-lookup"><span data-stu-id="75f63-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transaction**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-420">Unité de travail dans laquelle une série d’opérations connexes se produisent pendant un processus d’application.</span><span class="sxs-lookup"><span data-stu-id="75f63-420">A unit of work in which a series of related operations occur during an application process.</span></span> <span data-ttu-id="75f63-421">Une transaction s’exécute exactement une fois et est atomique : soit la totalité du travail est effectuée, soit aucune d’entre elles n’est.</span><span class="sxs-lookup"><span data-stu-id="75f63-421">A transaction executes exactly once and is atomic—either all of the work is done or none of it is.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Protocole Internet de transaction (TIP)**</span><span class="sxs-lookup"><span data-stu-id="75f63-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (TIP)**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-423">Transaction Internet Protocol est un protocole de validation en deux phases standard qui permet aux gestionnaires de transactions hétérogènes de coordonner les transactions distribuées, en particulier sur Internet.</span><span class="sxs-lookup"><span data-stu-id="75f63-423">Transaction Internet Protocol is a standard two-phase commit protocol that enables heterogeneous transaction managers to coordinate distributed transactions, especially over the Internet.</span></span> <span data-ttu-id="75f63-424">Le protocole de validation en deux phases TIP est simple à implémenter et est indépendant du protocole de communication entre applications, de sorte qu’il peut être utilisé avec n’importe quel protocole d’application, en particulier HTTP.</span><span class="sxs-lookup"><span data-stu-id="75f63-424">The TIP two-phase commit protocol is simple to implement and is independent of the application-to-application communications protocol, such that it may be used with any application protocol but especially HTTP.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**Gestionnaire de transactions**</span><span class="sxs-lookup"><span data-stu-id="75f63-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-426">Partie du Distributed Transaction Coordinator Microsoft (DTC) qui s’exécute sur chaque ordinateur participant à une transaction distribuée et qui gère les activités liées à la validation ou à l’abandon de cette partie de la transaction.</span><span class="sxs-lookup"><span data-stu-id="75f63-426">The part of the Microsoft Distributed Transaction Coordinator (DTC) that executes on each computer participating in a distributed transaction and manages the activities related to committing or aborting that part of the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**application de traitement des transactions**</span><span class="sxs-lookup"><span data-stu-id="75f63-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**transaction processing application**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-428">Collection d’opérations de transaction qui automatisent une tâche d’entreprise donnée.</span><span class="sxs-lookup"><span data-stu-id="75f63-428">A collection of transaction operations that automate a given business task.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**système de traitement des transactions**</span><span class="sxs-lookup"><span data-stu-id="75f63-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**transaction processing system**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-430">Système complet, comprenant à la fois le matériel et les logiciels de l’ordinateur, qui héberge une application de traitement des transactions pour effectuer des transactions de routine nécessaires pour mener à bien l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="75f63-430">A complete system, comprising both computer hardware and software, that hosts a transaction processing application to perform routine transactions necessary to conduct business.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**Protocole de validation en deux phases**</span><span class="sxs-lookup"><span data-stu-id="75f63-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**two-phase commit protocol**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-432">Un protocole utilisé uniquement dans les transactions distribuées garantit que le résultat d’une transaction est cohérent dans l’ensemble des gestionnaires de transactions participant à la transaction.</span><span class="sxs-lookup"><span data-stu-id="75f63-432">A protocol used only in distributed transactions, ensures that the outcome of a transaction is consistent across all transaction managers participating in the transaction.</span></span> <span data-ttu-id="75f63-433">Le protocole fonctionne en deux phases distinctes pour valider ou abandonner une transaction : la phase 1 évalue la condition de chaque gestionnaire de ressources et la phase 2 termine la transaction.</span><span class="sxs-lookup"><span data-stu-id="75f63-433">The protocol operates in two distinct phases to ultimately commit or abort a transaction: phase one evaluates the condition of each resource manager, and phase two completes the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**composant non configuré**</span><span class="sxs-lookup"><span data-stu-id="75f63-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**unconfigured component**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-435">Composant COM qui n’a pas été configuré dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-435">A COM component that has not been configured within the COM+ catalog.</span></span> <span data-ttu-id="75f63-436">Les composants non configurés ne peuvent pas utiliser les services COM+.</span><span class="sxs-lookup"><span data-stu-id="75f63-436">Unconfigured components cannot make use of COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**déplacement**</span><span class="sxs-lookup"><span data-stu-id="75f63-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**whereabouts**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-438">Pour les transactions DTC, structure de données opaque qui représente l’adresse du gestionnaire de transactions du gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="75f63-438">For DTC transactions, an opaque data structure that represents the address of the resource manager's transaction manager.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfaces XA**</span><span class="sxs-lookup"><span data-stu-id="75f63-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA interfaces**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-440">Ensemble standard d’interfaces de programmation qui permettent aux développeurs d’applications COM+ d’accéder aux bases de données compatibles XA et de créer des gestionnaires de ressources qui fonctionnent avec les bases de données relationnelles, la mise en file d’attente des messages, les fichiers transactionnels et les bases de données orientées objet.</span><span class="sxs-lookup"><span data-stu-id="75f63-440">A standard set of programming interfaces that allow COM+ application developers to access XA-compliant databases and create resource managers that operate with relational databases, message queuing, transactional files, and object-oriented databases.</span></span> <span data-ttu-id="75f63-441">Bien que Microsoft ne prenne pas directement en charge le protocole XA, Microsoft prend en charge les fonctions de traduction entre les transactions OLE et XA.</span><span class="sxs-lookup"><span data-stu-id="75f63-441">Although Microsoft does not directly support the XA protocol, Microsoft does support translation facilities between OLE transactions and XA.</span></span>

</dd> <dt>

<span data-ttu-id="75f63-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Services Web XML**</span><span class="sxs-lookup"><span data-stu-id="75f63-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML web services**</span></span>
</dt> <dd>

<span data-ttu-id="75f63-443">Unités de logique d’application fournissant des données et des services à d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="75f63-443">Units of application logic providing data and services to other applications.</span></span> <span data-ttu-id="75f63-444">Les applications accèdent aux services Web XML via des protocoles Web standard, tels que SOAP.</span><span class="sxs-lookup"><span data-stu-id="75f63-444">Applications access XML web services through standard Web protocols, such as SOAP.</span></span>

</dd> </dl>

 

 
