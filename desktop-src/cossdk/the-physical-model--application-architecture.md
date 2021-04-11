---
description: Une fois les modèles conceptuels et logiques terminés, vous pouvez prendre des décisions sur l’implémentation physique de l’application.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'Modèle physique : architecture de l’application'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111426"
---
# <a name="the-physical-model-application-architecture"></a><span data-ttu-id="79659-103">Modèle physique : architecture de l’application</span><span class="sxs-lookup"><span data-stu-id="79659-103">The Physical Model: Application Architecture</span></span>

<span data-ttu-id="79659-104">Une fois les modèles conceptuels et logiques terminés, vous pouvez prendre des décisions sur l’implémentation physique de l’application.</span><span class="sxs-lookup"><span data-stu-id="79659-104">After the conceptual and logical models are complete, you can make decisions on the physical implementation of the application.</span></span> <span data-ttu-id="79659-105">Pour créer le modèle physique, vous devez comprendre où se trouvent les différents services de l’application et comment ils doivent être implémentés.</span><span class="sxs-lookup"><span data-stu-id="79659-105">To create the physical model, you must understand where the various services of the application should be located and how they should be implemented.</span></span> <span data-ttu-id="79659-106">Il est recommandé de déterminer l’emplacement des différents services avant d’implémenter les services.</span><span class="sxs-lookup"><span data-stu-id="79659-106">Determining where various services reside should come before how the services will be implemented.</span></span>

<span data-ttu-id="79659-107">Une règle de base pour déterminer l’emplacement des différents services est la suivante : placer le composant dans lequel il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="79659-107">One basic rule for determining where various services reside is this: Put the component where it is being used.</span></span> <span data-ttu-id="79659-108">Si, par exemple, un composant affiche des informations pour le client de base, il doit se trouver sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="79659-108">If, for example, a component displays information for the base client, it should go on the user's computer.</span></span> <span data-ttu-id="79659-109">Si un composant valide des informations à partir du client de base, il doit également résider sur l’ordinateur du client de base.</span><span class="sxs-lookup"><span data-stu-id="79659-109">If a component validates information from the base client, it should also reside on the base client's computer.</span></span> <span data-ttu-id="79659-110">Si un composant met à jour des informations dans une base de données, il doit résider sur le serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="79659-110">If a component updates information in a database, it should reside on the database server.</span></span>

<span data-ttu-id="79659-111">Il existe, bien sûr, des considérations supplémentaires qui rendent des exceptions à cette règle.</span><span class="sxs-lookup"><span data-stu-id="79659-111">There are, of course, additional considerations that make exceptions to this rule.</span></span> <span data-ttu-id="79659-112">Les problèmes de performances et de sécurité peuvent également dicter l’emplacement d’un composant.</span><span class="sxs-lookup"><span data-stu-id="79659-112">Performance and security issues can also dictate where a component is located.</span></span> <span data-ttu-id="79659-113">Tenez compte des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="79659-113">Consider the following:</span></span>

-   <span data-ttu-id="79659-114">Un composant va-t-il changer fréquemment, ce qui complique la distribution des mises à jour ?</span><span class="sxs-lookup"><span data-stu-id="79659-114">Is a component going to change frequently, making distributing updates difficult?</span></span>
-   <span data-ttu-id="79659-115">Le composant sera-t-il utilisé par d’autres applications, par exemple un composant de vérification de sécurité courant ?</span><span class="sxs-lookup"><span data-stu-id="79659-115">Will the component be used by other applications, such as a common security verification component?</span></span>
-   <span data-ttu-id="79659-116">Le composant effectue-t-il des calculs longs ou exécute des fonctions, telles que l’impression, qui peuvent être déchargées sur un serveur ?</span><span class="sxs-lookup"><span data-stu-id="79659-116">Does the component make lengthy calculations or performs functions, such as printing, that can be offloaded to a server?</span></span>
-   <span data-ttu-id="79659-117">La sécurité d’un composant peut-elle être améliorée en la plaçant sur un serveur ?</span><span class="sxs-lookup"><span data-stu-id="79659-117">Can the security of a component be enhanced by placing it on a server?</span></span>

<span data-ttu-id="79659-118">Localiser correctement les composants d’une application peut également isoler l’équipe de développement du recodage coûteux si le système ou l’emplacement des données change.</span><span class="sxs-lookup"><span data-stu-id="79659-118">Properly locating components of an application can also insulate the development team from costly recoding if the system or the location of the data changes.</span></span> <span data-ttu-id="79659-119">Par exemple, en plaçant les règles d’accès aux données dans une couche de données plutôt que dans des procédures stockées, il est plus facile d’isoler l’application de la dépendance sur un SGBD spécifique.</span><span class="sxs-lookup"><span data-stu-id="79659-119">For example, by putting the data access rules in a data layer rather than in stored procedures, the application is more easily insulated from dependence on a specific DBMS.</span></span> <span data-ttu-id="79659-120">Non seulement les modifications sont confinées et les tests sont compartimentés, mais les sources de données peuvent être modifiées et les données peuvent être distribuées sans modification radicale de l’application.</span><span class="sxs-lookup"><span data-stu-id="79659-120">Not only are changes confined and testing compartmentalized, but data sources can be changed and data can be distributed without fundamentally changing the application.</span></span>

<span data-ttu-id="79659-121">Enfin, la localisation des composants doit tirer parti de l’efficacité du système.</span><span class="sxs-lookup"><span data-stu-id="79659-121">Finally, locating components should take advantage of system efficiencies.</span></span> <span data-ttu-id="79659-122">Il est temps et économique de placer des objets métier dans des emplacements centralisés sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="79659-122">It is time and cost-effective to place business objects in centralized locations on the network.</span></span> <span data-ttu-id="79659-123">Les objets peuvent être partagés entre les applications, et les tests unitaires peuvent être effectués avant le déploiement des composants.</span><span class="sxs-lookup"><span data-stu-id="79659-123">Objects can be shared among applications, and unit testing can be done before any components are deployed.</span></span> <span data-ttu-id="79659-124">Les coûts de maintenance peuvent également être réduits, car les modifications de règles ne se produisent qu’à un seul point.</span><span class="sxs-lookup"><span data-stu-id="79659-124">Maintenance costs can also be decreased because rule changes occur only at a single point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79659-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79659-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79659-126">Modèle conceptuel : exigences de l’application</span><span class="sxs-lookup"><span data-stu-id="79659-126">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
</dt> <dt>

[<span data-ttu-id="79659-127">Modèle logique : définition et planification de l’application</span><span class="sxs-lookup"><span data-stu-id="79659-127">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



