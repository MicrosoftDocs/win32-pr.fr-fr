---
description: La fonction PdhVbGetLogFileSize retourne la taille du fichier journal spécifié. Cette fonction appelle PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: PdhVbGetLogFileSize fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536156"
---
# <a name="pdhvbgetlogfilesize-function"></a><span data-ttu-id="83390-104">PdhVbGetLogFileSize fonction)</span><span class="sxs-lookup"><span data-stu-id="83390-104">PdhVbGetLogFileSize function</span></span>

<span data-ttu-id="83390-105">La fonction **PdhVbGetLogFileSize** retourne la taille du fichier journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="83390-105">The **PdhVbGetLogFileSize** function returns the size of the specified log file.</span></span> <span data-ttu-id="83390-106">Cette fonction appelle [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span><span class="sxs-lookup"><span data-stu-id="83390-106">This function calls [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83390-107">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="83390-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="83390-108">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="83390-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="83390-109">Function PdhVbGetLogFileSize ( \_ ByVal HLog en tant que PDH \_ hLog, \_ ByRef llSize As long \_ ) As DWORD</span><span class="sxs-lookup"><span data-stu-id="83390-109">Function PdhVbGetLogFileSize( \_ ByVal hLog As PDH\_HLOG, \_ ByRef llSize As LONG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="83390-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83390-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83390-111">*hLog* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83390-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83390-112">Handle du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="83390-112">Handle to the log file.</span></span> <span data-ttu-id="83390-113">Ce descripteur est retourné par la fonction [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) .</span><span class="sxs-lookup"><span data-stu-id="83390-113">This handle is returned by the [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) function.</span></span>

</dd> <dt>

<span data-ttu-id="83390-114">*llSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="83390-114">*llSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83390-115">Pointeur vers une variable qui reçoit la taille du fichier journal, en octets.</span><span class="sxs-lookup"><span data-stu-id="83390-115">Pointer to a variable that receives the size of the log file, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83390-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83390-116">Return value</span></span>

<span data-ttu-id="83390-117">Si la fonction est réussie, elle retourne 0.</span><span class="sxs-lookup"><span data-stu-id="83390-117">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="83390-118">Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="83390-118">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="83390-119">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="83390-119">The following are possible values.</span></span>



| <span data-ttu-id="83390-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="83390-120">Return code</span></span>                                                                                                | <span data-ttu-id="83390-121">Description</span><span class="sxs-lookup"><span data-stu-id="83390-121">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83390-122"><dt>**\_mémoire tampon PDH insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83390-122"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="83390-123">Les données demandées sont supérieures à la mémoire tampon fournie.</span><span class="sxs-lookup"><span data-stu-id="83390-123">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="83390-124">Impossible de retourner les données demandées.</span><span class="sxs-lookup"><span data-stu-id="83390-124">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="83390-125"><dt>**PDH \_ argument non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83390-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="83390-126">Une ou plusieurs des mémoires tampons de chaîne n’ont pas la taille correcte.</span><span class="sxs-lookup"><span data-stu-id="83390-126">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="83390-127"><dt>**\_handle PDH non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83390-127"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="83390-128">Le descripteur n’est pas un objet PDH valide.</span><span class="sxs-lookup"><span data-stu-id="83390-128">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="83390-129"><dt>**\_erreur d' \_ ouverture du fichier journal \_ PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83390-129"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="83390-130">Impossible d’ouvrir le fichier journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="83390-130">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="83390-131"><dt>**\_fichier PDH \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="83390-131"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="83390-132">Impossible de trouver le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="83390-132">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="83390-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83390-133">Requirements</span></span>



| <span data-ttu-id="83390-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83390-134">Requirement</span></span> | <span data-ttu-id="83390-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="83390-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83390-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83390-136">Minimum supported client</span></span><br/> | <span data-ttu-id="83390-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83390-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83390-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83390-138">Minimum supported server</span></span><br/> | <span data-ttu-id="83390-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83390-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="83390-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="83390-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="83390-141"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83390-141"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="83390-142">DLL</span><span class="sxs-lookup"><span data-stu-id="83390-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83390-143"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83390-143"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83390-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83390-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83390-145">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="83390-145">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[<span data-ttu-id="83390-146">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="83390-146">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> <dt>

[<span data-ttu-id="83390-147">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="83390-147">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

