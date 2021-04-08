---
title: Restrictions sur l’extension de schéma
description: Afin de réduire le risque de modifications du schéma d’une application qui a pour but de réduire les autres applications et de préserver la cohérence du schéma, Active Directory Domain Services appliquer des restrictions sur le type de modifications de schéma qu’une application ou un utilisateur est autorisé à effectuer.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671245"
---
# <a name="restrictions-on-schema-extension"></a><span data-ttu-id="03b2f-103">Restrictions sur l’extension de schéma</span><span class="sxs-lookup"><span data-stu-id="03b2f-103">Restrictions on Schema Extension</span></span>

<span data-ttu-id="03b2f-104">Afin de réduire le risque de modifications du schéma d’une application qui a pour but de réduire les autres applications et de préserver la cohérence du schéma, Active Directory Domain Services appliquer des restrictions sur le type de modifications de schéma qu’une application ou un utilisateur est autorisé à effectuer.</span><span class="sxs-lookup"><span data-stu-id="03b2f-104">In order to reduce the possibility of schema changes by one application breaking other applications and to maintain schema consistency, Active Directory Domain Services enforce restrictions on the type of schema changes that an application or user is allowed to make.</span></span>

<span data-ttu-id="03b2f-105">Les restrictions sont imposées uniquement lors de la modification d’objets de schéma existants.</span><span class="sxs-lookup"><span data-stu-id="03b2f-105">The restrictions are imposed only on modification of existing schema objects.</span></span> <span data-ttu-id="03b2f-106">Le schéma est classé en deux catégories.</span><span class="sxs-lookup"><span data-stu-id="03b2f-106">The schema is categorized into two categories.</span></span> <span data-ttu-id="03b2f-107">Les objets de schéma fournis avec Windows 2000 dans le schéma de base appartiennent à la catégorie 1.</span><span class="sxs-lookup"><span data-stu-id="03b2f-107">The schema objects that ship with Windows 2000 in the base schema belong to Category 1.</span></span> <span data-ttu-id="03b2f-108">Tous les objets de schéma ajoutés ultérieurement par d’autres applications ou utilisateurs via l’extension de schéma dynamique appartiennent à la catégorie 2.</span><span class="sxs-lookup"><span data-stu-id="03b2f-108">Any schema objects added later by other applications or users through dynamic schema extension belong to Category 2.</span></span> <span data-ttu-id="03b2f-109">La catégorie d’un objet de schéma peut être déterminée par le bit 0x10 défini dans l’attribut **systemFlags** de l’objet **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="03b2f-109">The category of a schema object can be determined by the 0x10 bit set in the **systemFlags** attribute on the **classSchema** object.</span></span> <span data-ttu-id="03b2f-110">Ce bit n’est défini que sur les objets de catégorie 1 et ne peut pas être modifié, ni défini sur un objet de catégorie 2.</span><span class="sxs-lookup"><span data-stu-id="03b2f-110">This bit is only set on Category 1 objects, and cannot be altered, nor can it be set on any Category 2 object.</span></span>

<span data-ttu-id="03b2f-111">L’attribut **systemFlags** est utilisé en interne par Active Directory Domain Services pour identifier les caractéristiques spéciales des objets « infrastructure » dans le schéma de base.</span><span class="sxs-lookup"><span data-stu-id="03b2f-111">The **systemFlags** attribute is used internally by Active Directory Domain Services to identify special characteristics of "infrastructure" objects in the base schema.</span></span> <span data-ttu-id="03b2f-112">Outre l’identification des objets catégorie 1, **systemFlags** détermine si un objet peut être déplacé, supprimé ou renommé.</span><span class="sxs-lookup"><span data-stu-id="03b2f-112">In addition to identifying Category 1 objects, **systemFlags** controls whether an object can be moved, deleted, or renamed.</span></span> <span data-ttu-id="03b2f-113">Ces opérations sont évitées pour les objets dont dépend Windows 2000 pour s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="03b2f-113">These operations are prevented for objects that Windows 2000 depends on to run.</span></span>

<span data-ttu-id="03b2f-114">Sur tous les objets de schéma, catégorie 1 ou 2, Active Directory Domain Services imposer les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="03b2f-114">On any schema objects, Category 1 or 2, Active Directory Domain Services impose the following restrictions:</span></span>

-   <span data-ttu-id="03b2f-115">Vous ne pouvez pas ajouter un nouveau **mustContain** à une classe (directement ou par héritage en ajoutant une classe auxiliaire).</span><span class="sxs-lookup"><span data-stu-id="03b2f-115">You cannot add a new **mustContain** to a class (directly or through inheritance by adding an auxiliary class).</span></span>
-   <span data-ttu-id="03b2f-116">Vous ne pouvez pas supprimer de **mustContain** de la classe (directement ou par héritage).</span><span class="sxs-lookup"><span data-stu-id="03b2f-116">You cannot delete any **mustContain** of the class (directly or through inheritance).</span></span>

<span data-ttu-id="03b2f-117">En outre, les restrictions supplémentaires suivantes sont imposées sur les objets de schéma de catégorie 1 :</span><span class="sxs-lookup"><span data-stu-id="03b2f-117">In addition, the following additional restrictions are imposed on Category 1 schema objects:</span></span>

-   <span data-ttu-id="03b2f-118">Vous ne pouvez pas modifier les attributs suivants d’un attribut Category 1 :</span><span class="sxs-lookup"><span data-stu-id="03b2f-118">You cannot change the following attributes of a Category 1 attribute:</span></span>

    -   <span data-ttu-id="03b2f-119">**rangeLower** et **rangeUpper** (plage de valeurs).</span><span class="sxs-lookup"><span data-stu-id="03b2f-119">**rangeLower** and **rangeUpper** (value range).</span></span>
    -   <span data-ttu-id="03b2f-120">**attributeSecurityGuid** (détermine le jeu de propriétés auquel l’attribut appartient, le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="03b2f-120">**attributeSecurityGuid** (determines which property set the attribute belongs in, if any).</span></span>

-   <span data-ttu-id="03b2f-121">Vous ne pouvez pas modifier le **defaultObjectCategory** d’une classe de catégorie 1.</span><span class="sxs-lookup"><span data-stu-id="03b2f-121">You cannot change the **defaultObjectCategory** of a Category 1 class.</span></span>
-   <span data-ttu-id="03b2f-122">Vous ne pouvez pas modifier l' **objectCategory** d’une instance d’une classe de catégorie 1.</span><span class="sxs-lookup"><span data-stu-id="03b2f-122">You cannot change the **objectCategory** of any instance of a Category 1 class.</span></span>
-   <span data-ttu-id="03b2f-123">Vous ne pouvez pas rendre obsolète une classe ou un attribut de catégorie 1.</span><span class="sxs-lookup"><span data-stu-id="03b2f-123">You cannot make a Category 1 class or attribute defunct.</span></span>
-   <span data-ttu-id="03b2f-124">Vous ne pouvez pas modifier le **lDAPDisplayName** d’une classe ou d’un attribut Category 1.</span><span class="sxs-lookup"><span data-stu-id="03b2f-124">You cannot change the **lDAPDisplayName** of a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="03b2f-125">Vous ne pouvez pas renommer une classe ou un attribut Category 1.</span><span class="sxs-lookup"><span data-stu-id="03b2f-125">You cannot rename a Category 1 class or attribute.</span></span>

 

 




