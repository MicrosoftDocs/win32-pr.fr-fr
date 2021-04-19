---
description: Un frame réel du pilote.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Structure de FRAMEs (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515409"
---
# <a name="frame-structure"></a><span data-ttu-id="be707-103">Structure de FRAME</span><span class="sxs-lookup"><span data-stu-id="be707-103">FRAME structure</span></span>

<span data-ttu-id="be707-104">La structure du **Frame** est un cadre réel du pilote.</span><span class="sxs-lookup"><span data-stu-id="be707-104">The **FRAME** structure is an actual frame from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="be707-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be707-105">Syntax</span></span>


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a><span data-ttu-id="be707-106">Membres</span><span class="sxs-lookup"><span data-stu-id="be707-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="be707-107">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="be707-107">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="be707-108">Temps écoulé, en microsecondes, entre le début de la capture et le moment où le frame a été capturé.</span><span class="sxs-lookup"><span data-stu-id="be707-108">Elapsed time, in microseconds, between the start of the capture and the time when the frame was captured.</span></span>

</dd> <dt>

<span data-ttu-id="be707-109">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="be707-109">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="be707-110">Longueur du cadre MAC.</span><span class="sxs-lookup"><span data-stu-id="be707-110">MAC frame length.</span></span>

</dd> <dt>

<span data-ttu-id="be707-111">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="be707-111">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="be707-112">Longueur de trame réelle copiée.</span><span class="sxs-lookup"><span data-stu-id="be707-112">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="be707-113">**MacFrame**</span><span class="sxs-lookup"><span data-stu-id="be707-113">**MacFrame**</span></span>
</dt> <dd>

<span data-ttu-id="be707-114">Données de frame.</span><span class="sxs-lookup"><span data-stu-id="be707-114">Frame data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be707-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be707-115">Requirements</span></span>



| <span data-ttu-id="be707-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be707-116">Requirement</span></span> | <span data-ttu-id="be707-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="be707-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="be707-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be707-118">Minimum supported client</span></span><br/> | <span data-ttu-id="be707-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be707-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="be707-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be707-120">Minimum supported server</span></span><br/> | <span data-ttu-id="be707-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be707-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="be707-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="be707-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="be707-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="be707-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




