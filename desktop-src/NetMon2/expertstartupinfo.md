---
description: Contient des données qui décrivent un expert lorsqu’il démarre.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: EXPERTSTARTUPINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950975"
---
# <a name="expertstartupinfo-structure"></a><span data-ttu-id="4897f-103">EXPERTSTARTUPINFO, structure</span><span class="sxs-lookup"><span data-stu-id="4897f-103">EXPERTSTARTUPINFO structure</span></span>

<span data-ttu-id="4897f-104">La structure **EXPERTSTARTUPINFO** contient des données qui décrivent un expert lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="4897f-104">The **EXPERTSTARTUPINFO** structure contains data that describes an expert when it starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="4897f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4897f-105">Syntax</span></span>


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a><span data-ttu-id="4897f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4897f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4897f-107">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="4897f-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4897f-108">Indicateurs qui décrivent l’expert.</span><span class="sxs-lookup"><span data-stu-id="4897f-108">Flags that describe the expert.</span></span>

</dd> <dt>

<span data-ttu-id="4897f-109">**hCapture**</span><span class="sxs-lookup"><span data-stu-id="4897f-109">**hCapture**</span></span>
</dt> <dd>

<span data-ttu-id="4897f-110">Handle vers une capture.</span><span class="sxs-lookup"><span data-stu-id="4897f-110">Handle to a capture.</span></span>

</dd> <dt>

<span data-ttu-id="4897f-111">**szCaptureFile**</span><span class="sxs-lookup"><span data-stu-id="4897f-111">**szCaptureFile**</span></span>
</dt> <dd>

<span data-ttu-id="4897f-112">Nom du fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="4897f-112">Name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="4897f-113">**dwFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="4897f-113">**dwFrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="4897f-114">Numéro de frame.</span><span class="sxs-lookup"><span data-stu-id="4897f-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="4897f-115">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="4897f-115">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="4897f-116">Handle du protocole.</span><span class="sxs-lookup"><span data-stu-id="4897f-116">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="4897f-117">**lpPropertyInst**</span><span class="sxs-lookup"><span data-stu-id="4897f-117">**lpPropertyInst**</span></span>
</dt> <dd>

<span data-ttu-id="4897f-118">Pointeur vers une structure [**PROPERTYINST**](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="4897f-118">Pointer to a [**PROPERTYINST**](propertyinst.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4897f-119">**sBitfield**</span><span class="sxs-lookup"><span data-stu-id="4897f-119">**sBitfield**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4897f-120">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="4897f-120">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="4897f-121">Utilisé uniquement si le membre **DataQualifier** de la structure [**PROPERTYINST**](propertyinst.md) est défini sur Prop \_ Qualys \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="4897f-121">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="4897f-122">**Ble**</span><span class="sxs-lookup"><span data-stu-id="4897f-122">**bOn**</span></span>
</dt> <dd>

<span data-ttu-id="4897f-123">Utilisé uniquement si le membre **DataQualifier** de la structure [**PROPERTYINST**](propertyinst.md) est défini sur Prop \_ Qualys \_ Flags.</span><span class="sxs-lookup"><span data-stu-id="4897f-123">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4897f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4897f-124">Requirements</span></span>



| <span data-ttu-id="4897f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4897f-125">Requirement</span></span> | <span data-ttu-id="4897f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4897f-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4897f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4897f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4897f-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4897f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4897f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4897f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4897f-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4897f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4897f-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="4897f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4897f-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4897f-132"><dt>Netmon.h</dt></span></span> </dl> |



 

 




