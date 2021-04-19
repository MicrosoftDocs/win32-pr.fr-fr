---
description: La fonction PdhVbAddCounter crée une entrée de compteur dans l’objet de requête spécifié et retourne un handle à ce compteur en cas de réussite.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: PdhVbAddCounter fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520565"
---
# <a name="pdhvbaddcounter-function"></a><span data-ttu-id="909af-103">PdhVbAddCounter fonction)</span><span class="sxs-lookup"><span data-stu-id="909af-103">PdhVbAddCounter function</span></span>

<span data-ttu-id="909af-104">La fonction **PdhVbAddCounter** crée une entrée de compteur dans l’objet de requête spécifié et retourne un handle à ce compteur en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="909af-104">The **PdhVbAddCounter** function creates a counter entry in the specified query object, and returns a handle to that counter upon successful completion.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="909af-105">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="909af-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="909af-106">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="909af-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="909af-107">Function PdhVbAddCounter ( \_ ByVal QueryHandle As long, \_ ByVal trajet As String, \_ ByVal CounterHandle As long \_ ) As long</span><span class="sxs-lookup"><span data-stu-id="909af-107">Function PdhVbAddCounter( \_ ByVal QueryHandle As Long, \_ ByVal CounterPath As String, \_ ByVal CounterHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="909af-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="909af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="909af-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="909af-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="909af-110">ID de la requête à laquelle ce compteur doit être assigné.</span><span class="sxs-lookup"><span data-stu-id="909af-110">ID of the query to which this counter is to be assigned.</span></span> <span data-ttu-id="909af-111">Cette valeur est retournée par la fonction [**PdhVbOpenQuery**](pdhvbopenquery.md) .</span><span class="sxs-lookup"><span data-stu-id="909af-111">This value is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="909af-112">*CounterPath*</span><span class="sxs-lookup"><span data-stu-id="909af-112">*CounterPath*</span></span> 
</dt> <dd>

<span data-ttu-id="909af-113">Chaîne de texte qui spécifie le nom du chemin d’accès au compteur à ajouter à la requête.</span><span class="sxs-lookup"><span data-stu-id="909af-113">Text string that specifies the name of the counter path to add to the query.</span></span> <span data-ttu-id="909af-114">Le contenu de cette chaîne doit être un chemin de compteur valide, tel qu’il est obtenu à partir de l’Explorateur de compteurs ou d’une autre source.</span><span class="sxs-lookup"><span data-stu-id="909af-114">The contents of this string must be a valid counter path, as obtained from the counter browser or other source.</span></span>

</dd> <dt>

<span data-ttu-id="909af-115">*CounterHandle*</span><span class="sxs-lookup"><span data-stu-id="909af-115">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="909af-116">Référence unique qui identifie ce compteur dans la requête.</span><span class="sxs-lookup"><span data-stu-id="909af-116">Unique reference that identifies this counter in the query.</span></span> <span data-ttu-id="909af-117">Cette variable doit être initialisée à zéro avant que la fonction ne soit appelée.</span><span class="sxs-lookup"><span data-stu-id="909af-117">This variable must be initialized to zero before the function is called.</span></span> <span data-ttu-id="909af-118">Elle contient une valeur valide lors du retour uniquement si la fonction se termine correctement.</span><span class="sxs-lookup"><span data-stu-id="909af-118">It contains a valid value on return only if the function completes successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="909af-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="909af-119">Return value</span></span>

<span data-ttu-id="909af-120">Si la fonction réussit, elle retourne un entier **long** égal à \_ l’erreur Success et un nouveau handle dans la variable *CounterHandle* .</span><span class="sxs-lookup"><span data-stu-id="909af-120">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *CounterHandle* variable.</span></span>

<span data-ttu-id="909af-121">Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="909af-121">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="909af-122">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="909af-122">The following are possible values.</span></span>



| <span data-ttu-id="909af-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="909af-123">Return code</span></span>                                                                                                     | <span data-ttu-id="909af-124">Description</span><span class="sxs-lookup"><span data-stu-id="909af-124">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="909af-125"><dt>**PDH \_ argument non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="909af-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="909af-126">Un ou plusieurs des arguments sont non valides ou incorrects.</span><span class="sxs-lookup"><span data-stu-id="909af-126">One or more of the arguments is invalid or incorrect.</span></span><br/>              |
| <dl> <span data-ttu-id="909af-127"><dt>**\_échec d' \_ allocation de mémoire PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="909af-127"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="909af-128">Impossible d’allouer une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="909af-128">A memory buffer could not be allocated.</span></span><br/>                            |
| <dl> <span data-ttu-id="909af-129"><dt>**\_handle PDH non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="909af-129"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>             | <span data-ttu-id="909af-130">Le descripteur de requête n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="909af-130">The query handle is not valid.</span></span><br/>                                     |
| <dl> <span data-ttu-id="909af-131"><dt>**PDH \_ CSTATUS \_ aucun \_ compteur**</dt></span><span class="sxs-lookup"><span data-stu-id="909af-131"><dt>**PDH\_CSTATUS\_NO\_COUNTER**</dt></span></span> </dl>        | <span data-ttu-id="909af-132">Le compteur spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="909af-132">The specified counter was not found.</span></span><br/>                               |
| <dl> <span data-ttu-id="909af-133"><dt>**PDH \_ CSTATUS \_ aucun \_ objet**</dt></span><span class="sxs-lookup"><span data-stu-id="909af-133"><dt>**PDH\_CSTATUS\_NO\_OBJECT**</dt></span></span> </dl>         | <span data-ttu-id="909af-134">L’objet spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="909af-134">The specified object could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="909af-135"><dt>**PDH \_ CSTATUS \_ aucun \_ ordinateur**</dt></span><span class="sxs-lookup"><span data-stu-id="909af-135"><dt>**PDH\_CSTATUS\_NO\_MACHINE**</dt></span></span> </dl>        | <span data-ttu-id="909af-136">Une entrée d’ordinateur n’a pas pu être créée.</span><span class="sxs-lookup"><span data-stu-id="909af-136">A computer entry could not be created.</span></span><br/>                             |
| <dl> <span data-ttu-id="909af-137"><dt>**PDH \_ CSTATUS \_ , \_ COUNTERNAME incorrect**</dt></span><span class="sxs-lookup"><span data-stu-id="909af-137"><dt>**PDH\_CSTATUS\_BAD\_COUNTERNAME**</dt></span></span> </dl>   | <span data-ttu-id="909af-138">Une chaîne de chemin d’accès de nom de compteur vide a été transmise.</span><span class="sxs-lookup"><span data-stu-id="909af-138">An empty counter name path string was passed in.</span></span><br/>                   |
| <dl> <span data-ttu-id="909af-139"><dt>**\_fonction PDH \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="909af-139"><dt>**PDH\_FUNCTION\_NOT\_FOUND**</dt></span></span> </dl>        | <span data-ttu-id="909af-140">La fonction de calcul de ce compteur n’a pas pu être déterminée.</span><span class="sxs-lookup"><span data-stu-id="909af-140">The calculation function for this counter could not be determined.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="909af-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="909af-141">Requirements</span></span>



| <span data-ttu-id="909af-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="909af-142">Requirement</span></span> | <span data-ttu-id="909af-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="909af-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="909af-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="909af-144">Minimum supported client</span></span><br/> | <span data-ttu-id="909af-145">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="909af-145">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="909af-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="909af-146">Minimum supported server</span></span><br/> | <span data-ttu-id="909af-147">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="909af-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="909af-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="909af-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="909af-149"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="909af-149"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="909af-150">DLL</span><span class="sxs-lookup"><span data-stu-id="909af-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="909af-151"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="909af-151"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="909af-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="909af-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="909af-153">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="909af-153">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
</dt> </dl>

 

