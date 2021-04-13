---
description: La structure EXPERTFRAMEDESCRIPTOR contient des informations sur un frame. Lorsque l’expert appelle la fonction ExpertGetFrame avec succès, Moniteur réseau transmet la structure EXPERTFRAMEDESCRIPTOR à l’expert.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: EXPERTFRAMEDESCRIPTOR, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484337"
---
# <a name="expertframedescriptor-structure"></a><span data-ttu-id="44c84-104">EXPERTFRAMEDESCRIPTOR, structure</span><span class="sxs-lookup"><span data-stu-id="44c84-104">EXPERTFRAMEDESCRIPTOR structure</span></span>

<span data-ttu-id="44c84-105">La structure **EXPERTFRAMEDESCRIPTOR** contient des informations sur un frame.</span><span class="sxs-lookup"><span data-stu-id="44c84-105">The **EXPERTFRAMEDESCRIPTOR** structure contains information about a frame.</span></span> <span data-ttu-id="44c84-106">Lorsque l’expert appelle la fonction [**ExpertGetFrame**](expertgetframe.md) avec succès, moniteur réseau transmet la structure **EXPERTFRAMEDESCRIPTOR** à l’expert.</span><span class="sxs-lookup"><span data-stu-id="44c84-106">When the expert calls the [**ExpertGetFrame**](expertgetframe.md) function successfully, Network Monitor passes the **EXPERTFRAMEDESCRIPTOR** structure back to the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="44c84-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44c84-107">Syntax</span></span>


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="44c84-108">Membres</span><span class="sxs-lookup"><span data-stu-id="44c84-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="44c84-109">**FrameNumber**</span><span class="sxs-lookup"><span data-stu-id="44c84-109">**FrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="44c84-110">Numéro d’un cadre spécifié.</span><span class="sxs-lookup"><span data-stu-id="44c84-110">Number of a specified frame.</span></span>

</dd> <dt>

<span data-ttu-id="44c84-111">**hFrame**</span><span class="sxs-lookup"><span data-stu-id="44c84-111">**hFrame**</span></span>
</dt> <dd>

<span data-ttu-id="44c84-112">Handle vers un frame.</span><span class="sxs-lookup"><span data-stu-id="44c84-112">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="44c84-113">**pFrame**</span><span class="sxs-lookup"><span data-stu-id="44c84-113">**pFrame**</span></span>
</dt> <dd>

<span data-ttu-id="44c84-114">Pointeur vers un frame brut.</span><span class="sxs-lookup"><span data-stu-id="44c84-114">Pointer to a raw frame.</span></span>

</dd> <dt>

<span data-ttu-id="44c84-115">**lpRecognizeDataTable**</span><span class="sxs-lookup"><span data-stu-id="44c84-115">**lpRecognizeDataTable**</span></span>
</dt> <dd>

<span data-ttu-id="44c84-116">Table qui indique où chaque analyseur identifie le début des données.</span><span class="sxs-lookup"><span data-stu-id="44c84-116">Table that indicates where each parser identifies the start of the data.</span></span>

</dd> <dt>

<span data-ttu-id="44c84-117">**lpPropertyTable**</span><span class="sxs-lookup"><span data-stu-id="44c84-117">**lpPropertyTable**</span></span>
</dt> <dd>

<span data-ttu-id="44c84-118">Table de propriétés de frame identifiée par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="44c84-118">Table of frame properties that the parser identifies.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44c84-119">Notes</span><span class="sxs-lookup"><span data-stu-id="44c84-119">Remarks</span></span>

<span data-ttu-id="44c84-120">Si l’expert spécifie des \_ propriétés d’attachement de balises \_ lors de l’appel de [**ExpertGetFrame**](expertgetframe.md), le membre **szPropertyText** dans chaque structure [**PROPERTYINST**](propertyinst.md) a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="44c84-120">If the expert specifies FLAGS\_ATTACH\_PROPERTIES when calling [**ExpertGetFrame**](expertgetframe.md), then the **szPropertyText** member in each [**PROPERTYINST**](propertyinst.md) structure is **NULL**.</span></span>

<span data-ttu-id="44c84-121">Si l’expert ne spécifie pas \_ les \_ propriétés d’attachement des indicateurs lors de l’appel de la fonction [**ExpertGetFrame**](expertgetframe.md) , le membre **lpPropertyTable** est **null** au retour.</span><span class="sxs-lookup"><span data-stu-id="44c84-121">If the expert does not specify FLAGS\_ATTACH\_PROPERTIES when calling the [**ExpertGetFrame**](expertgetframe.md) function, then the **lpPropertyTable** member is **NULL** on return.</span></span>

## <a name="requirements"></a><span data-ttu-id="44c84-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44c84-122">Requirements</span></span>



| <span data-ttu-id="44c84-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44c84-123">Requirement</span></span> | <span data-ttu-id="44c84-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="44c84-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="44c84-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44c84-125">Minimum supported client</span></span><br/> | <span data-ttu-id="44c84-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44c84-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="44c84-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44c84-127">Minimum supported server</span></span><br/> | <span data-ttu-id="44c84-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44c84-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="44c84-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="44c84-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="44c84-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="44c84-130"><dt>Netmon.h</dt></span></span> </dl> |



 

 




