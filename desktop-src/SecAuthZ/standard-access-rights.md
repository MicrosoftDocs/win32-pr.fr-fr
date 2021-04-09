---
description: Chaque type d’objet sécurisable possède un ensemble de droits d’accès qui correspondent à des opérations spécifiques à ce type d’objet.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Droits d’accès standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863002"
---
# <a name="standard-access-rights"></a><span data-ttu-id="d8c80-103">Droits d’accès standard</span><span class="sxs-lookup"><span data-stu-id="d8c80-103">Standard Access Rights</span></span>

<span data-ttu-id="d8c80-104">Chaque type d’objet sécurisable possède un ensemble de droits d’accès qui correspondent à des opérations spécifiques à ce type d’objet.</span><span class="sxs-lookup"><span data-stu-id="d8c80-104">Each type of securable object has a set of access rights that correspond to operations specific to that type of object.</span></span> <span data-ttu-id="d8c80-105">En plus de ces droits d’accès spécifiques aux objets, il existe un ensemble de droits d’accès standard qui correspondent à des opérations communes à la plupart des types d’objets sécurisables.</span><span class="sxs-lookup"><span data-stu-id="d8c80-105">In addition to these object-specific access rights, there is a set of standard access rights that correspond to operations common to most types of securable objects.</span></span>

<span data-ttu-id="d8c80-106">Le [format de masque d’accès](access-mask-format.md) comprend un ensemble de bits pour les droits d’accès standard.</span><span class="sxs-lookup"><span data-stu-id="d8c80-106">The [access mask format](access-mask-format.md) includes a set of bits for the standard access rights.</span></span> <span data-ttu-id="d8c80-107">Les constantes Windows suivantes pour les droits d’accès standard sont définies dans Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="d8c80-107">The following Windows constants for standard access rights are defined in Winnt.h.</span></span>



| <span data-ttu-id="d8c80-108">Constante</span><span class="sxs-lookup"><span data-stu-id="d8c80-108">Constant</span></span>      | <span data-ttu-id="d8c80-109">Signification</span><span class="sxs-lookup"><span data-stu-id="d8c80-109">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c80-110">Suppression</span><span class="sxs-lookup"><span data-stu-id="d8c80-110">DELETE</span></span>        | <span data-ttu-id="d8c80-111">Droit de supprimer l'objet.</span><span class="sxs-lookup"><span data-stu-id="d8c80-111">The right to delete the object.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d8c80-112">LIRE \_ le contrôle</span><span class="sxs-lookup"><span data-stu-id="d8c80-112">READ\_CONTROL</span></span> | <span data-ttu-id="d8c80-113">Droit de lire les informations du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)de l’objet, à l’exclusion des informations contenues dans la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="d8c80-113">The right to read the information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), not including the information in the [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> |
| <span data-ttu-id="d8c80-114">SYNCHRONIZE</span><span class="sxs-lookup"><span data-stu-id="d8c80-114">SYNCHRONIZE</span></span>   | <span data-ttu-id="d8c80-115">Droit d'utiliser l'objet pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="d8c80-115">The right to use the object for synchronization.</span></span> <span data-ttu-id="d8c80-116">Cela permet à un thread d’attendre jusqu’à ce que l’objet soit dans l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="d8c80-116">This enables a thread to wait until the object is in the signaled state.</span></span> <span data-ttu-id="d8c80-117">Certains types d’objets ne prennent pas en charge ce droit d’accès.</span><span class="sxs-lookup"><span data-stu-id="d8c80-117">Some object types do not support this access right.</span></span>                                                                                                                                                                |
| <span data-ttu-id="d8c80-118">ÉCRITURE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="d8c80-118">WRITE\_DAC</span></span>    | <span data-ttu-id="d8c80-119">Droit de modifier la [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) dans le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8c80-119">The right to modify the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) in the object's security descriptor.</span></span>                                                                                                                    |
| <span data-ttu-id="d8c80-120">propriétaire en écriture \_</span><span class="sxs-lookup"><span data-stu-id="d8c80-120">WRITE\_OWNER</span></span>  | <span data-ttu-id="d8c80-121">Droit de modifier le propriétaire défini dans le descripteur de sécurité de l'objet.</span><span class="sxs-lookup"><span data-stu-id="d8c80-121">The right to change the owner in the object's security descriptor.</span></span>                                                                                                                                                                                                                                                                           |



 

<span data-ttu-id="d8c80-122">Winnt. h définit également les combinaisons suivantes des constantes de droits d’accès standard.</span><span class="sxs-lookup"><span data-stu-id="d8c80-122">Winnt.h also defines the following combinations of the standard access rights constants.</span></span>



| <span data-ttu-id="d8c80-123">Constante</span><span class="sxs-lookup"><span data-stu-id="d8c80-123">Constant</span></span>                   | <span data-ttu-id="d8c80-124">Signification</span><span class="sxs-lookup"><span data-stu-id="d8c80-124">Meaning</span></span>                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d8c80-125">\_droits standard \_ tous</span><span class="sxs-lookup"><span data-stu-id="d8c80-125">STANDARD\_RIGHTS\_ALL</span></span>      | <span data-ttu-id="d8c80-126">Combine la suppression, \_ le contrôle de lecture, \_ l’écriture DAC, le propriétaire d’écriture \_ et l’accès de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="d8c80-126">Combines DELETE, READ\_CONTROL, WRITE\_DAC, WRITE\_OWNER, and SYNCHRONIZE access.</span></span> |
| <span data-ttu-id="d8c80-127">\_exécution des droits standard \_</span><span class="sxs-lookup"><span data-stu-id="d8c80-127">STANDARD\_RIGHTS\_EXECUTE</span></span>  | <span data-ttu-id="d8c80-128">Actuellement défini en tant que contrôle de lecture égal \_ .</span><span class="sxs-lookup"><span data-stu-id="d8c80-128">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="d8c80-129">\_droits de \_ lecture standard</span><span class="sxs-lookup"><span data-stu-id="d8c80-129">STANDARD\_RIGHTS\_READ</span></span>     | <span data-ttu-id="d8c80-130">Actuellement défini en tant que contrôle de lecture égal \_ .</span><span class="sxs-lookup"><span data-stu-id="d8c80-130">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="d8c80-131">\_droits standard \_ requis</span><span class="sxs-lookup"><span data-stu-id="d8c80-131">STANDARD\_RIGHTS\_REQUIRED</span></span> | <span data-ttu-id="d8c80-132">Combine les accès de suppression, de \_ contrôle de lecture, d’écriture \_ DAC et de propriétaire d’écriture \_ .</span><span class="sxs-lookup"><span data-stu-id="d8c80-132">Combines DELETE, READ\_CONTROL, WRITE\_DAC, and WRITE\_OWNER access.</span></span>              |
| <span data-ttu-id="d8c80-133">\_écriture des droits standard \_</span><span class="sxs-lookup"><span data-stu-id="d8c80-133">STANDARD\_RIGHTS\_WRITE</span></span>    | <span data-ttu-id="d8c80-134">Actuellement défini en tant que contrôle de lecture égal \_ .</span><span class="sxs-lookup"><span data-stu-id="d8c80-134">Currently defined to equal READ\_CONTROL.</span></span>                                         |



 

 

 
