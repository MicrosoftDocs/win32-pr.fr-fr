---
description: La \_ structure d’informations sur le port \_ 3 spécifie la valeur d’état d’un port d’imprimante.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: Structure PORT_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529823"
---
# <a name="port_info_3-structure"></a><span data-ttu-id="f3c96-103">Structure des informations de PORT \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="f3c96-103">PORT\_INFO\_3 structure</span></span>

<span data-ttu-id="f3c96-104">La structure d' **\_ informations sur le port \_ 3** spécifie la valeur d’état d’un port d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f3c96-104">The **PORT\_INFO\_3** structure specifies the status value of a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c96-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3c96-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a><span data-ttu-id="f3c96-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f3c96-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3c96-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="f3c96-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="f3c96-108">Nouvelle valeur d’état de port.</span><span class="sxs-lookup"><span data-stu-id="f3c96-108">The new port status value.</span></span> <span data-ttu-id="f3c96-109">Cette valeur est utilisée uniquement si le membre **pszStatus** a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="f3c96-109">This value is used only if the **pszStatus** member is **NULL**.</span></span>

<span data-ttu-id="f3c96-110">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f3c96-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="f3c96-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3c96-111">Value</span></span>                            | <span data-ttu-id="f3c96-112">Signification</span><span class="sxs-lookup"><span data-stu-id="f3c96-112">Meaning</span></span>                                             |
|----------------------------------|-----------------------------------------------------|
| <span data-ttu-id="f3c96-113">0</span><span class="sxs-lookup"><span data-stu-id="f3c96-113">0</span></span>                                | <span data-ttu-id="f3c96-114">Efface l’état du port d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f3c96-114">Clears the printer port status.</span></span>                     |
| <span data-ttu-id="f3c96-115">État du PORT \_ \_ hors connexion</span><span class="sxs-lookup"><span data-stu-id="f3c96-115">PORT\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="f3c96-116">L’imprimante du port est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="f3c96-116">The port's printer is offline.</span></span>                      |
| <span data-ttu-id="f3c96-117">\_ \_ bourrage papier dans l’état du port \_</span><span class="sxs-lookup"><span data-stu-id="f3c96-117">PORT\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="f3c96-118">L’imprimante du port présente un bourrage papier.</span><span class="sxs-lookup"><span data-stu-id="f3c96-118">The port's printer has a paper jam.</span></span>                 |
| <span data-ttu-id="f3c96-119">\_ \_ sortie papier de l’état du port \_</span><span class="sxs-lookup"><span data-stu-id="f3c96-119">PORT\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="f3c96-120">L’imprimante du port n’est plus imprimée.</span><span class="sxs-lookup"><span data-stu-id="f3c96-120">The port's printer is out of paper.</span></span>                 |
| <span data-ttu-id="f3c96-121">bac de sortie de l’état du PORT \_ \_ \_ \_ plein</span><span class="sxs-lookup"><span data-stu-id="f3c96-121">PORT\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="f3c96-122">Le bac de sortie printer’s du port est plein.</span><span class="sxs-lookup"><span data-stu-id="f3c96-122">The port's printer's output bin is full.</span></span>            |
| <span data-ttu-id="f3c96-123">problème de papier sur l’état du PORT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3c96-123">PORT\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="f3c96-124">L’imprimante du port présente un problème de papier.</span><span class="sxs-lookup"><span data-stu-id="f3c96-124">The port's printer has a paper problem.</span></span>             |
| <span data-ttu-id="f3c96-125">État du PORT \_ \_ non \_ toner</span><span class="sxs-lookup"><span data-stu-id="f3c96-125">PORT\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="f3c96-126">L’imprimante du port est en dehors du toner.</span><span class="sxs-lookup"><span data-stu-id="f3c96-126">The port's printer is out of toner.</span></span>                 |
| <span data-ttu-id="f3c96-127">porte d’état de PORT \_ \_ \_ ouverte</span><span class="sxs-lookup"><span data-stu-id="f3c96-127">PORT\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="f3c96-128">La porte de l’imprimante du port est ouverte.</span><span class="sxs-lookup"><span data-stu-id="f3c96-128">The door of the port's printer is open.</span></span>             |
| <span data-ttu-id="f3c96-129">INTERVENTION de l’utilisateur sur l’état du PORT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3c96-129">PORT\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="f3c96-130">L’imprimante du port nécessite une intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3c96-130">The port's printer requires user intervention.</span></span>      |
| <span data-ttu-id="f3c96-131">\_ \_ mémoire insuffisante sur l’état \_ du \_ port</span><span class="sxs-lookup"><span data-stu-id="f3c96-131">PORT\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="f3c96-132">La mémoire de l’imprimante du port est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f3c96-132">The port's printer is out of memory.</span></span>                |
| <span data-ttu-id="f3c96-133">\_toner état \_ \_ faible du port</span><span class="sxs-lookup"><span data-stu-id="f3c96-133">PORT\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="f3c96-134">L’imprimante du port est faible sur le toner.</span><span class="sxs-lookup"><span data-stu-id="f3c96-134">The port's printer is low on toner.</span></span>                 |
| <span data-ttu-id="f3c96-135">État du PORT en \_ \_ préchauffage \_</span><span class="sxs-lookup"><span data-stu-id="f3c96-135">PORT\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="f3c96-136">L’imprimante du port est en état de préchauffage.</span><span class="sxs-lookup"><span data-stu-id="f3c96-136">The port's printer is warming up.</span></span>                   |
| <span data-ttu-id="f3c96-137">État du PORT-économie \_ \_ d’énergie \_</span><span class="sxs-lookup"><span data-stu-id="f3c96-137">PORT\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="f3c96-138">L’imprimante du port est en mode de conservation de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="f3c96-138">The port's printer is in a power-conservation mode.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f3c96-139">**pszStatus**</span><span class="sxs-lookup"><span data-stu-id="f3c96-139">**pszStatus**</span></span>
</dt> <dd>

<span data-ttu-id="f3c96-140">Pointeur vers une nouvelle chaîne de valeur d’état de port d’imprimante à définir.</span><span class="sxs-lookup"><span data-stu-id="f3c96-140">Pointer to a new printer port status value string to set.</span></span> <span data-ttu-id="f3c96-141">Utilisez ce membre s’il n’existe pas de valeur d’État appropriée parmi celles listées pour **dwStatus**.</span><span class="sxs-lookup"><span data-stu-id="f3c96-141">Use this member if there is no suitable status value among those listed for **dwStatus**.</span></span>

</dd> <dt>

<span data-ttu-id="f3c96-142">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="f3c96-142">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="f3c96-143">Gravité de la valeur de l’état du port.</span><span class="sxs-lookup"><span data-stu-id="f3c96-143">The severity of the port status value.</span></span>

<span data-ttu-id="f3c96-144">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f3c96-144">This member can be one of the following values.</span></span>



| <span data-ttu-id="f3c96-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3c96-145">Value</span></span>                       | <span data-ttu-id="f3c96-146">Signification</span><span class="sxs-lookup"><span data-stu-id="f3c96-146">Meaning</span></span>                                   |
|-----------------------------|-------------------------------------------|
| <span data-ttu-id="f3c96-147">\_erreur de \_ type d’état de port \_</span><span class="sxs-lookup"><span data-stu-id="f3c96-147">PORT\_STATUS\_TYPE\_ERROR</span></span>   | <span data-ttu-id="f3c96-148">La valeur de l’état du port indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="f3c96-148">The port status value indicates an error.</span></span> |
| <span data-ttu-id="f3c96-149">\_avertissement de \_ type d’état de port \_</span><span class="sxs-lookup"><span data-stu-id="f3c96-149">PORT\_STATUS\_TYPE\_WARNING</span></span> | <span data-ttu-id="f3c96-150">La valeur de l’état du port est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="f3c96-150">The port status value is a warning.</span></span>       |
| <span data-ttu-id="f3c96-151">\_ \_ informations sur le type d’État du port \_</span><span class="sxs-lookup"><span data-stu-id="f3c96-151">PORT\_STATUS\_TYPE\_INFO</span></span>    | <span data-ttu-id="f3c96-152">La valeur de l’état du port est informatif.</span><span class="sxs-lookup"><span data-stu-id="f3c96-152">The port status value is informational.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3c96-153">Notes</span><span class="sxs-lookup"><span data-stu-id="f3c96-153">Remarks</span></span>

<span data-ttu-id="f3c96-154">Lorsque vous définissez une valeur d’état de port d’imprimante avec la valeur de gravité \_ \_ erreur de type état du port \_ , le spouleur d’impression cesse d’envoyer des travaux au port.</span><span class="sxs-lookup"><span data-stu-id="f3c96-154">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="f3c96-155">Le spouleur d’impression ne reprend pas l’envoi des travaux au port jusqu’à ce qu’un autre appel [**SetPort**](setport.md) soit effectué pour effacer l’État.</span><span class="sxs-lookup"><span data-stu-id="f3c96-155">The print spooler does not resume sending jobs to the port until another [**SetPort**](setport.md) call is made to clear the status.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c96-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3c96-156">Requirements</span></span>



| <span data-ttu-id="f3c96-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3c96-157">Requirement</span></span> | <span data-ttu-id="f3c96-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3c96-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c96-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3c96-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c96-160">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3c96-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f3c96-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3c96-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c96-162">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3c96-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f3c96-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3c96-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3c96-164"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3c96-164"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f3c96-165">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f3c96-165">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f3c96-166">**\_ \_ Informations sur \_ le port 3W** (Unicode) et **\_ \_ informations sur le port \_ 3A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f3c96-166">**\_PORT\_INFO\_3W** (Unicode) and **\_PORT\_INFO\_3A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="f3c96-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3c96-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c96-168">Impression</span><span class="sxs-lookup"><span data-stu-id="f3c96-168">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f3c96-169">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="f3c96-169">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f3c96-170">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="f3c96-170">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




