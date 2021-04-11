---
title: Énumération MP_FASTPATH_TYPE (MpClient. h)
description: Type de FastPath.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMP_FASTPATH_TYPE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89db79c54b166a833369ff52e47473463e0a2b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105778"
---
# <a name="mp_fastpath_type-enumeration"></a><span data-ttu-id="15362-105">\_ \_ Énumération de type FASTPATH MP</span><span class="sxs-lookup"><span data-stu-id="15362-105">MP\_FASTPATH\_TYPE enumeration</span></span>

<span data-ttu-id="15362-106">Type de FastPath.</span><span class="sxs-lookup"><span data-stu-id="15362-106">FastPath type.</span></span>

## <a name="syntax"></a><span data-ttu-id="15362-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15362-107">Syntax</span></span>


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="15362-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="15362-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="15362-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**FASTPATH de point de gestion \_ \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="15362-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP\_FASTPATH\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="15362-110">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="15362-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="15362-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**\_ \_ machine virtuelle FASTPATH MP**</span><span class="sxs-lookup"><span data-stu-id="15362-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP\_FASTPATH\_VDM**</span></span>
</dt> <dd>

<span data-ttu-id="15362-112">Mise à jour de VDM.</span><span class="sxs-lookup"><span data-stu-id="15362-112">VDM update.</span></span>

</dd> <dt>

<span data-ttu-id="15362-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**\_FASTPATH MP \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="15362-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP\_FASTPATH\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="15362-114">Notification de désactivation de signature.</span><span class="sxs-lookup"><span data-stu-id="15362-114">Signature disable notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15362-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15362-115">Requirements</span></span>



| <span data-ttu-id="15362-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15362-116">Requirement</span></span> | <span data-ttu-id="15362-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="15362-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15362-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15362-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15362-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15362-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="15362-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15362-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15362-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15362-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15362-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="15362-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="15362-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="15362-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





