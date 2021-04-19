---
description: Lorsqu’il est installé sur un serveur d’applications, COM+ crée automatiquement une partition, appelée partition globale.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implémentation de la partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514128"
---
# <a name="partition-implementation"></a><span data-ttu-id="b2018-103">Implémentation de la partition</span><span class="sxs-lookup"><span data-stu-id="b2018-103">Partition Implementation</span></span>

<span data-ttu-id="b2018-104">Lorsqu’il est installé sur un serveur d’applications, COM+ crée automatiquement une partition, appelée *partition globale*.</span><span class="sxs-lookup"><span data-stu-id="b2018-104">When installed on an application server, COM+ automatically creates a partition, known as the *global partition*.</span></span> <span data-ttu-id="b2018-105">La partition globale comprend un ensemble standard d’applications COM+.</span><span class="sxs-lookup"><span data-stu-id="b2018-105">The global partition includes a standard set of COM+ applications.</span></span> <span data-ttu-id="b2018-106">Les applications COM+ qui sont installées dans la partition globale sont automatiquement disponibles pour tous les utilisateurs sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b2018-106">COM+ applications that are installed in the global partition are automatically available to all users on the server.</span></span> <span data-ttu-id="b2018-107">Si vous avez d’autres applications COM+ que vous souhaitez mettre à la disposition de tous les utilisateurs sur le serveur, vous pouvez les ajouter à la partition globale.</span><span class="sxs-lookup"><span data-stu-id="b2018-107">If you have other COM+ applications that you would like to make available to all users on the server, you can add them into the global partition.</span></span>

<span data-ttu-id="b2018-108">En plus de la partition globale, vous pouvez créer d’autres partitions pour les utilisateurs sur ce serveur uniquement ou pour les utilisateurs dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="b2018-108">In addition to the global partition, you can create other partitions for users on that server only, or for users throughout the domain.</span></span> <span data-ttu-id="b2018-109">La création de partitions supplémentaires et l’installation simultanée de plusieurs configurations d’une application COM+ permettent à vos utilisateurs d’exécuter ces configurations d’application simultanément sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b2018-109">Creating additional partitions and installing multiple configurations of a COM+ application into them allows your users to execute those application configurations simultaneously on the same computer.</span></span> <span data-ttu-id="b2018-110">En outre, en installant des applications COM+ dans une partition autre que la partition globale, vous pouvez contrôler l’accès des utilisateurs à ces applications.</span><span class="sxs-lookup"><span data-stu-id="b2018-110">Also, by installing COM+ applications into a partition other than the global partition, you can control user access to those applications.</span></span>

<span data-ttu-id="b2018-111">**Windows XP :** La possibilité de créer, de configurer ou de déléguer des partitions COM+ n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b2018-111">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="b2018-112">La partition globale est la seule partition COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="b2018-112">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="b2018-113">Pour plus d’informations sur les partitions locales et les partitions définies dans Active Directory, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2018-113">For more information on local partitions and partitions defined within Active Directory, see the following topics:</span></span>

-   [<span data-ttu-id="b2018-114">Partitions locales</span><span class="sxs-lookup"><span data-stu-id="b2018-114">Local Partitions</span></span>](local-partitions.md)
-   [<span data-ttu-id="b2018-115">Partitions et Active Directory</span><span class="sxs-lookup"><span data-stu-id="b2018-115">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
-   [<span data-ttu-id="b2018-116">Partitions par défaut</span><span class="sxs-lookup"><span data-stu-id="b2018-116">Default Partitions</span></span>](default-partitions.md)
-   [<span data-ttu-id="b2018-117">Partition globale</span><span class="sxs-lookup"><span data-stu-id="b2018-117">The Global Partition</span></span>](the-global-partition.md)
-   [<span data-ttu-id="b2018-118">Propriétés de partition</span><span class="sxs-lookup"><span data-stu-id="b2018-118">Partition Properties</span></span>](partition-properties.md)

## <a name="related-topics"></a><span data-ttu-id="b2018-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2018-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2018-120">Restrictions relatives à la conception d’applications</span><span class="sxs-lookup"><span data-stu-id="b2018-120">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="b2018-121">Composants et partitions COM+ en file d’attente</span><span class="sxs-lookup"><span data-stu-id="b2018-121">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="b2018-122">Inscription et activation de composants dans des partitions</span><span class="sxs-lookup"><span data-stu-id="b2018-122">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="b2018-123">Que sont les partitions COM+ ?</span><span class="sxs-lookup"><span data-stu-id="b2018-123">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



