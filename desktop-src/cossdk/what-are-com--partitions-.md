---
description: Une partition COM+ est un conteneur logique qui permet aux applications de s’exécuter indépendamment des autres configurations de ces applications.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: Que sont les partitions COM+ ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104116010"
---
# <a name="what-are-com-partitions"></a><span data-ttu-id="0ba9d-103">Que sont les partitions COM+ ?</span><span class="sxs-lookup"><span data-stu-id="0ba9d-103">What Are COM+ Partitions?</span></span>

<span data-ttu-id="0ba9d-104">Une partition COM+ est un conteneur logique qui permet aux applications de s’exécuter indépendamment des autres configurations de ces applications.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-104">A COM+ partition is a logical container that allows applications to run independently of other configurations of those applications.</span></span> <span data-ttu-id="0ba9d-105">Chaque configuration d’une application est installée dans une partition distincte et peut être gérée séparément, en fonction des besoins spécifiques de ses utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-105">Each configuration of an application is installed into a separate partition and can be separately managed, according to the specific needs of its users.</span></span>

<span data-ttu-id="0ba9d-106">Au cours de l’activation d’un composant COM+, le service partitions détermine la configuration du composant à activer, en fonction de l’identité de l’utilisateur qui demande l’activation du composant.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-106">During activation of a COM+ component, the partitions service determines which configuration of the component to activate, based on the identity of the user requesting the component activation.</span></span> <span data-ttu-id="0ba9d-107">Par exemple, une organisation unique qui possède deux groupes, production et formation distincts, peut implémenter des partitions COM+ pour permettre aux deux groupes d’utiliser différentes configurations d’une application COM+ sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-107">For example, a single organization that has two separate groups, Production and Training, could implement COM+ partitions as a way to allow the two groups to use different configurations of a COM+ application on the same computer.</span></span>

<span data-ttu-id="0ba9d-108">**Windows XP :** La possibilité de créer, de configurer ou de déléguer des partitions COM+ n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-108">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="0ba9d-109">La partition globale est la seule partition COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-109">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="0ba9d-110">**Windows 2000 :** Le service partitions COM+ n’est pas disponible dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-110">**Windows 2000:** The COM+ partitions service is not available in Windows 2000.</span></span>

## <a name="benefits-of-using-com-partitions"></a><span data-ttu-id="0ba9d-111">Avantages de l’utilisation des partitions COM+</span><span class="sxs-lookup"><span data-stu-id="0ba9d-111">Benefits of Using COM+ Partitions</span></span>

<span data-ttu-id="0ba9d-112">L’utilisation de partitions COM+ offre plusieurs avantages, notamment les suivants :</span><span class="sxs-lookup"><span data-stu-id="0ba9d-112">The use of COM+ partitions offers several advantages, including the following:</span></span>

-   <span data-ttu-id="0ba9d-113">Les organisations peuvent réduire le coût total de possession (TCO) en utilisant moins de serveurs d’applications physiques pour prendre en charge les utilisateurs qui ont besoin de plusieurs configurations d’applications.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-113">Organizations can lower their total cost of ownership (TCO) by using fewer physical application servers to support users who need multiple application configurations.</span></span>
-   <span data-ttu-id="0ba9d-114">La surcharge administrative est réduite.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-114">Administrative overhead is reduced.</span></span> <span data-ttu-id="0ba9d-115">Au lieu de devoir configurer et gérer plusieurs ordinateurs, les administrateurs doivent uniquement configurer et gérer plusieurs partitions sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-115">Instead of having to configure and manage multiple computers, administrators need only configure and manage multiple partitions on the same computer.</span></span> <span data-ttu-id="0ba9d-116">En outre, les partitions peuvent être gérées par programme par le biais de l’ajout d’une nouvelle interface de programmation COM+.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-116">Furthermore, partitions can be managed programmatically through the addition of a new COM+ programming interface.</span></span>
-   <span data-ttu-id="0ba9d-117">La sécurité peut être implémentée et gérée sur la base d’une partition par partition pour les utilisateurs locaux, les utilisateurs de domaine et les unités d’organisation (UO).</span><span class="sxs-lookup"><span data-stu-id="0ba9d-117">Security can be implemented and managed on a partition-by-partition basis for local users, domain users, and organizational units (OUs).</span></span>
-   <span data-ttu-id="0ba9d-118">Les programmeurs et les administrateurs peuvent utiliser les outils de développement et d’administration de Microsoft, tels que les SDK Windows, Active Directory les utilisateurs et les ordinateurs, ainsi que l’outil d’administration Services de composants, pour gérer les partitions COM+.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-118">Programmers and administrators can use Microsoft's development and administrative tools—such as the Windows SDK, Active Directory Users and Computers, and Component Services administrative tool—to manage COM+ partitions.</span></span> <span data-ttu-id="0ba9d-119">La fonctionnalité partitions est entièrement intégrée à ces outils.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-119">The partitions feature is fully integrated into these tools.</span></span>

## <a name="primary-usage-scenario"></a><span data-ttu-id="0ba9d-120">Scénario d’utilisation principale</span><span class="sxs-lookup"><span data-stu-id="0ba9d-120">Primary Usage Scenario</span></span>

<span data-ttu-id="0ba9d-121">La principale raison pour laquelle les clients peuvent déployer la fonctionnalité partitions COM+ consiste à héberger des applications Web.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-121">A primary reason for customers to deploy the COM+ partitions feature is to host Web-based applications.</span></span> <span data-ttu-id="0ba9d-122">Supposons, par exemple, qu’une petite entreprise de logiciels développe une application COM+ pour une utilisation par le personnel hospitalier.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-122">For example, suppose a small software company develops a COM+ application for use by hospital personnel.</span></span> <span data-ttu-id="0ba9d-123">L’application, qui est une application Web distribuée, offre aux hôpitaux un moyen de stocker et de récupérer les dossiers médicaux des patients à l’aide d’une base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-123">The application, which is a distributed Web-based application, provides a way for hospitals to store and retrieve patient medical records using a SQL Server database.</span></span>

<span data-ttu-id="0ba9d-124">Supposons que l’entreprise logicielle a trois clients : hôpital A, hôpital B et hôpital C. Tandis que chaque client exécute le côté client de l’application COM+ localement sur ses ordinateurs de bureau, le côté serveur de l’application COM+ réside sur le serveur Web interne de l’éditeur de logiciels et est accessible par ses clients via le Web.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-124">Suppose the software company has three customers: Hospital A, Hospital B, and Hospital C. While each customer runs the client side of the COM+ application locally on its desktop computers, the server side of the COM+ application resides on the software company's in-house web server and is accessed by its customers via the Web.</span></span>

<span data-ttu-id="0ba9d-125">Étant donné que chaque hôpital a son propre ensemble d’exigences de stockage et de récupération et son propre ensemble de données de patients personnalisées, l’entreprise logicielle doit fournir un moyen de plusieurs configurations de la partie serveur de l’application à exécuter simultanément sur le serveur Web.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-125">Because each hospital has its own set of storage and retrieval requirements and its own set of customized patient data, the software company must provide a way for multiple configurations of the server part of the application to be executed simultaneously on the web server.</span></span> <span data-ttu-id="0ba9d-126">Les partitions COM+ offrent une solution à ce problème.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-126">COM+ partitions provide a solution to this problem.</span></span>

<span data-ttu-id="0ba9d-127">L’illustration suivante montre le scénario des partitions pour l’application COM+ de l’éditeur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="0ba9d-127">The following illustration shows the partitions scenario for the software company's COM+ application.</span></span>

![Diagramme illustrant un scénario de partitions pour une application COM+, avec une application cliente pour l’application serveur à la base de données SQL Server.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a><span data-ttu-id="0ba9d-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ba9d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ba9d-130">Restrictions relatives à la conception d’applications</span><span class="sxs-lookup"><span data-stu-id="0ba9d-130">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="0ba9d-131">Composants et partitions COM+ en file d’attente</span><span class="sxs-lookup"><span data-stu-id="0ba9d-131">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="0ba9d-132">Implémentation de la partition</span><span class="sxs-lookup"><span data-stu-id="0ba9d-132">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="0ba9d-133">Inscription et activation de composants dans des partitions</span><span class="sxs-lookup"><span data-stu-id="0ba9d-133">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



