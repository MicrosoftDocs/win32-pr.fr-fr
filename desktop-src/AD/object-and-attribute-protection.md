---
title: Protection des objets et des attributs
description: Une liste de contrôle d’accès (ACL) protège tous les objets de Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Protection des objets et des attributs
- sécurité AD, objet et attribut protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671262"
---
# <a name="object-and-attribute-protection"></a><span data-ttu-id="5ae76-105">Protection des objets et des attributs</span><span class="sxs-lookup"><span data-stu-id="5ae76-105">Object and Attribute Protection</span></span>

<span data-ttu-id="5ae76-106">Une liste de contrôle d’accès (ACL) protège tous les objets de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="5ae76-106">An access-control list (ACL) protects all objects in Active Directory Domain Services.</span></span> <span data-ttu-id="5ae76-107">Les listes de contrôle d’accès déterminent qui peut afficher l’objet, les attributs qu’ils peuvent lire et les actions que chaque utilisateur peut effectuer sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="5ae76-107">ACLs determine who can view the object, what attributes they can read, and what actions each user can perform on the object.</span></span> <span data-ttu-id="5ae76-108">L’existence d’un objet ou d’un attribut n’est jamais révélée à un utilisateur non autorisé.</span><span class="sxs-lookup"><span data-stu-id="5ae76-108">The existence of an object or an attribute is never revealed to an unauthorized user.</span></span>

<span data-ttu-id="5ae76-109">Une liste ACL est une liste d’entrées de contrôle d’accès (ACE) stockées avec l’objet qu’elle protège.</span><span class="sxs-lookup"><span data-stu-id="5ae76-109">An ACL is a list of access-control entries (ACEs) stored with the object that it protects.</span></span> <span data-ttu-id="5ae76-110">Dans Windows NT et Windows 2000, une liste de contrôle d’accès est stockée sous forme de valeur binaire, appelée descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5ae76-110">In Windows NT and Windows 2000, an ACL is stored as a binary value, called a security descriptor.</span></span> <span data-ttu-id="5ae76-111">Chaque ACE contient un identificateur de sécurité (SID), qui identifie le principal (utilisateur ou groupe) auquel l’entrée du contrôle d’accès s’applique, ainsi que les données sur le type d’accès accordé ou refusé par l’ACE.</span><span class="sxs-lookup"><span data-stu-id="5ae76-111">Each ACE contains a security identifier (SID), which identifies the principal (user or group) to whom the ACE applies, and data about what type of access the ACE grants or denies.</span></span>

<span data-ttu-id="5ae76-112">Les listes de contrôle d’accès pour les objets d’annuaire contiennent des entrées de contrôle d’accès qui s’appliquent à l’objet dans son ensemble et aux ACE qui s’appliquent aux attributs individuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5ae76-112">ACLs for directory objects contain ACEs that apply to the object as a whole and ACEs that apply to the individual attributes of the object.</span></span> <span data-ttu-id="5ae76-113">Cela permet à un administrateur de contrôler non seulement quels utilisateurs peuvent voir un objet, mais également quelles propriétés ils peuvent afficher.</span><span class="sxs-lookup"><span data-stu-id="5ae76-113">This allows an administrator to control not only which users can see an object, but also what properties those users can view.</span></span> <span data-ttu-id="5ae76-114">Par exemple, tous les utilisateurs peuvent se voir accorder l’accès en lecture aux attributs de messagerie et de numéro de téléphone de tous les autres utilisateurs, mais les propriétés de sécurité des utilisateurs peuvent être refusées à tous les membres du groupe administrateurs de sécurité spéciaux.</span><span class="sxs-lookup"><span data-stu-id="5ae76-114">For example, all users might be granted read access to the email and telephone number attributes for all other users, but security properties of users might be denied to all but members of a special security administrators group.</span></span> <span data-ttu-id="5ae76-115">Les utilisateurs individuels peuvent bénéficier d’un accès en écriture à des attributs personnels, tels que les adresses de téléphone et de publipostage sur leurs propres objets utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ae76-115">Individual users might be granted write access to personal attributes such as the telephone and mailing addresses on their own user objects.</span></span>

 

 




