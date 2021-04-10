---
title: Contrôle de l’accès aux objets et à leurs propriétés
description: Pour contrôler l’accès aux objets d’application, utilisez le descripteur de sécurité de l’objet, et plus précisément, avec la liste de contrôle d’accès discrétionnaire (DACL) et sa liste d’entrées de contrôle d’accès (ACE).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- objet AD, contrôle de l’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190709"
---
# <a name="controlling-access-to-objects-and-their-properties"></a><span data-ttu-id="3fc0f-104">Contrôle de l’accès aux objets et à leurs propriétés</span><span class="sxs-lookup"><span data-stu-id="3fc0f-104">Controlling Access to Objects and Their Properties</span></span>

<span data-ttu-id="3fc0f-105">Pour contrôler l’accès aux objets d’application, utilisez le descripteur de sécurité de l’objet, et plus précisément, avec la liste de contrôle d’accès discrétionnaire (DACL) et sa liste d’entrées de contrôle d’accès (ACE).</span><span class="sxs-lookup"><span data-stu-id="3fc0f-105">To control access to application objects, work with the object security descriptor, and specifically, with the discretionary access-control list (DACL) and its list of access-control entries (ACEs).</span></span>

<span data-ttu-id="3fc0f-106">Lorsqu’un objet est créé, il reçoit un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-106">When an object is created, it receives a security descriptor.</span></span> <span data-ttu-id="3fc0f-107">Pour plus d’informations et pour obtenir une description des règles que le système utilise pour créer la liste DACL pour un nouvel objet, voir [Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3fc0f-107">For more information, and a description of the rules that the system uses to create the DACL for a new object, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span> <span data-ttu-id="3fc0f-108">Ces règles révèlent que vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="3fc0f-108">These rules reveal that you can:</span></span>

-   <span data-ttu-id="3fc0f-109">Créez un nouveau descripteur de sécurité et attachez-le à l’objet au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-109">Create a new security descriptor and attach it to the object at creation time.</span></span> <span data-ttu-id="3fc0f-110">Pour plus d’informations, consultez [création d’un descripteur de sécurité pour un nouvel objet d’annuaire](creating-a-security-descriptor-for-a-new-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="3fc0f-110">For more information, see [Creating a Security Descriptor for a New Directory Object](creating-a-security-descriptor-for-a-new-directory-object.md).</span></span>
-   <span data-ttu-id="3fc0f-111">Appliquez une entrée du contrôle d’accès héritable, à tout moment dans la hiérarchie de répertoires, de telle sorte qu’une entrée du contrôle d’accès est héritée par les objets de l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-111">Apply an inheritable ACE, at any point in the directory hierarchy, such that an ACE is inherited by objects down the tree.</span></span> <span data-ttu-id="3fc0f-112">Un objet peut hériter d’une entrée du contrôle d’accès de son conteneur parent.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-112">An object can inherit an ACE from its parent container.</span></span> <span data-ttu-id="3fc0f-113">Pour plus d’informations, consultez [héritage et délégation de l’administration](inheritance-and-delegation-of-administration.md).</span><span class="sxs-lookup"><span data-stu-id="3fc0f-113">For more information, see [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md).</span></span>
-   <span data-ttu-id="3fc0f-114">Spécifiez une entrée du contrôle d’accès dans la liste DACL par défaut dans le schéma, si vous disposez des droits d’accès nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-114">Specify an ACE in the default DACL in the schema, if you have the necessary access rights.</span></span> <span data-ttu-id="3fc0f-115">Chaque définition de classe d’objet dans le schéma comprend un descripteur de sécurité par défaut qui peut avoir une liste DACL par défaut.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-115">Every object class definition in the schema includes a default security descriptor that can have a default DACL.</span></span> <span data-ttu-id="3fc0f-116">Pour plus d’informations, consultez [descripteur de sécurité par défaut](default-security-descriptor.md).</span><span class="sxs-lookup"><span data-stu-id="3fc0f-116">For more information, see [Default Security Descriptor](default-security-descriptor.md).</span></span>

<span data-ttu-id="3fc0f-117">En outre, la liste DACL d’un objet existant peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-117">In addition the DACL of an existing object can be modified.</span></span> <span data-ttu-id="3fc0f-118">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="3fc0f-118">You can:</span></span>

-   <span data-ttu-id="3fc0f-119">Remplacez la liste DACL par une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-119">Replace the DACL with a new one.</span></span>
-   <span data-ttu-id="3fc0f-120">Lisez la liste DACL existante, modifiez-la et appliquez la liste DACL modifiée.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-120">Read the existing DACL, modify it, and apply the modified DACL.</span></span> <span data-ttu-id="3fc0f-121">Pour plus d’informations, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="3fc0f-121">For more information, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="3fc0f-122">La liste suivante décrit la fonction la plus importante d’une entrée du contrôle d’accès dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-122">The following list describes the most important function of an ACE in Active Directory Domain Services.</span></span> <span data-ttu-id="3fc0f-123">Avec une entrée de contrôle d’accès, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="3fc0f-123">With an ACE, you can:</span></span>

-   <span data-ttu-id="3fc0f-124">Contrôler qui peut effectuer des opérations spécifiques sur un objet.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-124">Control who can perform specific operations on an object.</span></span>
-   <span data-ttu-id="3fc0f-125">Contrôler qui a accès à une propriété spécifique, ou à un ensemble de propriétés, d’un objet.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-125">Control who has access to a specific property, or set of properties, of an object.</span></span>
-   <span data-ttu-id="3fc0f-126">Contrôler qui peut créer des objets enfants dans un conteneur, y compris qui peut créer un type spécifique d’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-126">Control who can create child objects in a container, including who can create a specific type of child object.</span></span>
-   <span data-ttu-id="3fc0f-127">Définir des droits d’accès au contrôle privé pour un type d’objet et contrôler qui peut effectuer les opérations protégées par les droits privés.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-127">Define private control-access rights for an object type and control who can perform the operations protected by the private rights.</span></span>
-   <span data-ttu-id="3fc0f-128">Appliquez une entrée du contrôle d’accès à un objet conteneur à la racine d’une sous-arborescence de répertoires, de façon à ce que les protections puissent être héritées automatiquement par tous les objets enfants dans l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-128">Apply an ACE to a container object at the root of a directory subtree, such that the protections can be inherited automatically by all child objects down the tree.</span></span>
-   <span data-ttu-id="3fc0f-129">Applique une entrée du contrôle d’accès qui est héritée automatiquement par un type spécifique d’objet enfant dans une sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-129">Apply an ACE that is inherited automatically by a specific type of child object in a subtree.</span></span>
-   <span data-ttu-id="3fc0f-130">Créer une entrée du contrôle d’accès qui accorde des droits à un groupe de sécurité plutôt qu’à un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-130">Create an ACE that grants rights to a security group, rather than to a single user.</span></span>
-   <span data-ttu-id="3fc0f-131">Appliquez une entrée du contrôle d’accès pour stratégie de groupe objets afin de contrôler les comptes et les ordinateurs affectés par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="3fc0f-131">Apply an ACE to Group Policy Objects to control the accounts and computers affected by the policy.</span></span>

 

 




