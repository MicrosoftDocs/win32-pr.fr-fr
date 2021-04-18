---
description: La fonction PdhVbUpdateLog met à jour la requête actuelle et écrit de nouvelles données dans le fichier journal. Cette fonction appelle PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: PdhVbUpdateLog fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519900"
---
# <a name="pdhvbupdatelog-function"></a><span data-ttu-id="84221-104">PdhVbUpdateLog fonction)</span><span class="sxs-lookup"><span data-stu-id="84221-104">PdhVbUpdateLog function</span></span>

<span data-ttu-id="84221-105">La fonction **PdhVbUpdateLog** met à jour la requête actuelle et écrit de nouvelles données dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="84221-105">The **PdhVbUpdateLog** function function updates the current query and writes new data to the log file.</span></span> <span data-ttu-id="84221-106">Cette fonction appelle [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span><span class="sxs-lookup"><span data-stu-id="84221-106">This function calls [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84221-107">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="84221-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="84221-108">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="84221-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="84221-109">Function PdhVbUpdateLog ( \_ ByVal HLog en tant que PDH \_ hLog, \_ BYVAL szUserString As LPCTSTR \_ )</span><span class="sxs-lookup"><span data-stu-id="84221-109">Function PdhVbUpdateLog( \_ ByVal hLog As PDH\_HLOG, \_ ByVal szUserString As LPCTSTR \_ )</span></span>

## <a name="parameters"></a><span data-ttu-id="84221-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84221-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84221-111">*hLog* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84221-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84221-112">Handle du fichier journal à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="84221-112">Handle to the log file to be updated.</span></span> <span data-ttu-id="84221-113">Ce descripteur est retourné par la fonction [**PdhVbOpenLog**](pdhvbopenlog.md) .</span><span class="sxs-lookup"><span data-stu-id="84221-113">This handle is returned by the [**PdhVbOpenLog**](pdhvbopenlog.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="84221-114">*szUserString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84221-114">*szUserString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84221-115">Pointeur vers une chaîne qui spécifie les données à ajouter au fichier journal.</span><span class="sxs-lookup"><span data-stu-id="84221-115">Pointer to a string that specifies the data to be added to the log file.</span></span> <span data-ttu-id="84221-116">Il est généralement utilisé pour les commentaires dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="84221-116">This is generally used for comments within the log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84221-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84221-117">Return value</span></span>

<span data-ttu-id="84221-118">Si la fonction est réussie, elle retourne 0.</span><span class="sxs-lookup"><span data-stu-id="84221-118">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="84221-119">Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="84221-119">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="84221-120">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="84221-120">The following are possible values.</span></span>



| <span data-ttu-id="84221-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="84221-121">Return code</span></span>                                                                                                | <span data-ttu-id="84221-122">Description</span><span class="sxs-lookup"><span data-stu-id="84221-122">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84221-123"><dt>**\_mémoire tampon PDH insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="84221-123"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="84221-124">Les données demandées sont supérieures à la mémoire tampon fournie.</span><span class="sxs-lookup"><span data-stu-id="84221-124">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="84221-125">Impossible de retourner les données demandées.</span><span class="sxs-lookup"><span data-stu-id="84221-125">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="84221-126"><dt>**PDH \_ argument non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="84221-126"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="84221-127">Une ou plusieurs des mémoires tampons de chaîne n’ont pas la taille correcte.</span><span class="sxs-lookup"><span data-stu-id="84221-127">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="84221-128"><dt>**\_handle PDH non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="84221-128"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="84221-129">Le descripteur n’est pas un objet PDH valide.</span><span class="sxs-lookup"><span data-stu-id="84221-129">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="84221-130"><dt>**\_erreur d' \_ ouverture du fichier journal \_ PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="84221-130"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="84221-131">Impossible d’ouvrir le fichier journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="84221-131">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="84221-132"><dt>**\_fichier PDH \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="84221-132"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="84221-133">Impossible de trouver le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="84221-133">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="84221-134">Notes</span><span class="sxs-lookup"><span data-stu-id="84221-134">Remarks</span></span>

<span data-ttu-id="84221-135">Il doit y avoir une requête actuellement ouverte et les compteurs souhaités doivent y être ajoutés pour que cette fonction soit appelée.</span><span class="sxs-lookup"><span data-stu-id="84221-135">There must be a currently opened query, and the desired counters must be added to it before this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="84221-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84221-136">Requirements</span></span>



| <span data-ttu-id="84221-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84221-137">Requirement</span></span> | <span data-ttu-id="84221-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="84221-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84221-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84221-139">Minimum supported client</span></span><br/> | <span data-ttu-id="84221-140">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84221-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84221-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84221-141">Minimum supported server</span></span><br/> | <span data-ttu-id="84221-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84221-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="84221-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="84221-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="84221-144"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84221-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="84221-145">DLL</span><span class="sxs-lookup"><span data-stu-id="84221-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84221-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84221-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84221-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84221-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84221-148">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="84221-148">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[<span data-ttu-id="84221-149">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="84221-149">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="84221-150">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="84221-150">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> </dl>

 

