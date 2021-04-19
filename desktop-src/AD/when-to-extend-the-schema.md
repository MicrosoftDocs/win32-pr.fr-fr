---
title: Quand étendre le schéma
description: Étendez le schéma uniquement si aucune classe d’objet existante ne répond aux besoins de votre application. L’extension du schéma est une opération complexe. les modifications de schéma sont répliquées sur chaque contrôleur de domaine de la forêt d’entreprise. Envisagez cette considération avec prudence.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Quand étendre l’AD du schéma
- schéma Active Directory, quand étendre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511614"
---
# <a name="when-to-extend-the-schema"></a><span data-ttu-id="0cdf2-107">Quand étendre le schéma</span><span class="sxs-lookup"><span data-stu-id="0cdf2-107">When to Extend the Schema</span></span>

<span data-ttu-id="0cdf2-108">Étendez le schéma uniquement si aucune classe d’objet existante ne répond aux besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-108">Extend the schema only if no existing object class fulfills the requirements of your application.</span></span> <span data-ttu-id="0cdf2-109">L’extension du schéma est une opération complexe. les modifications de schéma sont répliquées sur chaque contrôleur de domaine de la forêt d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-109">Extending the schema is a complex operation; schema changes are replicated to every domain controller in the enterprise forest.</span></span> <span data-ttu-id="0cdf2-110">Envisagez cette considération avec prudence.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-110">Consider this carefully.</span></span>

<span data-ttu-id="0cdf2-111">Le schéma peut être étendu de trois façons :</span><span class="sxs-lookup"><span data-stu-id="0cdf2-111">The schema can be extended in three ways:</span></span>

-   <span data-ttu-id="0cdf2-112">Dérivez une nouvelle sous-classe d’une classe existante-la sous-classe possède tous les attributs de la superclasse et les attributs que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-112">Derive a new subclass from an existing class - the subclass has all of the attributes of the superclass and any attributes you specify.</span></span> <span data-ttu-id="0cdf2-113">Dérivation à partir d’une classe existante :</span><span class="sxs-lookup"><span data-stu-id="0cdf2-113">Derive from an existing class:</span></span>
    -   <span data-ttu-id="0cdf2-114">Lorsque la classe existante requiert des attributs supplémentaires, mais dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-114">When the existing class requires additional attributes, but otherwise is acceptable.</span></span>
    -   <span data-ttu-id="0cdf2-115">Lorsque la possibilité de transformer des objets existants de la classe en une nouvelle classe n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-115">When the ability to transform existing objects of the class into a new class is not required.</span></span> <span data-ttu-id="0cdf2-116">Il n’est pas possible d’ajouter une sous-classe à un objet existant.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-116">It is not possible to add a subclass to an existing object.</span></span>
    -   <span data-ttu-id="0cdf2-117">Pour utiliser le composant logiciel enfichable Gestionnaire de répertoire existant pour gérer les attributs étendus des objets.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-117">To use the existing Directory Manager snap-in to manage the extended attributes of the objects.</span></span>
-   <span data-ttu-id="0cdf2-118">Ajoutez des attributs à une classe existante et/ou ajoutez des objets parents pour la classe.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-118">Add attributes to an existing class and/or add parent objects for the class.</span></span> <span data-ttu-id="0cdf2-119">Lors de l’ajout de plusieurs attributs, effectuez cette opération de manière structurée en définissant une classe auxiliaire et en ajoutant cette classe auxiliaire à la classe existante.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-119">When adding multiple attributes, perform this operation in a structured manner by defining an auxiliary class and adding that auxiliary class to the existing class.</span></span>
-   <span data-ttu-id="0cdf2-120">La modification d’une classe existante est requise lorsqu’une application nécessite la possibilité d’étendre des objets existants de la classe.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-120">Modification of an existing class is required when an application requires the ability to extend existing objects of the class.</span></span> <span data-ttu-id="0cdf2-121">Par exemple, pour ajouter des données spécifiques à l’application à l’objet utilisateur, étendez l’utilisateur de la classe normalement, car vous devez gérer les utilisateurs existants et pas seulement les utilisateurs spéciaux créés par votre application.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-121">For example, to add application-specific data to the User object, extend the class User normally, because you must handle existing Users and not just special Users created by your application.</span></span>
-   <span data-ttu-id="0cdf2-122">Créez une nouvelle classe avec les attributs requis.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-122">Create a new class with the required attributes.</span></span> <span data-ttu-id="0cdf2-123">Créez une nouvelle classe. autrement dit, une classe dérivée de « Top » quand aucune classe existante ne répond aux spécifications opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-123">Create a new class; that is, a class derived from "Top" when no existing class fulfills the operational requirements.</span></span>

<span data-ttu-id="0cdf2-124">Quand vous sous-classez une classe existante, les éléments d’interface utilisateur associés à la classe d’origine ne sont pas hérités par la sous-classe.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-124">When you subclass an existing class, any user interface items associated to the original class will not be inherited by the subclass.</span></span> <span data-ttu-id="0cdf2-125">Par exemple, si vous sous-classez un objet utilisateur, les pages de propriétés et les éléments de menu associés à l’utilisateur ne sont pas hérités.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-125">For example, if you subclass a user object, the property pages and menu items associated to user are not inherited.</span></span> <span data-ttu-id="0cdf2-126">Pour cette raison, il est préférable d’étendre un objet existant ou de créer une classe auxiliaire au lieu de créer une sous-classe.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-126">For this reason, it is preferable to extend an existing object or create an auxiliary class rather than create a subclass.</span></span>

<span data-ttu-id="0cdf2-127">Si vous sous-classez une classe existante ou modifiez une classe existante, vous devez étendre les outils tels que le composant logiciel enfichable utilisateurs et ordinateurs Active Directory pour gérer les attributs étendus des objets.</span><span class="sxs-lookup"><span data-stu-id="0cdf2-127">Whether you subclass an existing class or modify an existing class, you will want to extend tools such as the Active Directory Users and Computers snap-in to manage the extended attributes of the objects.</span></span> <span data-ttu-id="0cdf2-128">Pour plus d’informations, consultez [extension de l’interface utilisateur pour les objets d’annuaire](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0cdf2-128">For more information, see [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

 

 




