---
description: La structure HANDOFFENTRY définit une entrée de protocole spécifique dans une structure HANDOFFTABLE.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: HANDOFFENTRY, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525126"
---
# <a name="handoffentry-structure"></a><span data-ttu-id="cf185-103">HANDOFFENTRY, structure</span><span class="sxs-lookup"><span data-stu-id="cf185-103">HANDOFFENTRY structure</span></span>

<span data-ttu-id="cf185-104">La structure **HANDOFFENTRY** définit une entrée de protocole spécifique dans une structure **HANDOFFTABLE** .</span><span class="sxs-lookup"><span data-stu-id="cf185-104">The **HANDOFFENTRY** structure defines a specific protocol entry in a **HANDOFFTABLE** structure.</span></span>

<span data-ttu-id="cf185-105">Cette structure est renseignée par Moniteur réseau en fonction des informations contenues dans un fichier. ini fourni par l’utilisateur fourni lors de l’appel de la fonction [**CreateHandoffTable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="cf185-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span> <span data-ttu-id="cf185-106">Cette structure ne doit jamais être modifiée explicitement par une application.</span><span class="sxs-lookup"><span data-stu-id="cf185-106">This structure should never be explicitly modified by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf185-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf185-107">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="cf185-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cf185-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cf185-109">**visionnant \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="cf185-109">**hoe\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="cf185-110">Signature qui identifie cette entrée en tant qu’entrée de table de remise.</span><span class="sxs-lookup"><span data-stu-id="cf185-110">Signature that identifies this entry as a handoff table entry.</span></span>

</dd> <dt>

<span data-ttu-id="cf185-111">**visionnant \_ ProtIdentNumber**</span><span class="sxs-lookup"><span data-stu-id="cf185-111">**hoe\_ProtIdentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="cf185-112">Numéro de protocole fourni par le fichier. ini fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf185-112">Protocol number provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="cf185-113">**visionnant \_ ProtocolHandle**</span><span class="sxs-lookup"><span data-stu-id="cf185-113">**hoe\_ProtocolHandle**</span></span>
</dt> <dd>

<span data-ttu-id="cf185-114">Handle de protocole créé à l’aide du nom de protocole fourni par le fichier. ini fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf185-114">Handle of protocol created using the protocol name provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="cf185-115">**visionnant \_ ProtocolData**</span><span class="sxs-lookup"><span data-stu-id="cf185-115">**hoe\_ProtocolData**</span></span>
</dt> <dd>

<span data-ttu-id="cf185-116">Données d’instance de protocole fournies par le fichier. ini fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf185-116">Protocol instance data provided by user supplied .ini file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf185-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cf185-117">Remarks</span></span>

<span data-ttu-id="cf185-118">Cette structure est renseignée par Moniteur réseau lorsque Moniteur réseau crée une table de remise.</span><span class="sxs-lookup"><span data-stu-id="cf185-118">This structure is filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf185-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf185-119">Requirements</span></span>



| <span data-ttu-id="cf185-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf185-120">Requirement</span></span> | <span data-ttu-id="cf185-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf185-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cf185-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf185-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cf185-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf185-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cf185-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf185-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cf185-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf185-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cf185-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf185-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf185-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf185-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf185-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf185-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf185-129">HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="cf185-129">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




