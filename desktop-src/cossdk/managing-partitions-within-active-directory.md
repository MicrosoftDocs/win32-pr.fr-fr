---
description: En guise d’alternative à la gestion des partitions de Active Directory par le biais de l’outil d’administration utilisateurs et ordinateurs Active Directory, vous pouvez gérer les partitions COM+ par programme à l’aide d’un ensemble d’objets COM+ au sein de l’interface système d’Active Directory (ADSI).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Gestion des partitions dans Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524175"
---
# <a name="managing-partitions-within-active-directory"></a><span data-ttu-id="4bb7b-103">Gestion des partitions dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="4bb7b-103">Managing Partitions Within Active Directory</span></span>

<span data-ttu-id="4bb7b-104">En guise d’alternative à la gestion des partitions de Active Directory par le biais de l’outil d’administration utilisateurs et ordinateurs Active Directory, vous pouvez gérer les partitions COM+ par programme à l’aide d’un ensemble d’objets COM+ au sein de l’interface système d’Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="4bb7b-104">As an alternative to managing Active Directory partitions through the Active Directory Users and Computers administrative tool, you can manage COM+ partitions programmatically through the use of a set of COM+ objects within Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="4bb7b-105">Quelle que soit la technique d’administration choisie pour la gestion des partitions COM+, les administrateurs doivent suivre une séquence générale d’étapes :</span><span class="sxs-lookup"><span data-stu-id="4bb7b-105">Regardless of the administrative technique you choose for managing COM+ partitions, there is a general sequence of steps that administrators must follow:</span></span>

1.  <span data-ttu-id="4bb7b-106">Créez les nouvelles partitions COM+ dans Active Directory pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="4bb7b-106">Create the new COM+ partitions within Active Directory for your domain.</span></span>
2.  <span data-ttu-id="4bb7b-107">Créez des groupes de partitions COM+ dans Active Directory et mappez-les à vos partitions COM+ nouvellement créées.</span><span class="sxs-lookup"><span data-stu-id="4bb7b-107">Create COM+ partition sets within Active Directory, and map them to your newly created COM+ partitions.</span></span>
3.  <span data-ttu-id="4bb7b-108">Configurez vos partitions Active Directory sur votre ordinateur local, à l’aide de l’objet COM+ approprié.</span><span class="sxs-lookup"><span data-stu-id="4bb7b-108">Configure your Active Directory partitions on your local machine, using the appropriate COM+ object.</span></span> <span data-ttu-id="4bb7b-109">Quand vous configurez une partition Active Directory sur un ordinateur local, un dossier **applications com+** est automatiquement créé dans ce dossier de partition.</span><span class="sxs-lookup"><span data-stu-id="4bb7b-109">When you configure an Active Directory partition on a local machine, a **COM+ Applications** folder is automatically created in that partition folder.</span></span>
4.  <span data-ttu-id="4bb7b-110">Installez vos applications COM+ dans les partitions COM+ appropriées.</span><span class="sxs-lookup"><span data-stu-id="4bb7b-110">Install your COM+ applications in the appropriate COM+ partitions.</span></span>

<span data-ttu-id="4bb7b-111">Toutes les étapes précédentes peuvent être effectuées par programme, à l’aide d’un ensemble d’interfaces Active Directory appelées ADSI.</span><span class="sxs-lookup"><span data-stu-id="4bb7b-111">All of the preceding steps can be done programmatically, using a set of Active Directory interfaces called ADSI.</span></span> <span data-ttu-id="4bb7b-112">Les objets disponibles pour la gestion des partitions disponibles dans ADSI sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4bb7b-112">The objects available for managing partitions that are available within ADSI are as follows:</span></span>

-   <span data-ttu-id="4bb7b-113">nom de l' \_ USERPARTITIONSETLINK DS \_</span><span class="sxs-lookup"><span data-stu-id="4bb7b-113">DS\_USERPARTITIONSETLINK\_NAME</span></span>
-   <span data-ttu-id="4bb7b-114">nom de l' \_ PARTITIONLINK DS \_</span><span class="sxs-lookup"><span data-stu-id="4bb7b-114">DS\_PARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="4bb7b-115">nom de l' \_ ObjectID DS \_</span><span class="sxs-lookup"><span data-stu-id="4bb7b-115">DS\_OBJECTID\_NAME</span></span>
-   <span data-ttu-id="4bb7b-116">nom de l' \_ DEFAULTPARTITIONLINK DS \_</span><span class="sxs-lookup"><span data-stu-id="4bb7b-116">DS\_DEFAULTPARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="4bb7b-117">nom de l' \_ USERLINK DS \_</span><span class="sxs-lookup"><span data-stu-id="4bb7b-117">DS\_USERLINK\_NAME</span></span>
-   <span data-ttu-id="4bb7b-118">nom de l' \_ PARTITIONSET DS \_</span><span class="sxs-lookup"><span data-stu-id="4bb7b-118">DS\_PARTITIONSET\_NAME</span></span>
-   <span data-ttu-id="4bb7b-119">nom de la \_ partition DS \_</span><span class="sxs-lookup"><span data-stu-id="4bb7b-119">DS\_PARTITION\_NAME</span></span>

<span data-ttu-id="4bb7b-120">Pour plus d’informations sur la création et la gestion des partitions COM+ à l’aide des outils d’administration Active Directory utilisateurs et ordinateurs et services de composants, consultez l’aide en ligne disponible dans chaque outil.</span><span class="sxs-lookup"><span data-stu-id="4bb7b-120">For information on creating and managing COM+ partitions through the use of the Active Directory Users and Computers and Component Services administrative tools, see the online help available from within each tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bb7b-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4bb7b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bb7b-122">Collecte des métriques de partition</span><span class="sxs-lookup"><span data-stu-id="4bb7b-122">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="4bb7b-123">Configuration du cache de partition</span><span class="sxs-lookup"><span data-stu-id="4bb7b-123">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="4bb7b-124">Regroupement d’applications en partitions</span><span class="sxs-lookup"><span data-stu-id="4bb7b-124">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="4bb7b-125">Gestion des partitions locales</span><span class="sxs-lookup"><span data-stu-id="4bb7b-125">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="4bb7b-126">Définition des droits d’administration pour une partition</span><span class="sxs-lookup"><span data-stu-id="4bb7b-126">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



