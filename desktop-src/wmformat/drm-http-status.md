---
title: Énumération DRM_HTTP_STATUS (Drmexternals. h)
description: Le \_ \_ type d’énumération de l’État http DRM définit une plage d’États pour une requête DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- Format Windows Media d’énumération DRM_HTTP_STATUS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512181"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a><span data-ttu-id="17f10-105">Énumération DRM_HTTP_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="17f10-105">DRM_HTTP_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="17f10-106">Le type d’énumération de l' **\_ \_ État http DRM** définit une plage d’États pour une requête [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="17f10-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of states for a [*DRM*](wmformat-glossary.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f10-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17f10-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="17f10-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="17f10-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="17f10-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_NOTINITIATED http**</span><span class="sxs-lookup"><span data-stu-id="17f10-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="17f10-110">Les opérations HTTP n’ont pas été initiées.</span><span class="sxs-lookup"><span data-stu-id="17f10-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="17f10-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_connexion http**</span><span class="sxs-lookup"><span data-stu-id="17f10-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="17f10-112">La connexion est en cours d’établissement.</span><span class="sxs-lookup"><span data-stu-id="17f10-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="17f10-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_demande http**</span><span class="sxs-lookup"><span data-stu-id="17f10-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="17f10-114">Les données sont demandées.</span><span class="sxs-lookup"><span data-stu-id="17f10-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="17f10-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_réception http**</span><span class="sxs-lookup"><span data-stu-id="17f10-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="17f10-116">Les données sont reçues.</span><span class="sxs-lookup"><span data-stu-id="17f10-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="17f10-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="17f10-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="17f10-118">Les opérations HTTP sont terminées.</span><span class="sxs-lookup"><span data-stu-id="17f10-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17f10-119">Notes</span><span class="sxs-lookup"><span data-stu-id="17f10-119">Remarks</span></span>

<span data-ttu-id="17f10-120">Cette énumération est utilisée par la structure d' [**\_ \_ État**](wm-individualize-status.md) de l’énumération WM.</span><span class="sxs-lookup"><span data-stu-id="17f10-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="17f10-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17f10-121">Requirements</span></span>



| <span data-ttu-id="17f10-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17f10-122">Requirement</span></span> | <span data-ttu-id="17f10-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="17f10-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f10-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17f10-124">Minimum supported client</span></span><br/> | <span data-ttu-id="17f10-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17f10-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="17f10-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17f10-126">Minimum supported server</span></span><br/> | <span data-ttu-id="17f10-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17f10-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="17f10-128">Version</span><span class="sxs-lookup"><span data-stu-id="17f10-128">Version</span></span><br/>                  | <span data-ttu-id="17f10-129">SDK Windows Media Format 7 ou versions ultérieures du kit de développement logiciel (SDK)</span><span class="sxs-lookup"><span data-stu-id="17f10-129">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="17f10-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="17f10-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="17f10-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="17f10-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f10-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17f10-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f10-133">**État de l' \_ individualisation DRM \_**</span><span class="sxs-lookup"><span data-stu-id="17f10-133">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drm-individualization-status.md)
</dt> <dt>

[<span data-ttu-id="17f10-134">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="17f10-134">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





