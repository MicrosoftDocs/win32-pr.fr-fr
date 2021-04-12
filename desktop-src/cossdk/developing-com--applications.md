---
description: Lors du développement d’applications COM+, les principales tâches incluent la conception de composants COM pour encapsuler la logique d’application et l’intégration de ces composants dans une application COM+, la création de l’application COM+ et l’administration de l’application par le biais du déploiement et de la maintenance.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Développement d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523244"
---
# <a name="developing-com-applications"></a><span data-ttu-id="9ecb7-103">Développement d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="9ecb7-103">Developing COM+ Applications</span></span>

<span data-ttu-id="9ecb7-104">Lors du développement d’applications COM+, les principales tâches incluent la conception de composants COM pour encapsuler la logique d’application et l’intégration de ces composants dans une application COM+, la création de l’application COM+ et l’administration de l’application par le biais du déploiement et de la maintenance.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-104">When developing COM+ applications, the principal tasks include designing COM components to encapsulate application logic and integrating these components into a COM+ application, creating the COM+ application, and administering the application through deployment and maintenance.</span></span>

## <a name="designing-com-components"></a><span data-ttu-id="9ecb7-105">Conception de composants COM</span><span class="sxs-lookup"><span data-stu-id="9ecb7-105">Designing COM Components</span></span>

<span data-ttu-id="9ecb7-106">Les étapes suivantes décrivent une procédure générale pour une bonne conception de composant :</span><span class="sxs-lookup"><span data-stu-id="9ecb7-106">The following steps describe a general procedure for good component design:</span></span>

1.  <span data-ttu-id="9ecb7-107">Définissez les classes COM et les classes d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-107">Define the COM classes and implementation classes.</span></span>
2.  <span data-ttu-id="9ecb7-108">Regroupez les classes en composants.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-108">Group the classes into components.</span></span>
3.  <span data-ttu-id="9ecb7-109">Sélectionnez l’ensemble des services COM+ pour votre composant, même si vous ne les spécifiez pas tous lors du développement du composant.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-109">Select the set of COM+ services for your component, even if you do not specify all of them when developing the component.</span></span> <span data-ttu-id="9ecb7-110">Ces services peuvent être spécifiés ultérieurement à l’aide de l’outil d’administration Services de composants ou du modèle objet d’administration COM+ (pour plus d’informations sur le modèle objet d’administration COM+, consultez automatisation de l' [administration com+](automating-com--administration.md) ).</span><span class="sxs-lookup"><span data-stu-id="9ecb7-110">These services can later be specified using the Component Services administrative tool or the COM+ administration object model (See [Automating COM+ Administration](automating-com--administration.md) for more information about the COM+ administration object model.)</span></span>

## <a name="creating-the-com-application"></a><span data-ttu-id="9ecb7-111">Création de l’application COM+</span><span class="sxs-lookup"><span data-stu-id="9ecb7-111">Creating the COM+ Application</span></span>

<span data-ttu-id="9ecb7-112">Après avoir conçu les composants COM, le développeur intègre les composants dans une application COM+ et configure l’application.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-112">After designing the COM components, the developer integrates the components into a COM+ application and configures the application.</span></span> <span data-ttu-id="9ecb7-113">Les étapes suivantes décrivent le processus :</span><span class="sxs-lookup"><span data-stu-id="9ecb7-113">The following steps describe the process:</span></span>

1.  <span data-ttu-id="9ecb7-114">Intégrez les composants dans une application COM+.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-114">Integrate the components into a COM+ application.</span></span> <span data-ttu-id="9ecb7-115">Vous pouvez intégrer les composants à une application COM+ existante ou créer une nouvelle application (vide) pour les composants.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-115">You can integrate the components into an existing COM+ application or create a new (empty) application for the components.</span></span> <span data-ttu-id="9ecb7-116">(Consultez [création d’applications com+](creating-com--applications.md).)</span><span class="sxs-lookup"><span data-stu-id="9ecb7-116">(See [Creating COM+ Applications](creating-com--applications.md).)</span></span>
2.  <span data-ttu-id="9ecb7-117">Spécifiez le jeu d’attributs approprié pour chacune des classes (le cas échéant) et, s’il n’est pas spécifié dans l’outil de développement.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-117">Specify the correct set of attributes for each of the classes (if any, and if not specified in the development tool).</span></span> <span data-ttu-id="9ecb7-118">Ces attributs expriment les dépendances des composants sur les services COM+ sur lesquels l’implémentation peut s’appuyer (par exemple, les transactions, les composants en file d’attente, la sécurité, le regroupement d’objets et l’activation juste-à-temps).</span><span class="sxs-lookup"><span data-stu-id="9ecb7-118">These attributes express the components dependencies on any COM+ services its implementation might rely on (for example, transactions, Queued Components, Security, Object Pooling, and Just-in-Time Activation).</span></span>
3.  <span data-ttu-id="9ecb7-119">Configurez l’infrastructure de sécurité (rôles et attribution de rôles aux classes, interfaces et méthodes).</span><span class="sxs-lookup"><span data-stu-id="9ecb7-119">Set up the security framework (roles and assignment of roles to classes, interfaces, and methods).</span></span>
4.  <span data-ttu-id="9ecb7-120">Configurez des attributs spécifiques à l’environnement sur des classes et des applications (par exemple, la taille du pool d’objets par défaut).</span><span class="sxs-lookup"><span data-stu-id="9ecb7-120">Configure environment-specific attributes on classes and applications (the default object pool size, for example).</span></span> <span data-ttu-id="9ecb7-121">Ces attributs spécifiques à l’environnement peuvent être définis (ou modifiés) ultérieurement par l’administrateur système.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-121">These environment-specific attributes can later be set (or modified) by the system administrator.</span></span>
5.  <span data-ttu-id="9ecb7-122">Exportez l’application pour la redistribution et le déploiement.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-122">Export the application for redistribution and deployment.</span></span>

<span data-ttu-id="9ecb7-123">Pour plus d’informations sur les étapes de la conception d’applications distribuées, consultez [conception d’applications com+](designing-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="9ecb7-123">For more detailed information on the steps in designing distributed applications, see [Designing COM+ Applications](designing-com--applications.md).</span></span>

## <a name="administering-com-applications"></a><span data-ttu-id="9ecb7-124">Administration des applications COM+</span><span class="sxs-lookup"><span data-stu-id="9ecb7-124">Administering COM+ Applications</span></span>

<span data-ttu-id="9ecb7-125">En général, un développeur remet une application COM+ partiellement configurée à l’administrateur système.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-125">Typically, a developer delivers a partially configured COM+ application to the system administrator.</span></span> <span data-ttu-id="9ecb7-126">L’administrateur peut ensuite personnaliser l’application pour un ou plusieurs environnements spécifiques (par exemple, en ajoutant des comptes d’utilisateur dans des rôles et des noms de serveurs dans un cluster d’applications).</span><span class="sxs-lookup"><span data-stu-id="9ecb7-126">The administrator can then customize the application for one or more specific environments (for example, by adding user accounts in roles and server names in an application cluster).</span></span> <span data-ttu-id="9ecb7-127">Les tâches de l’administrateur sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ecb7-127">The administrator's tasks include the following:</span></span>

-   <span data-ttu-id="9ecb7-128">Installation de l’application COM+ partiellement configurée sur un ordinateur d’administration.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-128">Installing the partially configured COM+ application on an administrative computer.</span></span>
-   <span data-ttu-id="9ecb7-129">Fournir des attributs spécifiques à l’environnement, tels que les membres du rôle et la taille du pool d’objets.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-129">Providing environment-specific attributes, such as role members and object pool size.</span></span>
-   <span data-ttu-id="9ecb7-130">Réexportation de l’application COM+ entièrement configurée.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-130">Re-exporting the fully configured COM+ application.</span></span>
-   <span data-ttu-id="9ecb7-131">Création d’un proxy d’application (si l’application doit être accessible à distance).</span><span class="sxs-lookup"><span data-stu-id="9ecb7-131">Creating an application proxy (if the application is to be accessed remotely).</span></span>

<span data-ttu-id="9ecb7-132">Une fois qu’une application est entièrement configurée pour un environnement spécifique, l’administrateur peut la déployer sur des ordinateurs de test ou de production.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-132">After an application is fully configured for a specific environment, the administrator can then deploy it on test or production machines.</span></span> <span data-ttu-id="9ecb7-133">Cela implique l’installation de l’application COM+ entièrement configurée sur un ou plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-133">This involves installing the fully configured COM+ application on one or more computers.</span></span>

<span data-ttu-id="9ecb7-134">Pour plus d’informations sur les procédures d’administration COM+, consultez l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="9ecb7-134">For detailed information on COM+ administration procedures, see the Component Services administrative tool.</span></span>

 

 



