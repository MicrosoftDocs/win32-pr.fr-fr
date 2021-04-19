---
description: Représente des informations sur les cibles d’appel pour la protection du workflow de contrôle (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: Structure CFG_CALL_TARGET_INFO (Ntmmapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518242"
---
# <a name="cfg_call_target_info-structure"></a><span data-ttu-id="8493a-103">Structure des informations de la \_ cible de l’appel de cfg \_ \_</span><span class="sxs-lookup"><span data-stu-id="8493a-103">CFG\_CALL\_TARGET\_INFO structure</span></span>

<span data-ttu-id="8493a-104">Représente des informations sur les cibles d’appel pour la protection du workflow de contrôle (CFG).</span><span class="sxs-lookup"><span data-stu-id="8493a-104">Represents information about call targets for Control Flow Guard (CFG).</span></span>

## <a name="syntax"></a><span data-ttu-id="8493a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8493a-105">Syntax</span></span>


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="8493a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8493a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8493a-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="8493a-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="8493a-108">Décalage par rapport à une adresse virtuelle (de début) fournie.</span><span class="sxs-lookup"><span data-stu-id="8493a-108">Offset relative to a provided (start) virtual address.</span></span> <span data-ttu-id="8493a-109">Ce décalage doit être aligné sur 16 octets.</span><span class="sxs-lookup"><span data-stu-id="8493a-109">This offset should be 16 byte aligned.</span></span>

</dd> <dt>

<span data-ttu-id="8493a-110">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="8493a-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="8493a-111">Indicateurs décrivant l’opération à effectuer sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="8493a-111">Flags describing the operation to be performed on the address.</span></span> <span data-ttu-id="8493a-112">Si **la \_ cible d’appel cfg \_ \_ valide** est définie, l’adresse est marquée comme valide pour cfg.</span><span class="sxs-lookup"><span data-stu-id="8493a-112">If **CFG\_CALL\_TARGET\_VALID** is set, then the address will be marked valid for CFG.</span></span> <span data-ttu-id="8493a-113">Dans le cas contraire, elle sera marquée comme une cible d’appel non valide.</span><span class="sxs-lookup"><span data-stu-id="8493a-113">Otherwise, it will be marked an invalid call target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8493a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8493a-114">Requirements</span></span>



| <span data-ttu-id="8493a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8493a-115">Requirement</span></span> | <span data-ttu-id="8493a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8493a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8493a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8493a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8493a-118">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8493a-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8493a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8493a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8493a-120">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8493a-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8493a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8493a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8493a-122"><dt>Ntmmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8493a-122"><dt>Ntmmapi.h</dt></span></span> </dl> |



 

 




