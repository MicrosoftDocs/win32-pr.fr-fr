---
description: Indique l’état actuel d’un expert en cours d’exécution.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: EXPERTSTATUS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525156"
---
# <a name="expertstatus-structure"></a><span data-ttu-id="e3af0-103">EXPERTSTATUS, structure</span><span class="sxs-lookup"><span data-stu-id="e3af0-103">EXPERTSTATUS structure</span></span>

<span data-ttu-id="e3af0-104">La structure **EXPERTSTATUS** indique l’état actuel d’un expert en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e3af0-104">The **EXPERTSTATUS** structure indicates the current status of a running expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3af0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3af0-105">Syntax</span></span>


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a><span data-ttu-id="e3af0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e3af0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3af0-107">**État**</span><span class="sxs-lookup"><span data-stu-id="e3af0-107">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="e3af0-108">Valeur actuelle de l’État expert définie par l’énumération [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="e3af0-108">Current expert status value defined by the [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e3af0-109">**Sous-état**</span><span class="sxs-lookup"><span data-stu-id="e3af0-109">**SubStatus**</span></span>
</dt> <dd>

<span data-ttu-id="e3af0-110">Valeur du sous-état.</span><span class="sxs-lookup"><span data-stu-id="e3af0-110">Sub-status value.</span></span>

</dd> <dt>

<span data-ttu-id="e3af0-111">**PercentDone**</span><span class="sxs-lookup"><span data-stu-id="e3af0-111">**PercentDone**</span></span>
</dt> <dd>

<span data-ttu-id="e3af0-112">Pourcentage d’achèvement de l’analyse d’experts des données réseau.</span><span class="sxs-lookup"><span data-stu-id="e3af0-112">Percentage completion of the expert analysis of network data.</span></span>

</dd> <dt>

<span data-ttu-id="e3af0-113">**Frame**</span><span class="sxs-lookup"><span data-stu-id="e3af0-113">**Frame**</span></span>
</dt> <dd>

<span data-ttu-id="e3af0-114">Numéro de frame.</span><span class="sxs-lookup"><span data-stu-id="e3af0-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="e3af0-115">**szStatusText**</span><span class="sxs-lookup"><span data-stu-id="e3af0-115">**szStatusText**</span></span>
</dt> <dd>

<span data-ttu-id="e3af0-116">Texte qui décrit l’état de l’expert.</span><span class="sxs-lookup"><span data-stu-id="e3af0-116">Text that describes the expert status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3af0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3af0-117">Requirements</span></span>



| <span data-ttu-id="e3af0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3af0-118">Requirement</span></span> | <span data-ttu-id="e3af0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3af0-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e3af0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3af0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3af0-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3af0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e3af0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3af0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3af0-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3af0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e3af0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3af0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3af0-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3af0-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




