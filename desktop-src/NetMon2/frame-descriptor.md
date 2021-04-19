---
description: La \_ structure du descripteur de Frame fournit des informations descriptives sur les frames bruts.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Structure de FRAME_DESCRIPTOR (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513355"
---
# <a name="frame_descriptor-structure"></a><span data-ttu-id="dbcd1-103">\_Structure du descripteur de frame</span><span class="sxs-lookup"><span data-stu-id="dbcd1-103">FRAME\_DESCRIPTOR structure</span></span>

<span data-ttu-id="dbcd1-104">La structure du **\_ descripteur de frame** fournit des informations descriptives sur les frames bruts.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-104">The **FRAME\_DESCRIPTOR** structure provides descriptive information about raw frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbcd1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbcd1-105">Syntax</span></span>


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="dbcd1-106">Membres</span><span class="sxs-lookup"><span data-stu-id="dbcd1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dbcd1-107">**FramePointer**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-107">**FramePointer**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-108">Pointeur vers les données de frame.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-108">Pointer to frame data.</span></span>

</dd> <dt>

<span data-ttu-id="dbcd1-109">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-109">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-110">Heure système, en microsecondes, à laquelle le frame a été capturé.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-110">System time, in microseconds, when the frame was captured.</span></span> <span data-ttu-id="dbcd1-111">Cette durée est généralement utilisée pour déterminer l’intervalle entre les deux frames capturés.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-111">This time is typically used to determine the interval between the times two frames were captured.</span></span>

</dd> <dt>

<span data-ttu-id="dbcd1-112">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-112">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-113">Longueur du frame.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-113">Length of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="dbcd1-114">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-114">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-115">Longueur de trame réelle copiée.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-115">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="dbcd1-116">**ETYPE**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-116">**Etype**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-117">Nom ETYPE.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-117">Etype name.</span></span>

</dd> <dt>

<span data-ttu-id="dbcd1-118">**SAP**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-118">**Sap**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-119">Valeur SAP.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-119">SAP value.</span></span>

</dd> <dt>

<span data-ttu-id="dbcd1-120">**LowProtocol**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-120">**LowProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-121">Index du protocole trouvé.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-121">Index of protocol found.</span></span>

</dd> <dt>

<span data-ttu-id="dbcd1-122">**LowProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-122">**LowProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-123">Décalage des données de protocole obtenues à partir de **LowProtocol**.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-123">Offset to protocol data obtained from **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="dbcd1-124">**HighPort**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-124">**HighPort**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-125">Port de protocole élevé identifié dans **LowProtocol**.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-125">Port of high protocol identified in **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="dbcd1-126">**HighProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="dbcd1-126">**HighProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="dbcd1-127">Décalage des données de protocole obtenues à partir de **HighPort**.</span><span class="sxs-lookup"><span data-stu-id="dbcd1-127">Offset to protocol data obtained from **HighPort**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbcd1-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbcd1-128">Requirements</span></span>



| <span data-ttu-id="dbcd1-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbcd1-129">Requirement</span></span> | <span data-ttu-id="dbcd1-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbcd1-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dbcd1-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbcd1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dbcd1-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbcd1-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dbcd1-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbcd1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dbcd1-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbcd1-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dbcd1-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbcd1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbcd1-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbcd1-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




