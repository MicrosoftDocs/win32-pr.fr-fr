---
description: Indicateurs qui limitent les données à définir ou à retourner.
title: SRRF (Shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034668"
---
# <a name="srrf"></a><span data-ttu-id="5d14f-103">SRRF</span><span class="sxs-lookup"><span data-stu-id="5d14f-103">SRRF</span></span>

<span data-ttu-id="5d14f-104">Indicateurs qui limitent les données à définir ou à retourner.</span><span class="sxs-lookup"><span data-stu-id="5d14f-104">Flags that restrict the data to be set or returned.</span></span>



| <span data-ttu-id="5d14f-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="5d14f-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="5d14f-106">Description</span><span class="sxs-lookup"><span data-stu-id="5d14f-106">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <span data-ttu-id="5d14f-107"><dt>**SRRF \_ RT \_ reg \_ None**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-107"><dt>**SRRF\_RT\_REG\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="5d14f-108">Tapez REG \_ None.</span><span class="sxs-lookup"><span data-stu-id="5d14f-108">Type REG\_NONE.</span></span><br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <span data-ttu-id="5d14f-109"><dt>**SRRF \_ RT \_ reg \_**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-109"><dt>**SRRF\_RT\_REG\_SZ**</dt> <dt>0x00000002</dt></span></span> </dl>                       | <span data-ttu-id="5d14f-110">Tapez REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="5d14f-110">Type REG\_SZ.</span></span> <span data-ttu-id="5d14f-111">\_ \_ Les types reg Expand SZ sont convertis automatiquement en reg \_ SZ, sauf si l' \_ indicateur NOEXPAND SRRF est spécifié.</span><span class="sxs-lookup"><span data-stu-id="5d14f-111">REG\_EXPAND\_SZ types are automatically converted to REG\_SZ unless the SRRF\_NOEXPAND flag is specified.</span></span><br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <span data-ttu-id="5d14f-112"><dt>**SRRF \_ RT \_ reg \_ développer \_ SZ**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-112"><dt>**SRRF\_RT\_REG\_EXPAND\_SZ**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="5d14f-113">Tapez REG \_ expand \_ sz.</span><span class="sxs-lookup"><span data-stu-id="5d14f-113">Type REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="5d14f-114">Si vous récupérez une valeur, vous devez également obtenir l' \_ indicateur NOEXPAND SRRF, ou [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) échoue avec le \_ paramètre error non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="5d14f-114">If retrieving a value, you must also get the SRRF\_NOEXPAND flag, or [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) fails with ERROR\_INVALID\_PARAMETER.</span></span><br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <span data-ttu-id="5d14f-115"><dt>**SRRF \_ RT \_ reg \_ binaire**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-115"><dt>**SRRF\_RT\_REG\_BINARY**</dt> <dt>0x00000008</dt></span></span> </dl>           | <span data-ttu-id="5d14f-116">Tapez REG \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="5d14f-116">Type REG\_BINARY.</span></span><br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <span data-ttu-id="5d14f-117"><dt>**SRRF \_ RT \_ reg ( \_ DWORD**</dt> ) <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-117"><dt>**SRRF\_RT\_REG\_DWORD**</dt> <dt>0x00000010</dt></span></span> </dl>              | <span data-ttu-id="5d14f-118">Tapez REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="5d14f-118">Type REG\_DWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <span data-ttu-id="5d14f-119"><dt>**SRRF \_ RT \_ reg \_ multi- \_ SZ**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-119"><dt>**SRRF\_RT\_REG\_MULTI\_SZ**</dt> <dt>0x00000020</dt></span></span> </dl>    | <span data-ttu-id="5d14f-120">Tapez REG \_ multi \_ sz.</span><span class="sxs-lookup"><span data-stu-id="5d14f-120">Type REG\_MULTI\_SZ.</span></span><br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <span data-ttu-id="5d14f-121"><dt>**SRRF \_ RT \_ reg \_**</dt> <dt>0x00000040</dt> QWord</span><span class="sxs-lookup"><span data-stu-id="5d14f-121"><dt>**SRRF\_RT\_REG\_QWORD**</dt> <dt>0x00000040</dt></span></span> </dl>              | <span data-ttu-id="5d14f-122">Tapez REG \_ QWORD.</span><span class="sxs-lookup"><span data-stu-id="5d14f-122">Type REG\_QWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <span data-ttu-id="5d14f-123"><dt>**SRRF \_ RT \_ DWORD**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-123"><dt>**SRRF\_RT\_DWORD**</dt> <dt>0x00000018</dt></span></span> </dl>                           | <span data-ttu-id="5d14f-124">\_Types de fichiers binaires reg DWORD et 32 bits \_ .</span><span class="sxs-lookup"><span data-stu-id="5d14f-124">REG\_DWORD and 32-bit REG\_BINARY types.</span></span> <span data-ttu-id="5d14f-125">Cette valeur est équivalente à SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg reg \_ .</span><span class="sxs-lookup"><span data-stu-id="5d14f-125">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_DWORD.</span></span> <span data-ttu-id="5d14f-126">Si vous récupérez une valeur, si les données binaires de la valeur sont supérieures à 32 bits, elles ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="5d14f-126">If retrieving a value, if the value's binary data is larger than 32 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <span data-ttu-id="5d14f-127"><dt>**SRRF \_ RT \_ QWord**</dt> <dt>0x00000048</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-127"><dt>**SRRF\_RT\_QWORD**</dt> <dt>0x00000048</dt></span></span> </dl>                           | <span data-ttu-id="5d14f-128">\_Types de fichiers binaires reg QWord et 64 bits \_ .</span><span class="sxs-lookup"><span data-stu-id="5d14f-128">REG\_QWORD and 64-bit REG\_BINARY types.</span></span> <span data-ttu-id="5d14f-129">Cela équivaut à SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ QWORD.</span><span class="sxs-lookup"><span data-stu-id="5d14f-129">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_QWORD.</span></span> <span data-ttu-id="5d14f-130">Si vous récupérez une valeur, si les données binaires de la valeur sont supérieures à 64 bits, elles ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="5d14f-130">If retrieving a value, if the value's binary data is larger than 64 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <span data-ttu-id="5d14f-131"><dt>**SRRF \_ RT \_ any**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-131"><dt>**SRRF\_RT\_ANY**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                                 | <span data-ttu-id="5d14f-132">Tous les types.</span><span class="sxs-lookup"><span data-stu-id="5d14f-132">All types.</span></span> <span data-ttu-id="5d14f-133">Définissez cet indicateur si aucune autre \_ valeur SRRF RT n’est définie.</span><span class="sxs-lookup"><span data-stu-id="5d14f-133">Set this flag if no other SRRF\_RT value is set.</span></span><br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <span data-ttu-id="5d14f-134"><dt>**SRRF \_ RM \_ n’importe quel**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-134"><dt>**SRRF\_RM\_ANY**</dt> <dt>0x00000000</dt></span></span> </dl>                                 | <span data-ttu-id="5d14f-135">Aucune restriction de mode.</span><span class="sxs-lookup"><span data-stu-id="5d14f-135">No mode restriction.</span></span> <span data-ttu-id="5d14f-136">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5d14f-136">This is the default value.</span></span><br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <span data-ttu-id="5d14f-137"><dt>**SRRF \_ 0x00010000 \_ normale RM**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-137"><dt>**SRRF\_RM\_NORMAL**</dt> <dt>0x00010000</dt></span></span> </dl>                        | <span data-ttu-id="5d14f-138">Limitez le mode de démarrage du système à « démarrage normal ».</span><span class="sxs-lookup"><span data-stu-id="5d14f-138">Restrict system startup mode to "normal boot".</span></span><br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <span data-ttu-id="5d14f-139"><dt>**SRRF \_ 0x00020000 \_ sécurisé RM**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-139"><dt>**SRRF\_RM\_SAFE**</dt> <dt>0x00020000</dt></span></span> </dl>                              | <span data-ttu-id="5d14f-140">Limitez le mode de démarrage du système à « mode sans échec ».</span><span class="sxs-lookup"><span data-stu-id="5d14f-140">Restrict system startup mode to "safe mode".</span></span><br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <span data-ttu-id="5d14f-141"><dt>**SRRF \_ RM \_ SAFENETWORK**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-141"><dt>**SRRF\_RM\_SAFENETWORK**</dt> <dt>0x00040000</dt></span></span> </dl>         | <span data-ttu-id="5d14f-142">Limitez le mode de démarrage du système à « mode sans échec avec mise en réseau ».</span><span class="sxs-lookup"><span data-stu-id="5d14f-142">Restrict system startup mode to "safe mode with networking".</span></span><br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <span data-ttu-id="5d14f-143"><dt>**SRRF \_ NOEXPAND**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-143"><dt>**SRRF\_NOEXPAND**</dt> <dt>0x10000000</dt></span></span> </dl>                            | <span data-ttu-id="5d14f-144">Ne développez pas automatiquement les chaînes d’environnement de REG \_ expand \_ sz.</span><span class="sxs-lookup"><span data-stu-id="5d14f-144">Do not automatically expand REG\_EXPAND\_SZ environment strings.</span></span><br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <span data-ttu-id="5d14f-145"><dt>**SRRF \_ ZEROONFAILURE**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-145"><dt>**SRRF\_ZEROONFAILURE**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="5d14f-146">Si vous récupérez une valeur, si *pvData* n’est pas **null**, définissez le contenu de la mémoire tampon *pvData* sur tous les zéros en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5d14f-146">If retrieving a value, if *pvData* is not **NULL**, set the contents of the *pvData* buffer to all zeros on failure.</span></span><br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <span data-ttu-id="5d14f-147"><dt>**SRRF \_ NOVIRT**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-147"><dt>**SRRF\_NOVIRT**</dt> <dt>0x40000000</dt></span></span> </dl>                                  | <span data-ttu-id="5d14f-148">Lorsque vous récupérez une valeur, si la clé demandée est virtualisée, échec avec le fichier d’erreur \_ \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="5d14f-148">When retrieving a value, if the requested key is virtualized, fail with ERROR\_FILE\_NOT\_FOUND.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="5d14f-149">Notes</span><span class="sxs-lookup"><span data-stu-id="5d14f-149">Remarks</span></span>

<span data-ttu-id="5d14f-150">Ces valeurs sont définies dans Shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="5d14f-150">These values are defined in Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d14f-151">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5d14f-151">Requirements</span></span>



| <span data-ttu-id="5d14f-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d14f-152">Requirement</span></span> | <span data-ttu-id="5d14f-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d14f-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5d14f-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d14f-154">Minimum supported client</span></span><br/> | <span data-ttu-id="5d14f-155">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d14f-155">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5d14f-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d14f-156">Minimum supported server</span></span><br/> | <span data-ttu-id="5d14f-157">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d14f-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5d14f-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d14f-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d14f-159"><dt>Shlwapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d14f-159"><dt>Shlwapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d14f-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d14f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d14f-161">**SHRegSetValue**</span><span class="sxs-lookup"><span data-stu-id="5d14f-161">**SHRegSetValue**</span></span>](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[<span data-ttu-id="5d14f-162">**SHRegGetValue**</span><span class="sxs-lookup"><span data-stu-id="5d14f-162">**SHRegGetValue**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




