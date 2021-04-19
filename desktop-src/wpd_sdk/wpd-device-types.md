---
description: Le \_ type d' \_ énumération types d’appareils wpd décrit les différents types d’appareils mobiles Windows couramment utilisés pour déterminer la classification de base et l’apparence visuelle d’un appareil portable.
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: Énumération WPD_DEVICE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3e71acf200a95bba05b7298a5824bfa353e4a90b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539497"
---
# <a name="wpd_device_types-enumeration"></a><span data-ttu-id="ee983-103">\_Énumération des types d’appareils wpd \_</span><span class="sxs-lookup"><span data-stu-id="ee983-103">WPD\_DEVICE\_TYPES enumeration</span></span>

<span data-ttu-id="ee983-104">Le type d’énumération **\_ \_ types d’appareils wpd** décrit les différents types d’appareils mobiles Windows couramment utilisés pour déterminer la classification de base et l’apparence visuelle d’un appareil portable.</span><span class="sxs-lookup"><span data-stu-id="ee983-104">The **WPD\_DEVICE\_TYPES** enumeration type describes the different Windows Portable Device (WPD) types commonly used to determine the basic classification and visual appearance of a portable device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee983-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee983-105">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="ee983-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ee983-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ee983-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**\_type d’appareil wpd \_ \_ générique**</span><span class="sxs-lookup"><span data-stu-id="ee983-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD\_DEVICE\_TYPE\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="ee983-108">WPD générique qui comprend des appareils multifonctions qui ne se trouvent pas dans l’un des autres valeurs d’énumération des [**\_ \_ types d’appareils wpd**](wpd-device-types.md) .</span><span class="sxs-lookup"><span data-stu-id="ee983-108">A generic WPD that includes multifunction devices that do not fall into one of the other [**WPD\_DEVICE\_TYPES**](wpd-device-types.md) enumeration values.</span></span>

</dd> <dt>

<span data-ttu-id="ee983-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_caméra de \_ type d’appareil wpd \_**</span><span class="sxs-lookup"><span data-stu-id="ee983-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD\_DEVICE\_TYPE\_CAMERA**</span></span>
</dt> <dd>

<span data-ttu-id="ee983-110">Appareil photo, tel qu’un appareil photo numérique.</span><span class="sxs-lookup"><span data-stu-id="ee983-110">A camera device, such as a digital still camera.</span></span>

</dd> <dt>

<span data-ttu-id="ee983-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_ \_ \_ lecteur multimédia type de périphérique wpd \_**</span><span class="sxs-lookup"><span data-stu-id="ee983-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER**</span></span>
</dt> <dd>

<span data-ttu-id="ee983-112">Périphérique de lecteur multimédia qui prend en charge la lecture audio, vidéo ou l’affichage d’images, telles qu’un lecteur de musique portable ou portable Media Center.</span><span class="sxs-lookup"><span data-stu-id="ee983-112">A media player device that supports playing audio, video, or viewing pictures, such as a portable music player or portable media center.</span></span> <span data-ttu-id="ee983-113">Cette fonctionnalité n’est pas tout à fait classée en tant que \_ lecteur multimédia du type d’appareil wpd \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ee983-113">Not all of this functionally is classified as a WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span> <span data-ttu-id="ee983-114">Par exemple, les appareils portables de musique sont classés en tant que \_ lecteur multimédia du type d’appareil wpd \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ee983-114">For example, portable music player devices are classified as WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span>

</dd> <dt>

<span data-ttu-id="ee983-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**\_type d’appareil wpd \_ \_ Téléphone**</span><span class="sxs-lookup"><span data-stu-id="ee983-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD\_DEVICE\_TYPE\_PHONE**</span></span>
</dt> <dd>

<span data-ttu-id="ee983-116">Un appareil téléphonique, tel qu’un téléphone mobile.</span><span class="sxs-lookup"><span data-stu-id="ee983-116">A phone device, such as a mobile phone.</span></span>

</dd> <dt>

<span data-ttu-id="ee983-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**vidéo sur le \_ type d’appareil wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee983-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**WPD\_DEVICE\_TYPE\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="ee983-118">Périphérique vidéo.</span><span class="sxs-lookup"><span data-stu-id="ee983-118">A video device.</span></span>

</dd> <dt>

<span data-ttu-id="ee983-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**TYPE d’appareil WPD- \_ \_ \_ Gestionnaire d' \_ informations personnelles \_**</span><span class="sxs-lookup"><span data-stu-id="ee983-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD\_DEVICE\_TYPE\_PERSONAL\_INFORMATION\_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="ee983-120">Un périphérique gestionnaire d’informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="ee983-120">A personal information manager device.</span></span>

</dd> <dt>

<span data-ttu-id="ee983-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_ \_ enregistreur audio du type d’appareil wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee983-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD\_DEVICE\_TYPE\_AUDIO\_RECORDER**</span></span>
</dt> <dd>

<span data-ttu-id="ee983-122">Un périphérique d’enregistrement audio.</span><span class="sxs-lookup"><span data-stu-id="ee983-122">An audio recorder device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee983-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ee983-123">Remarks</span></span>

<span data-ttu-id="ee983-124">**Wpd \_ Les \_ types d’appareils** sont lus à l’aide de l’interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="ee983-124">**WPD\_DEVICE\_TYPES** are read using the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span> <span data-ttu-id="ee983-125">Les applications WPD peuvent utiliser ces valeurs pour déterminer l’apparence visuelle générique de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee983-125">WPD applications may use these values to determine the generic visual appearance of the device.</span></span> <span data-ttu-id="ee983-126">Autrement dit, une image de caméra est affichée pour les appareils de type caméra, une image de téléphone mobile s’affiche pour les appareils de type téléphone, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ee983-126">That is, a camera picture is displayed for camera-like devices, a mobile phone picture is displayed for phone-like devices, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="ee983-127">Les applications WPD doivent utiliser les fonctionnalités du périphérique portable pour déterminer de façon fonctionnelle, et non la valeur des **\_ \_ types d’appareils wpd** .</span><span class="sxs-lookup"><span data-stu-id="ee983-127">WPD applications must use the capabilities of the portable device to determine functionally, not the **WPD\_DEVICE\_TYPES** value.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee983-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee983-128">Requirements</span></span>



| <span data-ttu-id="ee983-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee983-129">Requirement</span></span> | <span data-ttu-id="ee983-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee983-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee983-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee983-131">Header</span></span><br/> | <dl> <span data-ttu-id="ee983-132"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee983-132"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee983-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee983-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee983-134">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="ee983-134">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




