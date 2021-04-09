---
description: Spécifie le type de processus identifié dans la structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ .
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: Énumération D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111822"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a><span data-ttu-id="b7105-103">D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE, énumération</span><span class="sxs-lookup"><span data-stu-id="b7105-103">D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE enumeration</span></span>

<span data-ttu-id="b7105-104">Spécifie le type de processus identifié dans la structure [**de \_ \_ sortie D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) .</span><span class="sxs-lookup"><span data-stu-id="b7105-104">Specifies the type of process that is identified in the [**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7105-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7105-105">Syntax</span></span>


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a><span data-ttu-id="b7105-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b7105-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b7105-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="b7105-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="b7105-108">Type de processus inconnu.</span><span class="sxs-lookup"><span data-stu-id="b7105-108">Unknown process type.</span></span>

</dd> <dt>

<span data-ttu-id="b7105-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE, \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="b7105-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE\_DWM**</span></span>
</dt> <dd>

<span data-ttu-id="b7105-110">Gestionnaire de fenêtrage (DWM).</span><span class="sxs-lookup"><span data-stu-id="b7105-110">Desktop Window Manager (DWM) process.</span></span>

</dd> <dt>

<span data-ttu-id="b7105-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**\_handle PROCESSIDTYPE**</span><span class="sxs-lookup"><span data-stu-id="b7105-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="b7105-112">Handle vers un processus.</span><span class="sxs-lookup"><span data-stu-id="b7105-112">Handle to a process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7105-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7105-113">Requirements</span></span>



| <span data-ttu-id="b7105-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7105-114">Requirement</span></span> | <span data-ttu-id="b7105-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7105-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7105-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7105-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b7105-117">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7105-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b7105-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7105-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b7105-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7105-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7105-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7105-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7105-121"><dt>D3d9types. h (inclure d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7105-121"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7105-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7105-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7105-123">Énumérations de vidéos Direct3D</span><span class="sxs-lookup"><span data-stu-id="b7105-123">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




