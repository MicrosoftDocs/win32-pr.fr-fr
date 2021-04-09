---
description: Définit des droits standard, spécifiques et génériques. Ces droits sont utilisés dans les entrées de contrôle d’accès (ACE) et constituent le moyen principal de spécifier l’accès demandé ou accordé à un objet.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115334"
---
# <a name="access_mask"></a><span data-ttu-id="d3449-104">masque d’accès \_</span><span class="sxs-lookup"><span data-stu-id="d3449-104">ACCESS\_MASK</span></span>

<span data-ttu-id="d3449-105">Le type de données **\_ masque d’accès** est une valeur **DWORD** qui définit des droits standard, spécifiques et génériques.</span><span class="sxs-lookup"><span data-stu-id="d3449-105">The **ACCESS\_MASK** data type is a **DWORD** value that defines standard, specific, and generic rights.</span></span> <span data-ttu-id="d3449-106">Ces droits sont utilisés dans les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) et constituent le moyen principal de spécifier l’accès demandé ou accordé à un objet.</span><span class="sxs-lookup"><span data-stu-id="d3449-106">These rights are used in [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and are the primary means of specifying the requested or granted access to an object.</span></span>


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a><span data-ttu-id="d3449-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d3449-107">Remarks</span></span>

<span data-ttu-id="d3449-108">Les bits de cette valeur sont alloués comme suit.</span><span class="sxs-lookup"><span data-stu-id="d3449-108">The bits in this value are allocated as follows.</span></span>



| <span data-ttu-id="d3449-109">Bits</span><span class="sxs-lookup"><span data-stu-id="d3449-109">Bits</span></span>             | <span data-ttu-id="d3449-110">Signification</span><span class="sxs-lookup"><span data-stu-id="d3449-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3449-111">0 15</span><span class="sxs-lookup"><span data-stu-id="d3449-111">0 15</span></span><br/>  | <span data-ttu-id="d3449-112">Droits spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d3449-112">Specific rights.</span></span> <span data-ttu-id="d3449-113">Contient le masque d’accès spécifique au type d’objet associé au masque.</span><span class="sxs-lookup"><span data-stu-id="d3449-113">Contains the access mask specific to the object type associated with the mask.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d3449-114">16 23</span><span class="sxs-lookup"><span data-stu-id="d3449-114">16 23</span></span><br/> | <span data-ttu-id="d3449-115">Droits standard.</span><span class="sxs-lookup"><span data-stu-id="d3449-115">Standard rights.</span></span> <span data-ttu-id="d3449-116">Contient les droits d’accès standard de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d3449-116">Contains the object's standard access rights.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d3449-117">24</span><span class="sxs-lookup"><span data-stu-id="d3449-117">24</span></span><br/>    | <span data-ttu-id="d3449-118">Accédez à la sécurité du système (**accès à la \_ \_ sécurité du système**).</span><span class="sxs-lookup"><span data-stu-id="d3449-118">Access system security (**ACCESS\_SYSTEM\_SECURITY**).</span></span> <span data-ttu-id="d3449-119">Il est utilisé pour indiquer l’accès à une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="d3449-119">It is used to indicate access to a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="d3449-120">Ce type d’accès nécessite que le processus appelant ait le **privilège \_ \_ nom de sécurité se** (gérer le journal d’audit et de sécurité).</span><span class="sxs-lookup"><span data-stu-id="d3449-120">This type of access requires the calling process to have the **SE\_SECURITY\_NAME** (Manage auditing and security log) privilege.</span></span> <span data-ttu-id="d3449-121">Si cet indicateur est défini dans le masque d’accès d’une entrée de contrôle d’accès d’audit (succès ou échec de l’accès), l’accès à la liste SACL est audité.</span><span class="sxs-lookup"><span data-stu-id="d3449-121">If this flag is set in the access mask of an audit access ACE (successful or unsuccessful access), the SACL access will be audited.</span></span><br/> |
| <span data-ttu-id="d3449-122">25</span><span class="sxs-lookup"><span data-stu-id="d3449-122">25</span></span><br/>    | <span data-ttu-id="d3449-123">Maximum autorisé (**maximum \_ autorisé**).</span><span class="sxs-lookup"><span data-stu-id="d3449-123">Maximum allowed (**MAXIMUM\_ALLOWED**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d3449-124">26 27</span><span class="sxs-lookup"><span data-stu-id="d3449-124">26 27</span></span><br/> | <span data-ttu-id="d3449-125">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d3449-125">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d3449-126">28</span><span class="sxs-lookup"><span data-stu-id="d3449-126">28</span></span><br/>    | <span data-ttu-id="d3449-127">Générique tout (**générique \_ tout**).</span><span class="sxs-lookup"><span data-stu-id="d3449-127">Generic all (**GENERIC\_ALL**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d3449-128">29</span><span class="sxs-lookup"><span data-stu-id="d3449-128">29</span></span><br/>    | <span data-ttu-id="d3449-129">Exécution générique (**\_ Exécution générique**).</span><span class="sxs-lookup"><span data-stu-id="d3449-129">Generic execute (**GENERIC\_EXECUTE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d3449-130">30</span><span class="sxs-lookup"><span data-stu-id="d3449-130">30</span></span><br/>    | <span data-ttu-id="d3449-131">Écriture générique (**\_ écriture générique**).</span><span class="sxs-lookup"><span data-stu-id="d3449-131">Generic write (**GENERIC\_WRITE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d3449-132">31</span><span class="sxs-lookup"><span data-stu-id="d3449-132">31</span></span><br/>    | <span data-ttu-id="d3449-133">Lecture générique (**\_ lecture générique**).</span><span class="sxs-lookup"><span data-stu-id="d3449-133">Generic read (**GENERIC\_READ**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="d3449-134">Les bits de droits standard, 16 à 23, contiennent les droits d’accès standard de l’objet et peuvent être une combinaison des indicateurs prédéfinis suivants.</span><span class="sxs-lookup"><span data-stu-id="d3449-134">Standard rights bits, 16 to 23, contain the object's standard access rights and can be a combination of the following predefined flags.</span></span>



| <span data-ttu-id="d3449-135">bit</span><span class="sxs-lookup"><span data-stu-id="d3449-135">Bit</span></span>           | <span data-ttu-id="d3449-136">Indicateur</span><span class="sxs-lookup"><span data-stu-id="d3449-136">Flag</span></span>                         | <span data-ttu-id="d3449-137">Signification</span><span class="sxs-lookup"><span data-stu-id="d3449-137">Meaning</span></span>                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3449-138">16</span><span class="sxs-lookup"><span data-stu-id="d3449-138">16</span></span><br/> | <span data-ttu-id="d3449-139">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="d3449-139">**DELETE**</span></span><br/>        | <span data-ttu-id="d3449-140">Supprimer l’accès.</span><span class="sxs-lookup"><span data-stu-id="d3449-140">Delete access.</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="d3449-141">17</span><span class="sxs-lookup"><span data-stu-id="d3449-141">17</span></span><br/> | <span data-ttu-id="d3449-142">**LIRE \_ le contrôle**</span><span class="sxs-lookup"><span data-stu-id="d3449-142">**READ\_CONTROL**</span></span><br/> | <span data-ttu-id="d3449-143">Accès en lecture au propriétaire, au groupe et à la [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d3449-143">Read access to the owner, group, and [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the security descriptor.</span></span><br/> |
| <span data-ttu-id="d3449-144">18</span><span class="sxs-lookup"><span data-stu-id="d3449-144">18</span></span><br/> | <span data-ttu-id="d3449-145">**ÉCRITURE \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="d3449-145">**WRITE\_DAC**</span></span><br/>    | <span data-ttu-id="d3449-146">Accès en écriture à la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="d3449-146">Write access to the DACL.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="d3449-147">19</span><span class="sxs-lookup"><span data-stu-id="d3449-147">19</span></span><br/> | <span data-ttu-id="d3449-148">**propriétaire en écriture \_**</span><span class="sxs-lookup"><span data-stu-id="d3449-148">**WRITE\_OWNER**</span></span><br/>  | <span data-ttu-id="d3449-149">Accès en écriture au propriétaire.</span><span class="sxs-lookup"><span data-stu-id="d3449-149">Write access to owner.</span></span><br/>                                                                                                                                                                                                        |
| <span data-ttu-id="d3449-150">20</span><span class="sxs-lookup"><span data-stu-id="d3449-150">20</span></span><br/> | <span data-ttu-id="d3449-151">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="d3449-151">**SYNCHRONIZE**</span></span><br/>   | <span data-ttu-id="d3449-152">Synchronisez l’accès.</span><span class="sxs-lookup"><span data-stu-id="d3449-152">Synchronize access.</span></span><br/>                                                                                                                                                                                                           |



 

<span data-ttu-id="d3449-153">Les constantes suivantes définies dans Winnt. h représentent les droits d’accès spécifiques et standard.</span><span class="sxs-lookup"><span data-stu-id="d3449-153">The following constants defined in Winnt.h represent the specific and standard access rights.</span></span>


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a><span data-ttu-id="d3449-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3449-154">Requirements</span></span>



| <span data-ttu-id="d3449-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3449-155">Requirement</span></span> | <span data-ttu-id="d3449-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3449-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3449-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3449-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d3449-158">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3449-158">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d3449-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3449-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d3449-160">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3449-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d3449-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3449-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3449-162"><dt>Winnt. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3449-162"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3449-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3449-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3449-164">Contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="d3449-164">Access Control</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="d3449-165">Structures de Access Control de base</span><span class="sxs-lookup"><span data-stu-id="d3449-165">Basic Access Control Structures</span></span>](authorization-structures.md)
</dt> <dt>

[<span data-ttu-id="d3449-166">Droits d’accès et masques d’accès</span><span class="sxs-lookup"><span data-stu-id="d3449-166">Access Rights and Access Masks</span></span>](access-rights-and-access-masks.md)
</dt> <dt>

[<span data-ttu-id="d3449-167">**\_mappage générique**</span><span class="sxs-lookup"><span data-stu-id="d3449-167">**GENERIC\_MAPPING**</span></span>](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

