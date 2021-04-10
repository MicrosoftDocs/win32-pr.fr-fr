---
description: Contient un numéro de port utilisé pour les protocoles IP ou IPX.
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: GENERIC_PORT Union (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950971"
---
# <a name="generic_port-union"></a><span data-ttu-id="e163c-103">\_Union de port générique</span><span class="sxs-lookup"><span data-stu-id="e163c-103">GENERIC\_PORT union</span></span>

<span data-ttu-id="e163c-104">La structure du **\_ port générique** contient un numéro de port utilisé pour les protocoles IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="e163c-104">The **GENERIC\_PORT** structure contains a port number used for IP or IPX protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="e163c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e163c-105">Syntax</span></span>


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a><span data-ttu-id="e163c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e163c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e163c-107">**IPPort**</span><span class="sxs-lookup"><span data-stu-id="e163c-107">**IPPort**</span></span>
</dt> <dd>

<span data-ttu-id="e163c-108">Numéro de port IP rempli.</span><span class="sxs-lookup"><span data-stu-id="e163c-108">IP port number filled in.</span></span>

</dd> <dt>

<span data-ttu-id="e163c-109">**ByteSwappedIPXPort**</span><span class="sxs-lookup"><span data-stu-id="e163c-109">**ByteSwappedIPXPort**</span></span>
</dt> <dd>

<span data-ttu-id="e163c-110">Numéro de port IPX rempli.</span><span class="sxs-lookup"><span data-stu-id="e163c-110">IPX port number filled in.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e163c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e163c-111">Requirements</span></span>



| <span data-ttu-id="e163c-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e163c-112">Requirement</span></span> | <span data-ttu-id="e163c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e163c-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e163c-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e163c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e163c-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e163c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e163c-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e163c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e163c-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e163c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e163c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="e163c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e163c-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e163c-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




