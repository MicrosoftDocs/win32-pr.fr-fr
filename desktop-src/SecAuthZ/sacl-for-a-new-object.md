---
description: SACL pour un nouvel objet
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL pour un nouvel objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544703"
---
# <a name="sacl-for-a-new-object"></a><span data-ttu-id="635fd-103">SACL pour un nouvel objet</span><span class="sxs-lookup"><span data-stu-id="635fd-103">SACL for a New Object</span></span>

<span data-ttu-id="635fd-104">Le système utilise l’algorithme suivant pour créer une liste SACL pour la plupart des types de nouveaux objets sécurisables :</span><span class="sxs-lookup"><span data-stu-id="635fd-104">The system uses the following algorithm to build a SACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="635fd-105">La liste SACL de l’objet est la liste SACL du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) spécifié par le créateur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="635fd-105">The object's SACL is the SACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="635fd-106">Le système fusionne les ACE pouvant être héritées dans la liste SACL spécifiée, sauf si le \_ \_ bit protégé par la se est défini dans les bits de contrôle du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="635fd-106">The system merges any inheritable ACEs into the specified SACL unless the SE\_SACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span> <span data-ttu-id="635fd-107">\_ \_ \_ Les ACE d’attribut de ressource système et \_ \_ \_ \_ les ACE d’ID de stratégie système d’un objet parent sont fusionnées dans un nouvel objet, même si le bit protégé par le système d’application système \_ \_ est défini.</span><span class="sxs-lookup"><span data-stu-id="635fd-107">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs and SYSTEM\_SCOPED\_POLICY\_ID\_ACEs from a parent object will be merged to a new object even if the SE\_SACL\_PROTECTED bit is set.</span></span>
2.  <span data-ttu-id="635fd-108">Si le créateur ne spécifie pas de descripteur de sécurité, le système génère la liste SACL de l’objet à partir d’ACE pouvant être héritées.</span><span class="sxs-lookup"><span data-stu-id="635fd-108">If the creator does not specify a security descriptor, the system builds the object's SACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="635fd-109">S’il n’existe aucune SACL spécifiée ou héritée, l’objet n’a pas de SACL.</span><span class="sxs-lookup"><span data-stu-id="635fd-109">If there is no specified or inherited SACL, the object has no SACL.</span></span>

<span data-ttu-id="635fd-110">Pour spécifier une liste SACL pour un nouvel objet, le créateur de l’objet doit avoir \_ le \_ [privilège](privileges.md) nom de sécurité se activé.</span><span class="sxs-lookup"><span data-stu-id="635fd-110">To specify a SACL for a new object, the object's creator must have the SE\_SECURITY\_NAME [privilege](privileges.md) enabled.</span></span> <span data-ttu-id="635fd-111">Si la liste SACL spécifiée pour un nouvel objet contient uniquement des \_ ACE d’attribut de ressource système \_ \_ , le \_ privilège de nom de sécurité se \_ n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="635fd-111">If the specified SACL for a new object contain only SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs, then the SE\_SECURITY\_NAME privilege is not required.</span></span> <span data-ttu-id="635fd-112">Le créateur n’a pas besoin de ce privilège si la liste SACL de l’objet est générée à partir d’entrées de du même auteur.</span><span class="sxs-lookup"><span data-stu-id="635fd-112">The creator does not need this privilege if the object's SACL is built from inherited ACEs.</span></span>

<span data-ttu-id="635fd-113">Le système utilise un algorithme différent pour générer une liste SACL pour un nouvel objet Active Directory.</span><span class="sxs-lookup"><span data-stu-id="635fd-113">The system uses a different algorithm to build a SACL for a new Active Directory object.</span></span> <span data-ttu-id="635fd-114">Pour plus d’informations, voir [Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="635fd-114">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
