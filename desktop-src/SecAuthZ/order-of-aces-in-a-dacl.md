---
description: Lorsqu’un processus tente d’accéder à un objet sécurisable, le système passe par les entrées de contrôle d’accès (ACE) de la liste de contrôle d’accès discrétionnaire (DACL) des objets jusqu’à ce qu’il trouve des ACE qui autorisent ou refusent l’accès demandé.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Ordre des entrées de commande dans une liste DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520618"
---
# <a name="order-of-aces-in-a-dacl"></a><span data-ttu-id="c1947-103">Ordre des entrées de commande dans une liste DACL</span><span class="sxs-lookup"><span data-stu-id="c1947-103">Order of ACEs in a DACL</span></span>

<span data-ttu-id="c1947-104">Lorsqu’un [*processus*](/windows/desktop/SecGloss/p-gly) tente d’accéder à un objet sécurisable, le système passe par des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) dans la liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) de l’objet jusqu’à ce qu’il trouve des ACE qui autorisent ou refusent l’accès demandé.</span><span class="sxs-lookup"><span data-stu-id="c1947-104">When a [*process*](/windows/desktop/SecGloss/p-gly) tries to access a securable object, the system steps through the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) until it finds ACEs that allow or deny the requested access.</span></span> <span data-ttu-id="c1947-105">Les droits d’accès qu’un DACL permet à un utilisateur peuvent varier en fonction de l’ordre des entrées de commande dans la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="c1947-105">The access rights that a DACL allows a user could vary depending on the order of ACEs in the DACL.</span></span> <span data-ttu-id="c1947-106">Par conséquent, le système d’exploitation Windows XP définit un ordre préféré pour les ACE dans la liste DACL d’un objet sécurisable.</span><span class="sxs-lookup"><span data-stu-id="c1947-106">Consequently, the Windows XP operating system defines a preferred order for ACEs in the DACL of a securable object.</span></span> <span data-ttu-id="c1947-107">L’ordre par défaut fournit un Framework simple qui garantit qu’une entrée de contrôle d’accès refusée refuse réellement l’accès.</span><span class="sxs-lookup"><span data-stu-id="c1947-107">The preferred order provides a simple framework that ensures that an access-denied ACE actually denies access.</span></span> <span data-ttu-id="c1947-108">Pour plus d’informations sur l’algorithme du système de vérification de l’accès, consultez [Comment les DACL contrôlent l’accès à un objet](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="c1947-108">For more information about the system's algorithm for checking access, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="c1947-109">Pour Windows Server 2003 et Windows XP, l’ordre approprié des ACE est compliqué par l’introduction des ACE spécifiques aux objets et de l’héritage automatique.</span><span class="sxs-lookup"><span data-stu-id="c1947-109">For Windows Server 2003 and Windows XP, the proper order of ACEs is complicated by the introduction of object-specific ACEs and automatic inheritance.</span></span>

<span data-ttu-id="c1947-110">Les étapes suivantes décrivent l’ordre par défaut :</span><span class="sxs-lookup"><span data-stu-id="c1947-110">The following steps describe the preferred order:</span></span>

1.  <span data-ttu-id="c1947-111">Toutes les entrées ACE explicites sont placées dans un groupe avant les ACE héritées.</span><span class="sxs-lookup"><span data-stu-id="c1947-111">All explicit ACEs are placed in a group before any inherited ACEs.</span></span>
2.  <span data-ttu-id="c1947-112">Dans le groupe d’ACE explicites, les ACE Access-denied sont placées avant les ACE access-allowed.</span><span class="sxs-lookup"><span data-stu-id="c1947-112">Within the group of explicit ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>
3.  <span data-ttu-id="c1947-113">Les ACE héritées sont placées dans l’ordre dans lequel elles sont héritées.</span><span class="sxs-lookup"><span data-stu-id="c1947-113">Inherited ACEs are placed in the order in which they are inherited.</span></span> <span data-ttu-id="c1947-114">Les ACE héritées du parent de l’objet enfant viennent en premier, puis les ACE héritées du grand-parent, et ainsi de suite sur l’arborescence des objets.</span><span class="sxs-lookup"><span data-stu-id="c1947-114">ACEs inherited from the child object's parent come first, then ACEs inherited from the grandparent, and so on up the tree of objects.</span></span>
4.  <span data-ttu-id="c1947-115">Pour chaque niveau d’ACE héritées, les ACE Access-denied sont placées avant les ACE access-allowed.</span><span class="sxs-lookup"><span data-stu-id="c1947-115">For each level of inherited ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>

<span data-ttu-id="c1947-116">Bien entendu, tous les types ACE ne sont pas requis dans une liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="c1947-116">Of course, not all ACE types are required in an ACL.</span></span>

<span data-ttu-id="c1947-117">Les fonctions telles que [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) et [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) ajoutent une entrée de contrôle d’accès à la fin d’une liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="c1947-117">Functions such as [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) and [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) add an ACE to the end of an ACL.</span></span> <span data-ttu-id="c1947-118">Il incombe à l’appelant de s’assurer que les ACE sont ajoutées dans l’ordre approprié.</span><span class="sxs-lookup"><span data-stu-id="c1947-118">It is the caller's responsibility to ensure that the ACEs are added in the proper order.</span></span>

 

 
