---
title: Énumération WMDMMessage
description: Le type d’énumération WMDMMessage définit les types de messages et les États.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Gestionnaire de périphériques Windows Media WMDMMessage, énumération
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523893"
---
# <a name="wmdmmessage-enumeration"></a><span data-ttu-id="4dacc-104">Énumération WMDMMessage</span><span class="sxs-lookup"><span data-stu-id="4dacc-104">WMDMMessage enumeration</span></span>

<span data-ttu-id="4dacc-105">Le type d’énumération **WMDMMessage** définit les types de messages et les États.</span><span class="sxs-lookup"><span data-stu-id="4dacc-105">The **WMDMMessage** enumeration type defines message types and states.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dacc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4dacc-106">Syntax</span></span>


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a><span data-ttu-id="4dacc-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="4dacc-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4dacc-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**arrivée de l' \_ appareil WMDM MSG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4dacc-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM\_MSG\_DEVICE\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="4dacc-109">Un appareil Windows Media Gestionnaire de périphériques a été branché.</span><span class="sxs-lookup"><span data-stu-id="4dacc-109">A Windows Media Device Manager device has been plugged in.</span></span>

</dd> <dt>

<span data-ttu-id="4dacc-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**suppression de l' \_ appareil WMDM MSG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4dacc-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM\_MSG\_DEVICE\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="4dacc-111">Un appareil Windows Media Gestionnaire de périphériques a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="4dacc-111">A Windows Media Device Manager device has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="4dacc-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_arrivée du \_ support \_ MSG WMDM**</span><span class="sxs-lookup"><span data-stu-id="4dacc-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM\_MSG\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="4dacc-113">Le média a été inséré sur un appareil Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="4dacc-113">Media has been inserted in a Windows Media Device Manager device.</span></span>

</dd> <dt>

<span data-ttu-id="4dacc-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**\_suppression du \_ support \_ MSG WMDM**</span><span class="sxs-lookup"><span data-stu-id="4dacc-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM\_MSG\_MEDIA\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="4dacc-115">Le média a été supprimé d’un appareil Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="4dacc-115">Media has been removed from a Windows Media Device Manager device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4dacc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4dacc-116">Requirements</span></span>



| <span data-ttu-id="4dacc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4dacc-117">Requirement</span></span> | <span data-ttu-id="4dacc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4dacc-118">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4dacc-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4dacc-119">Header</span></span><br/> | <dl> <span data-ttu-id="4dacc-120"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4dacc-120"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dacc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dacc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dacc-122">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="4dacc-122">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





