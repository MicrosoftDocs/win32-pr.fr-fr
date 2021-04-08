---
title: Structure MPSTATUS_DATA (MpClient. h)
description: Contient des données sur l’état actuel d’un composant du produit.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSTATUS_DATA
- PMPSTATUS_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742301"
---
# <a name="mpstatus_data-structure"></a><span data-ttu-id="ba42d-105">\_Structure de données MPSTATUS</span><span class="sxs-lookup"><span data-stu-id="ba42d-105">MPSTATUS\_DATA structure</span></span>

<span data-ttu-id="ba42d-106">Contient des données sur l’état actuel d’un composant du produit.</span><span class="sxs-lookup"><span data-stu-id="ba42d-106">Contains data about the current status of a component of the product.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba42d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba42d-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a><span data-ttu-id="ba42d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ba42d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba42d-109">**ComponentID**</span><span class="sxs-lookup"><span data-stu-id="ba42d-109">**ComponentID**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-110">Type : **[ **\_ ID MPCOMPONENT**](mpcomponent-id.md)**</span><span class="sxs-lookup"><span data-stu-id="ba42d-110">Type: **[**MPCOMPONENT\_ID**](mpcomponent-id.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-111">ID de composant spécifique pour lequel l’État est signalé.</span><span class="sxs-lookup"><span data-stu-id="ba42d-111">Specific component ID for which status is reported.</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-112">**fEnable**</span><span class="sxs-lookup"><span data-stu-id="ba42d-112">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-113">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="ba42d-113">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-114">État demandé pour le composant.</span><span class="sxs-lookup"><span data-stu-id="ba42d-114">Status requested for the component.</span></span> <span data-ttu-id="ba42d-115">**HRESULT** dans les données de rappel indique la réussite ou l’échec de la requête.</span><span class="sxs-lookup"><span data-stu-id="ba42d-115">**hResult** in the callback data signifies success or failure for the request.</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-116">**ComponentStatus**</span><span class="sxs-lookup"><span data-stu-id="ba42d-116">**ComponentStatus**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-117">Données d’État supplémentaires en fonction de la valeur de **ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-117">Extra status data depending on value of **ComponentID**.</span></span>

> [!Note]  
> <span data-ttu-id="ba42d-118">Génère actuellement un pointeur vers une structure factice pour toutes les valeurs possibles de **ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-118">Currently results in a pointer to a dummy structure for all possible values of **ComponentID**.</span></span>

 

<dl> <dt>

<span data-ttu-id="ba42d-119">**P1**</span><span class="sxs-lookup"><span data-stu-id="ba42d-119">**p1**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-120">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-120">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-121">Quand **ComponentID**  ==  **MPCOMPONENT \_ comme \_ signature**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-121">When **ComponentID** == **MPCOMPONENT\_AS\_SIGNATURE**.</span></span> <span data-ttu-id="ba42d-122">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-122">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-123">**S2**</span><span class="sxs-lookup"><span data-stu-id="ba42d-123">**p2**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-124">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-124">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-125">Lorsque l' **ID** de la  ==  **\_ \_ signature AV MPCOMPONENT**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-125">When **ComponentID** == **MPCOMPONENT\_AV\_SIGNATURE**.</span></span> <span data-ttu-id="ba42d-126">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-126">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-127">**P3**</span><span class="sxs-lookup"><span data-stu-id="ba42d-127">**p3**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-128">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-128">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-129">Quand l'  ==  **\_ \_ analyse en temps réel** de l’ID d’MPCOMPONENT.</span><span class="sxs-lookup"><span data-stu-id="ba42d-129">When **ComponentID** == **MPCOMPONENT\_REALTIME\_MONITOR**.</span></span> <span data-ttu-id="ba42d-130">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-130">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-131">**P4**</span><span class="sxs-lookup"><span data-stu-id="ba42d-131">**p4**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-132">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-132">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-133">Quand **ComponentID**  ==  **MPCOMPONENT \_ onaccess \_ protection**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-133">When **ComponentID** == **MPCOMPONENT\_ONACCESS\_PROTECTION**.</span></span> <span data-ttu-id="ba42d-134">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-134">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-135">**P5**</span><span class="sxs-lookup"><span data-stu-id="ba42d-135">**p5**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-136">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-136">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-137">Quand **ComponentID**  ==  **MPCOMPONENT \_ IOAV \_ protection**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-137">When **ComponentID** == **MPCOMPONENT\_IOAV\_PROTECTION**.</span></span> <span data-ttu-id="ba42d-138">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-138">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-139">**P6**</span><span class="sxs-lookup"><span data-stu-id="ba42d-139">**p6**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-140">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-140">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-141">Quand l'  ==  **\_ \_ analyse du comportement MPCOMPONENT** de l’ID de la.</span><span class="sxs-lookup"><span data-stu-id="ba42d-141">When **ComponentID** == **MPCOMPONENT\_BEHAVIOR\_MONITOR**.</span></span> <span data-ttu-id="ba42d-142">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-142">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-143">**P7**</span><span class="sxs-lookup"><span data-stu-id="ba42d-143">**p7**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-144">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-144">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-145">Lors de l'  ==  **\_ \_ analyse automatique** de l’ID d’MPCOMPONENT.</span><span class="sxs-lookup"><span data-stu-id="ba42d-145">When **ComponentID** == **MPCOMPONENT\_AUTO\_SCAN**.</span></span> <span data-ttu-id="ba42d-146">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-146">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-147">**P8**</span><span class="sxs-lookup"><span data-stu-id="ba42d-147">**p8**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-148">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-148">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-149">Quand **ComponentID**  ==  **MPCOMPONENT \_ auto \_ SIGUPDATE**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-149">When **ComponentID** == **MPCOMPONENT\_AUTO\_SIGUPDATE**.</span></span> <span data-ttu-id="ba42d-150">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-150">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-151">**P9**</span><span class="sxs-lookup"><span data-stu-id="ba42d-151">**p9**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-152">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-152">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-153">Quand **ComponentID**  ==  **MPCOMPONENT \_ IPC**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-153">When **ComponentID** == **MPCOMPONENT\_IPC**.</span></span> <span data-ttu-id="ba42d-154">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-154">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-155">**activation**</span><span class="sxs-lookup"><span data-stu-id="ba42d-155">**pa**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-156">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-156">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-157">Quand **ComponentID**  ==  **MPCOMPONENT \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-157">When **ComponentID** == **MPCOMPONENT\_NIS**.</span></span> <span data-ttu-id="ba42d-158">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-158">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba42d-159">**gérés**</span><span class="sxs-lookup"><span data-stu-id="ba42d-159">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="ba42d-160">Type : **PMPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-160">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="ba42d-161">Quand **ComponentID**  ==  **MPCOMPONENT \_ Elam**.</span><span class="sxs-lookup"><span data-stu-id="ba42d-161">When **ComponentID** == **MPCOMPONENT\_ELAM**.</span></span> <span data-ttu-id="ba42d-162">Consultez [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="ba42d-162">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba42d-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba42d-163">Requirements</span></span>



| <span data-ttu-id="ba42d-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba42d-164">Requirement</span></span> | <span data-ttu-id="ba42d-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba42d-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba42d-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba42d-166">Minimum supported client</span></span><br/> | <span data-ttu-id="ba42d-167">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba42d-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ba42d-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba42d-168">Minimum supported server</span></span><br/> | <span data-ttu-id="ba42d-169">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba42d-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba42d-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba42d-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba42d-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba42d-171"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba42d-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba42d-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba42d-173">**\_ID MPCOMPONENT**</span><span class="sxs-lookup"><span data-stu-id="ba42d-173">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="ba42d-174">**MPSTATUS \_ DATAEX \_ inutilisé**</span><span class="sxs-lookup"><span data-stu-id="ba42d-174">**MPSTATUS\_DATAEX\_UNUSED**</span></span>](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





