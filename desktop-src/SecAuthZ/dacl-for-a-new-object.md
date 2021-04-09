---
description: Liste DACL pour un nouvel objet
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: Liste DACL pour un nouvel objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114134"
---
# <a name="dacl-for-a-new-object"></a><span data-ttu-id="0e013-103">Liste DACL pour un nouvel objet</span><span class="sxs-lookup"><span data-stu-id="0e013-103">DACL for a New Object</span></span>

<span data-ttu-id="0e013-104">Le système utilise l’algorithme suivant pour créer une liste DACL pour la plupart des types de nouveaux objets sécurisables :</span><span class="sxs-lookup"><span data-stu-id="0e013-104">The system uses the following algorithm to build a DACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="0e013-105">La liste DACL de l’objet est la liste DACL du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) spécifié par le créateur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e013-105">The object's DACL is the DACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="0e013-106">Le système fusionne toutes les entrées du contrôle d’accès (ACE) pouvant être héritées dans la liste DACL spécifiée, sauf si le \_ \_ bit protégé de se DACL est défini dans les bits de contrôle du descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="0e013-106">The system merges any inheritable ACEs into the specified DACL unless the SE\_DACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span>
2.  <span data-ttu-id="0e013-107">Si le créateur ne spécifie pas de descripteur de sécurité, le système génère la liste DACL de l’objet à partir d’ACE pouvant être héritées.</span><span class="sxs-lookup"><span data-stu-id="0e013-107">If the creator does not specify a security descriptor, the system builds the object's DACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="0e013-108">Si aucun descripteur de sécurité n’est spécifié et qu’il n’y a pas d’ACE pouvant être héritées, la DACL de l’objet est la liste DACL par défaut du jeton [*principal*](/windows/desktop/SecGloss/p-gly) ou d' [*emprunt d’identité*](/windows/desktop/SecGloss/i-gly) du créateur.</span><span class="sxs-lookup"><span data-stu-id="0e013-108">If no security descriptor is specified and there are no inheritable ACEs, the object's DACL is the default DACL from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creator.</span></span>
4.  <span data-ttu-id="0e013-109">S’il n’existe pas d’ACL spécifiée, héritée ou par défaut, le système crée l’objet sans DACL, ce qui permet à tout le monde d’accéder entièrement à l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e013-109">If there is no specified, inherited, or default DACL, the system creates the object with no DACL, which allows everyone full access to the object.</span></span>

<span data-ttu-id="0e013-110">Le système utilise un algorithme différent pour générer une liste DACL pour un nouvel objet Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0e013-110">The system uses a different algorithm to build a DACL for a new Active Directory object.</span></span> <span data-ttu-id="0e013-111">Pour plus d’informations, voir [Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="0e013-111">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
