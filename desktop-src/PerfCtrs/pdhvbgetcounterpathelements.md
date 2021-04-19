---
description: La fonction PdhVbGetCounterPathElements analyse une chaîne de chemin d’accès au compteur de performance complet dans ses éléments individuels.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: PdhVbGetCounterPathElements fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517855"
---
# <a name="pdhvbgetcounterpathelements-function"></a><span data-ttu-id="d8d1e-103">PdhVbGetCounterPathElements fonction)</span><span class="sxs-lookup"><span data-stu-id="d8d1e-103">PdhVbGetCounterPathElements function</span></span>

<span data-ttu-id="d8d1e-104">La fonction **PdhVbGetCounterPathElements** analyse une chaîne de chemin d’accès au compteur de performance complet dans ses éléments individuels.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-104">The **PdhVbGetCounterPathElements** function parses a fully qualified performance counter path string into its individual elements.</span></span> <span data-ttu-id="d8d1e-105">Chacune des variables de chaîne doit avoir la même taille (*bufferSize*) et être dimensionnée et initialisée avant d’être utilisée dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-105">Each of the string variables must be the same size (*BufferSize*) and dimensioned and initialized before it is used in this function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8d1e-106">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-106">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="d8d1e-107">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d8d1e-107">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="d8d1e-108">Function PdhVbGetCounterPathElements ( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal InstanceName As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal bufferSize As long \_ ) As long</span><span class="sxs-lookup"><span data-stu-id="d8d1e-108">Function PdhVbGetCounterPathElements( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal InstanceName As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal BufferSize As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="d8d1e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8d1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8d1e-110">*PathString*</span><span class="sxs-lookup"><span data-stu-id="d8d1e-110">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d1e-111">Chaîne du chemin d’accès du compteur qui doit être divisée en ses éléments individuels.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-111">Counter path string that is to be broken up into its individual elements.</span></span>

</dd> <dt>

<span data-ttu-id="d8d1e-112">*MachineName*</span><span class="sxs-lookup"><span data-stu-id="d8d1e-112">*MachineName*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d1e-113">Chaîne devant recevoir le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-113">String to receive the computer name.</span></span>

</dd> <dt>

<span data-ttu-id="d8d1e-114">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="d8d1e-114">*ObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d1e-115">Chaîne devant recevoir le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-115">String to receive the object name.</span></span>

</dd> <dt>

<span data-ttu-id="d8d1e-116">*InstanceName*</span><span class="sxs-lookup"><span data-stu-id="d8d1e-116">*InstanceName*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d1e-117">Chaîne devant recevoir le nom de l’instance, s’il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-117">String to receive the instance name, if used.</span></span>

</dd> <dt>

<span data-ttu-id="d8d1e-118">*ParentInstance*</span><span class="sxs-lookup"><span data-stu-id="d8d1e-118">*ParentInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d1e-119">Chaîne devant recevoir l’instance parente, si elle est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-119">String to receive the parent instance, if used.</span></span>

</dd> <dt>

<span data-ttu-id="d8d1e-120">*CounterName*</span><span class="sxs-lookup"><span data-stu-id="d8d1e-120">*CounterName*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d1e-121">Chaîne qui reçoit le nom du compteur.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-121">String to receive the counter name.</span></span>

</dd> <dt>

<span data-ttu-id="d8d1e-122">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="d8d1e-122">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d1e-123">Taille maximale de chaque variable de chaîne utilisée en tant que paramètre pour cet appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-123">Maximum size of each string variable used as a parameter to this function call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8d1e-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8d1e-124">Return value</span></span>

<span data-ttu-id="d8d1e-125">Si la fonction réussit, elle retourne un entier **long** égal à la réussite de l’erreur \_ .</span><span class="sxs-lookup"><span data-stu-id="d8d1e-125">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS.</span></span>

<span data-ttu-id="d8d1e-126">Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d8d1e-126">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="d8d1e-127">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-127">The following are possible values.</span></span>



| <span data-ttu-id="d8d1e-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d8d1e-128">Return code</span></span>                                                                                                     | <span data-ttu-id="d8d1e-129">Description</span><span class="sxs-lookup"><span data-stu-id="d8d1e-129">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8d1e-130"><dt>**PDH \_ argument non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8d1e-130"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="d8d1e-131">Une ou plusieurs des mémoires tampons de chaîne n’ont pas la taille correcte.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-131">One or more of the string buffers is not the correct size.</span></span><br/>                          |
| <dl> <span data-ttu-id="d8d1e-132"><dt>**PDH \_ \_ données supplémentaires**</dt></span><span class="sxs-lookup"><span data-stu-id="d8d1e-132"><dt>**PDH\_MORE\_DATA**</dt></span></span> </dl>                  | <span data-ttu-id="d8d1e-133">Un ou plusieurs éléments du chemin d’accès du compteur sont trop volumineux pour la longueur de la mémoire tampon de retour.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-133">One or more of the counter path elements is too large for the return buffer length.</span></span><br/> |
| <dl> <span data-ttu-id="d8d1e-134"><dt>**\_échec d' \_ allocation de mémoire PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8d1e-134"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="d8d1e-135">Impossible d’allouer une mémoire tampon temporaire.</span><span class="sxs-lookup"><span data-stu-id="d8d1e-135">A temporary memory buffer could not be allocated.</span></span><br/>                                   |



 

## <a name="requirements"></a><span data-ttu-id="d8d1e-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8d1e-136">Requirements</span></span>



| <span data-ttu-id="d8d1e-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8d1e-137">Requirement</span></span> | <span data-ttu-id="d8d1e-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8d1e-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d1e-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8d1e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d8d1e-140">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8d1e-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8d1e-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8d1e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d8d1e-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8d1e-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d8d1e-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8d1e-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8d1e-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8d1e-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8d1e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d8d1e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8d1e-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8d1e-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8d1e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8d1e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d1e-148">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="d8d1e-148">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="d8d1e-149">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="d8d1e-149">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="d8d1e-150">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="d8d1e-150">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

