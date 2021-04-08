---
title: Structure de PROTOCOL_SPECIFIC_DATA (RTM. h)
description: La \_ structure de données spécifique au protocole \_ contient de la mémoire réservée pour les données spécifiques à un protocole de routage particulier.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- PROTOCOL_SPECIFIC_DATA de la structure RAS
- Point d’accès RAS du pointeur de structure PPROTOCOL_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742189"
---
# <a name="protocol_specific_data-structure"></a><span data-ttu-id="427b1-105">\_Structure de données spécifique au protocole \_</span><span class="sxs-lookup"><span data-stu-id="427b1-105">PROTOCOL\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="427b1-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="427b1-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="427b1-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="427b1-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="427b1-108">La structure de **\_ \_ données spécifique au protocole** contient de la mémoire réservée pour les données spécifiques à un protocole de routage particulier.</span><span class="sxs-lookup"><span data-stu-id="427b1-108">The **PROTOCOL\_SPECIFIC\_DATA** structure contains memory reserved for data specific to a particular routing protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="427b1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="427b1-109">Syntax</span></span>


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="427b1-110">Membres</span><span class="sxs-lookup"><span data-stu-id="427b1-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="427b1-111">**\_Données PSD**</span><span class="sxs-lookup"><span data-stu-id="427b1-111">**PSD\_Data**</span></span>
</dt> <dd>

<span data-ttu-id="427b1-112">Spécifie un tableau de variables **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="427b1-112">Specifies an array of **DWORD** variables.</span></span> <span data-ttu-id="427b1-113">Cette mémoire est réservée pour les données spécifiques aux protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="427b1-113">This memory is reserved for data that is specific to routing protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="427b1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="427b1-114">Requirements</span></span>



| <span data-ttu-id="427b1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="427b1-115">Requirement</span></span> | <span data-ttu-id="427b1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="427b1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="427b1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="427b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="427b1-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="427b1-118">None supported</span></span><br/>                                                        |
| <span data-ttu-id="427b1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="427b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="427b1-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="427b1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="427b1-121">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="427b1-121">End of server support</span></span><br/>    | <span data-ttu-id="427b1-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="427b1-122">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="427b1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="427b1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="427b1-124"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="427b1-124"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="427b1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="427b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="427b1-126">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="427b1-126">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="427b1-127">Structures de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="427b1-127">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="427b1-128">**\_itinéraire IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="427b1-128">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="427b1-129">**\_itinéraire IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="427b1-129">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





