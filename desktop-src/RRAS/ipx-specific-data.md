---
title: Structure de IPX_SPECIFIC_DATA (RTM. h)
description: La \_ structure de \_ données spécifique à IPX contient des données spécifiques à IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA de la structure RAS
- Point d’accès RAS du pointeur de structure PIPX_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941637"
---
# <a name="ipx_specific_data-structure"></a><span data-ttu-id="34259-105">\_Structure de données spécifique à IPX \_</span><span class="sxs-lookup"><span data-stu-id="34259-105">IPX\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="34259-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="34259-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="34259-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="34259-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="34259-108">La structure de **\_ \_ données spécifique à IPX** contient des données spécifiques à IPX.</span><span class="sxs-lookup"><span data-stu-id="34259-108">The **IPX\_SPECIFIC\_DATA** structure contains IPX-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="34259-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34259-109">Syntax</span></span>


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="34259-110">Membres</span><span class="sxs-lookup"><span data-stu-id="34259-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="34259-111">**\_Indicateurs FSD**</span><span class="sxs-lookup"><span data-stu-id="34259-111">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="34259-112">Spécifie des indicateurs qui décrivent l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="34259-112">Specifies flags that describe the route.</span></span> <span data-ttu-id="34259-113">Actuellement, ce membre est soit zéro, soit la valeur d’indicateur suivante.</span><span class="sxs-lookup"><span data-stu-id="34259-113">Currently, this member is either zero or the following flag value.</span></span>



| <span data-ttu-id="34259-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="34259-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="34259-115">Signification</span><span class="sxs-lookup"><span data-stu-id="34259-115">Meaning</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <span data-ttu-id="34259-116"><dt>**\_ \_ itinéraire WAN du client global \_ IPX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34259-116"><dt>**IPX\_GLOBAL\_CLIENT\_WAN\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="34259-117">Spécifie que cet itinéraire est destiné au réseau global alloué pour tous les clients WAN.</span><span class="sxs-lookup"><span data-stu-id="34259-117">Specifies that this route is for the global network allocated for all WAN clients.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="34259-118">**FSD \_ TickCount**</span><span class="sxs-lookup"><span data-stu-id="34259-118">**FSD\_TickCount**</span></span>
</dt> <dd>

<span data-ttu-id="34259-119">Spécifie le nombre de cycles nécessaires pour atteindre le réseau de destination.</span><span class="sxs-lookup"><span data-stu-id="34259-119">Specifies the number of ticks it takes to reach the destination network.</span></span> <span data-ttu-id="34259-120">Les protocoles de routage autres que RIP doivent convertir leurs mesures en graduations.</span><span class="sxs-lookup"><span data-stu-id="34259-120">Routing protocols other than RIP should convert their metrics into ticks.</span></span>

</dd> <dt>

<span data-ttu-id="34259-121">**FSD \_ HopCount**</span><span class="sxs-lookup"><span data-stu-id="34259-121">**FSD\_HopCount**</span></span>
</dt> <dd>

<span data-ttu-id="34259-122">Spécifie le nombre de tronçons associé à l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="34259-122">Specifies the hop count associated with the route.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34259-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34259-123">Requirements</span></span>



| <span data-ttu-id="34259-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34259-124">Requirement</span></span> | <span data-ttu-id="34259-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="34259-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="34259-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34259-126">Minimum supported client</span></span><br/> | <span data-ttu-id="34259-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="34259-127">None supported</span></span><br/>                                                        |
| <span data-ttu-id="34259-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34259-128">Minimum supported server</span></span><br/> | <span data-ttu-id="34259-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34259-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="34259-130">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="34259-130">End of server support</span></span><br/>    | <span data-ttu-id="34259-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34259-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="34259-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="34259-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="34259-133"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="34259-133"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34259-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34259-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34259-135">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="34259-135">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="34259-136">Structures de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="34259-136">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="34259-137">**\_itinéraire IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="34259-137">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





