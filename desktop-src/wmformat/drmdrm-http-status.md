---
title: Énumération DRM_HTTP_STATUS (wmdrmsdk. h)
description: Le \_ \_ type d’énumération de l’État http DRM définit une plage d’États http pour une requête DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- Format Windows Media d’énumération DRM_HTTP_STATUS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537847"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="cac1b-105">Énumération DRM_HTTP_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="cac1b-105">DRM_HTTP_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="cac1b-106">Le type d’énumération de l' **\_ \_ État http DRM** définit une plage d’États http pour une requête DRM.</span><span class="sxs-lookup"><span data-stu-id="cac1b-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of HTTP states for a DRM request.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac1b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cac1b-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="cac1b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="cac1b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cac1b-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_NOTINITIATED http**</span><span class="sxs-lookup"><span data-stu-id="cac1b-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="cac1b-110">Les opérations HTTP n’ont pas été initiées.</span><span class="sxs-lookup"><span data-stu-id="cac1b-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="cac1b-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_connexion http**</span><span class="sxs-lookup"><span data-stu-id="cac1b-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="cac1b-112">La connexion est en cours d’établissement.</span><span class="sxs-lookup"><span data-stu-id="cac1b-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="cac1b-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_demande http**</span><span class="sxs-lookup"><span data-stu-id="cac1b-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="cac1b-114">Les données sont demandées.</span><span class="sxs-lookup"><span data-stu-id="cac1b-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="cac1b-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_réception http**</span><span class="sxs-lookup"><span data-stu-id="cac1b-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="cac1b-116">Les données sont reçues.</span><span class="sxs-lookup"><span data-stu-id="cac1b-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="cac1b-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="cac1b-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="cac1b-118">Les opérations HTTP sont terminées.</span><span class="sxs-lookup"><span data-stu-id="cac1b-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cac1b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="cac1b-119">Remarks</span></span>

<span data-ttu-id="cac1b-120">Cette énumération est utilisée par la structure d' [**\_ \_ État**](drmwm-individualize-status.md) de l’énumération WM.</span><span class="sxs-lookup"><span data-stu-id="cac1b-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac1b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cac1b-121">Requirements</span></span>



| <span data-ttu-id="cac1b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cac1b-122">Requirement</span></span> | <span data-ttu-id="cac1b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cac1b-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cac1b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cac1b-124">Header</span></span><br/> | <dl> <span data-ttu-id="cac1b-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac1b-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac1b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cac1b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac1b-127">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="cac1b-127">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





