---
title: Schéma de Active Directory (schéma Active Directory)
description: Le schéma de Active Directory Microsoft contient des définitions formelles de chaque classe d’objet pouvant être créée dans une forêt Active Directory.
ms.assetid: b3da4519-d0c6-47eb-9455-ada653ad5c9e
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3393a6da1b8d1bd2c2418084c8f7fc657732
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512091"
---
# <a name="active-directory-schema-ad-schema"></a><span data-ttu-id="6f2d1-104">Schéma de Active Directory (schéma Active Directory)</span><span class="sxs-lookup"><span data-stu-id="6f2d1-104">Active Directory Schema (AD Schema)</span></span>

<span data-ttu-id="6f2d1-105">Le schéma de Active Directory Microsoft contient des définitions formelles de chaque classe d’objet pouvant être créée dans une forêt Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-105">The Microsoft Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="6f2d1-106">Le schéma contient également des définitions formelles de chaque attribut qui peut exister dans un objet Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-106">The schema also contains formal definitions of every attribute that can exist in an Active Directory object.</span></span> <span data-ttu-id="6f2d1-107">Cette section fournit la référence pour chaque objet de schéma et fournit une brève explication des attributs, des classes et d’autres objets qui composent le schéma Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-107">This section provides the reference for each schema object and provides a brief explanation of the attributes, classes, and other objects that make up the Active Directory schema.</span></span>

> [!Note]  
> <span data-ttu-id="6f2d1-108">La documentation suivante contient la référence de programmation pour Active Directory schéma.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-108">The following documentation contains the programming reference for Active Directory schema.</span></span> <span data-ttu-id="6f2d1-109">Si vous êtes un utilisateur final qui tente de déboguer une erreur d’imprimante, effectuez une recherche sur le site de la [communauté Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6f2d1-109">If you are an end-user attempting to debug a printer error, try searching on the [Microsoft community site](https://answers.microsoft.com).</span></span> <span data-ttu-id="6f2d1-110">Si vous êtes un développeur à la recherche d’une vue d’ensemble générale de Active Directory schéma, consultez les rubriques de présentation du [schéma Active Directory](/windows/desktop/AD/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="6f2d1-110">If you are a developer looking for a general overview of Active Directory schema, see the [Active Directory Schema](/windows/desktop/AD/active-directory-schema) overview topics.</span></span> <span data-ttu-id="6f2d1-111">Si vous recherchez des instructions de programmation pour la mise à jour ou la modification du schéma, pour plus d’informations sur l’extension et la personnalisation du schéma, consultez [extension du](/windows/desktop/AD/extending-the-schema)schéma, ainsi que la plupart des rubriques du [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) et [services AD LDS (Active Directory Lightweight Directory Services)](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) guides de programmation.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-111">If you are looking for programming guidelines for updating or modifying the schema, For more information about extending and customizing the schema, see [Extending the Schema](/windows/desktop/AD/extending-the-schema), as well as many of the topics in the [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) and [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) programming guides.</span></span>

 

<span data-ttu-id="6f2d1-112">Dans chacune des rubriques de référence, il existe une section pour chaque système d’exploitation auquel s’applique la rubrique.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-112">In each of the reference topics, there is a section for each operating system that the topic applies to.</span></span> <span data-ttu-id="6f2d1-113">Les systèmes d’exploitation suivants sont actuellement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-113">The following operating systems are currently supported.</span></span> 

| <span data-ttu-id="6f2d1-114">Plateforme</span><span class="sxs-lookup"><span data-stu-id="6f2d1-114">Platform</span></span>                                                      | <span data-ttu-id="6f2d1-115">Nom dans la rubrique</span><span class="sxs-lookup"><span data-stu-id="6f2d1-115">Name in topic</span></span>                               |
|---------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="6f2d1-116">Microsoft Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f2d1-116">Microsoft Windows Server 2003</span></span><br/>                      | <span data-ttu-id="6f2d1-117">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6f2d1-117">Windows Server 2003</span></span><br/>              |
| <span data-ttu-id="6f2d1-118">Microsoft Active Directory Application Mode (ADAM)</span><span class="sxs-lookup"><span data-stu-id="6f2d1-118">Microsoft Active Directory Application Mode (ADAM)</span></span><br/> | <span data-ttu-id="6f2d1-119">ADAM</span><span class="sxs-lookup"><span data-stu-id="6f2d1-119">ADAM</span></span><br/>                             |
| <span data-ttu-id="6f2d1-120">Microsoft Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f2d1-120">Microsoft Windows Server 2003 R2</span></span><br/>                   | <span data-ttu-id="6f2d1-121">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6f2d1-121">Windows Server 2003 R2</span></span><br/>           |
| <span data-ttu-id="6f2d1-122">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f2d1-122">Microsoft Windows Server 2008</span></span><br/>                      | <span data-ttu-id="6f2d1-123">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f2d1-123">Microsoft Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="6f2d1-124">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f2d1-124">Microsoft Windows Server 2008 R2</span></span><br/>                   | <span data-ttu-id="6f2d1-125">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f2d1-125">Microsoft Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="6f2d1-126">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f2d1-126">Microsoft Windows Server 2012</span></span><br/>                      | <span data-ttu-id="6f2d1-127">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f2d1-127">Microsoft Windows Server 2012</span></span><br/>    |



 

<span data-ttu-id="6f2d1-128">Si un système d’exploitation n’est pas listé dans la rubrique, la rubrique n’est pas prise en charge sur ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-128">If an operating system is not listed in the topic, the topic is not supported on that operating system.</span></span> <span data-ttu-id="6f2d1-129">Par exemple, si une rubrique ne répertorie que Windows Server 2003 et ADAM, la rubrique ne s’applique pas à Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-129">For example, if a topic only lists Windows Server 2003 and ADAM, then the topic does not apply to Windows Server 2003 R2.</span></span>

<span data-ttu-id="6f2d1-130">Les sections suivantes contiennent des informations détaillées sur les éléments de schéma Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6f2d1-130">The following sections contain detailed information about the Active Directory schema elements.</span></span>

-   [<span data-ttu-id="6f2d1-131">Terminologie relative au schéma Active Directory</span><span class="sxs-lookup"><span data-stu-id="6f2d1-131">Active Directory Schema Terminology</span></span>](active-directory-schema-site.md)
-   [<span data-ttu-id="6f2d1-132">Classes</span><span class="sxs-lookup"><span data-stu-id="6f2d1-132">Classes</span></span>](classes.md)
-   [<span data-ttu-id="6f2d1-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="6f2d1-133">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="6f2d1-134">Syntaxes</span><span class="sxs-lookup"><span data-stu-id="6f2d1-134">Syntaxes</span></span>](syntaxes.md)
-   [<span data-ttu-id="6f2d1-135">Contrôler les droits d’accès</span><span class="sxs-lookup"><span data-stu-id="6f2d1-135">Control Access Rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="6f2d1-136">RootDSE</span><span class="sxs-lookup"><span data-stu-id="6f2d1-136">RootDSE</span></span>](rootdse.md)

 

