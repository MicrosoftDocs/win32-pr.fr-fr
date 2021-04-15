---
title: Vue d’ensemble du didacticiel ADSI avec Visual Basic
description: Active Directory est une base de données à usage spécial \ 8212 ; il ne s’agit pas d’un remplacement du Registre.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104570596"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a><span data-ttu-id="62960-103">Vue d’ensemble du didacticiel : ADSI avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="62960-103">Tutorial Overview: ADSI with Visual Basic</span></span>

> [!Note]  
> <span data-ttu-id="62960-104">La documentation suivante fait partie d’une description de scénario étendue pour les développeurs Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="62960-104">The following documentation is part of an extended scenario description for Visual Basic developers.</span></span> <span data-ttu-id="62960-105">Si vous recherchez une vue d’ensemble générale de Active Directory, consultez les [documents professionnels de l’informatique sur TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="62960-105">If you are looking for a general overview of Active Directory, see the [IT Pro docs on Technet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span></span> <span data-ttu-id="62960-106">Pour une analyse plus approfondie du côté développement de Active Directory, consultez [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="62960-106">For a more in-depth look at the development side of Active Directory, see [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span></span> <span data-ttu-id="62960-107">Pour plus d’informations sur les interfaces de service Active Directory, consultez la rubrique parente de cette rubrique : [Active Directory des interfaces de service](active-directory-service-interfaces-adsi.md), ainsi que la rubrique sœur : [à propos des interfaces de service Active Directory](about-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="62960-107">For a larger introduction to Active Directory Service Interfaces, see this topic's parent topic: [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md), as well as the sibling topic: [About Active Directory Service Interfaces](about-adsi.md).</span></span>

 

<span data-ttu-id="62960-108">Active Directory est une base de données à usage spécifique ; il ne s’agit pas d’un remplacement du Registre.</span><span class="sxs-lookup"><span data-stu-id="62960-108">Active Directory is a special-purpose database — it is not a registry replacement.</span></span> <span data-ttu-id="62960-109">Le répertoire est conçu pour gérer un grand nombre d’opérations de lecture et de recherche et un nombre nettement plus réduit de modifications et de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="62960-109">The directory is designed to handle a large number of read and search operations and a significantly smaller number of changes and updates.</span></span> <span data-ttu-id="62960-110">Active Directory données sont hiérarchiques, répliquées et extensibles.</span><span class="sxs-lookup"><span data-stu-id="62960-110">Active Directory data is hierarchical, replicated, and extensible.</span></span> <span data-ttu-id="62960-111">Étant donné qu’il est répliqué, vous ne souhaitez pas stocker de données dynamiques, telles que les prix des actions d’entreprise ou les performances de l’UC.</span><span class="sxs-lookup"><span data-stu-id="62960-111">Because it is replicated, you do not want to store dynamic data, such as corporate stock prices or CPU performance.</span></span> <span data-ttu-id="62960-112">Si vos données sont spécifiques à l’ordinateur, stockez les données dans le registre.</span><span class="sxs-lookup"><span data-stu-id="62960-112">If your data is machine-specific, store the data in the registry.</span></span> <span data-ttu-id="62960-113">Les données de file d’attente d’impression, les données de contact utilisateur et les données de configuration réseau/ordinateur sont des exemples typiques de données stockées dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="62960-113">Typical examples of data stored in the directory include printer queue data, user contact data, and network/computer configuration data.</span></span> <span data-ttu-id="62960-114">La base de données Active Directory se compose d’objets et d’attributs.</span><span class="sxs-lookup"><span data-stu-id="62960-114">The Active Directory database consists of objects and attributes.</span></span> <span data-ttu-id="62960-115">Les objets et les définitions d’attributs sont stockés dans le schéma Active Directory.</span><span class="sxs-lookup"><span data-stu-id="62960-115">Objects and attribute definitions are stored in the Active Directory schema.</span></span>

<span data-ttu-id="62960-116">Vous vous demandez peut-être quels objets sont actuellement stockés dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="62960-116">You may be wondering what objects are currently stored in Active Directory.</span></span> <span data-ttu-id="62960-117">Active Directory a trois partitions.</span><span class="sxs-lookup"><span data-stu-id="62960-117">Active Directory has three partitions.</span></span> <span data-ttu-id="62960-118">Ils sont également connus sous le nom de contextes de nommage : domaine, schéma et configuration.</span><span class="sxs-lookup"><span data-stu-id="62960-118">These are also known as naming contexts: domain, schema, and configuration.</span></span> <span data-ttu-id="62960-119">La partition de domaine contient les utilisateurs, les groupes, les contacts, les ordinateurs, les unités d’organisation et de nombreux autres types d’objets.</span><span class="sxs-lookup"><span data-stu-id="62960-119">The domain partition contains users, groups, contacts, computers, organizational units, and many other object types.</span></span> <span data-ttu-id="62960-120">Étant donné que Active Directory est extensible, vous pouvez également ajouter vos propres classes et/ou attributs.</span><span class="sxs-lookup"><span data-stu-id="62960-120">Because Active Directory is extensible, you can also add your own classes and/or attributes.</span></span> <span data-ttu-id="62960-121">La partition de schéma contient des classes et des définitions d’attributs.</span><span class="sxs-lookup"><span data-stu-id="62960-121">The schema partition contains classes and attribute definitions.</span></span> <span data-ttu-id="62960-122">La partition de configuration comprend des données de configuration pour les services, les partitions et les sites.</span><span class="sxs-lookup"><span data-stu-id="62960-122">The configuration partition includes configuration data for services, partitions, and sites.</span></span>

<span data-ttu-id="62960-123">La capture d’écran suivante montre la partition de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="62960-123">The following screen shot shows the Active Directory domain partition.</span></span>

![partition de domaine Active Directory](images/adadsi1.png)

## <a name="related-topics"></a><span data-ttu-id="62960-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62960-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62960-126">Accès Active Directory à l’aide de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="62960-126">Accessing Active Directory Using Visual Basic</span></span>](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[<span data-ttu-id="62960-127">Scénario : Fabrikam Corporation</span><span class="sxs-lookup"><span data-stu-id="62960-127">Scenario: The Fabrikam Corporation</span></span>](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[<span data-ttu-id="62960-128">Rubriques avancées</span><span class="sxs-lookup"><span data-stu-id="62960-128">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 