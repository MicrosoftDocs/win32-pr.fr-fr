---
description: le \_ type d' \_ énumération TYPES d’appareils wpd décrit les différents TYPES d’appareils mobiles (wpd) Windows couramment utilisés pour déterminer la classification de base et l’apparence visuelle d’un appareil portable.
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
ms.openlocfilehash: 747c4631bc2c24a6550904e36e58a6fc02547bc010da7fa1d08b896c6c17489c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657459"
---
# <a name="wpd_device_types-enumeration"></a>\_Énumération des types d’appareils wpd \_

le type d’énumération **\_ \_ TYPES d’appareils wpd** décrit les différents TYPES d’appareils mobiles (wpd) Windows couramment utilisés pour déterminer la classification de base et l’apparence visuelle d’un appareil portable.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**\_type d’appareil wpd \_ \_ générique**
</dt> <dd>

WPD générique qui comprend des appareils multifonctions qui ne se trouvent pas dans l’un des autres valeurs d’énumération des [**\_ \_ types d’appareils wpd**](wpd-device-types.md) .

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_caméra de \_ type d’appareil wpd \_**
</dt> <dd>

Appareil photo, tel qu’un appareil photo numérique.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_ \_ \_ lecteur multimédia type de périphérique wpd \_**
</dt> <dd>

Périphérique de lecteur multimédia qui prend en charge la lecture audio, vidéo ou l’affichage d’images, telles qu’un lecteur de musique portable ou portable Media Center. Cette fonctionnalité n’est pas tout à fait classée en tant que \_ lecteur multimédia du type d’appareil wpd \_ \_ \_ . Par exemple, les appareils portables de musique sont classés en tant que \_ lecteur multimédia du type d’appareil wpd \_ \_ \_ .

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**\_type d’appareil wpd \_ \_ Téléphone**
</dt> <dd>

Un appareil téléphonique, tel qu’un téléphone mobile.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**vidéo sur le \_ type d’appareil wpd \_ \_**
</dt> <dd>

Périphérique vidéo.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**TYPE d’appareil WPD- \_ \_ \_ Gestionnaire d' \_ informations personnelles \_**
</dt> <dd>

Un périphérique gestionnaire d’informations personnelles.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_ \_ enregistreur audio du type d’appareil wpd \_ \_**
</dt> <dd>

Un périphérique d’enregistrement audio.

</dd> </dl>

## <a name="remarks"></a>Remarques

**Wpd \_ Les \_ types d’appareils** sont lus à l’aide de l’interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) . Les applications WPD peuvent utiliser ces valeurs pour déterminer l’apparence visuelle générique de l’appareil. Autrement dit, une image de caméra est affichée pour les appareils de type caméra, une image de téléphone mobile s’affiche pour les appareils de type téléphone, et ainsi de suite.

> [!Note]  
> Les applications WPD doivent utiliser les fonctionnalités du périphérique portable pour déterminer de façon fonctionnelle, et non la valeur des **\_ \_ types d’appareils wpd** .

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




