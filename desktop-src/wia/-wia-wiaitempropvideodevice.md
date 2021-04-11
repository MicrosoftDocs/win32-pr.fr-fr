---
description: Le pilote vidéo d’acquisition d’images Windows (WIA) standard (wiavusd.dll) prend en charge les propriétés suivantes pour la diffusion en continu de périphériques vidéo.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Constantes de propriété d’appareil vidéo WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPV_LAST_PICTURE_TAKEN
- WIA_DPV_IMAGES_DIRECTORY
- WIA_DPV_DSHOW_DEVICE_PATH
- WIA_DPF_MOUNT_POINT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f02991cb5c2b8cc15eb89e335ef1e46442c89510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113259"
---
# <a name="video-wia-device-property-constants"></a>Constantes de propriété d’appareil vidéo WIA

Le pilote vidéo d’acquisition d’images Windows (WIA) standard (wiavusd.dll) prend en charge les propriétés suivantes pour la diffusion en continu de périphériques vidéo.

> [!Note]  
> WIA ne prend pas en charge les périphériques vidéo dans Windows Server 2003, Windows Vista ou version ultérieure. Pour ces versions de Windows, utilisez [DirectShow](/previous-versions//ms783323(v=vs.85)) pour acquérir des images à partir d’une vidéo.

 

Le préfixe « WIA \_ DPV \_ » indique une propriété d’appareil pour les périphériques vidéo et est la Convention d’affectation de noms utilisée dans C/C++. À des fins de script, ces constantes utilisent le préfixe « VideoDevice » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.



| Constante/valeur                                                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_ \_Dernière \_ image \_**</dt> de la DPV <dt>VideoDeviceLastPictureTaken</dt> </dl> | Cette propriété est utilisée pour informer le pilote WIA qu’une nouvelle image a été ajoutée. Les applications doivent définir la valeur de cette propriété sur le nom du fichier image créé à la suite d’un appel réussi à la méthode [**IWiaVideo :: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) . <br/> Type : VT \_ BSTR, Access : lecture/écriture<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_ \_ \_ Répertoire d’images de DPV**</dt> <dt>VideoDeviceImagesDirectory</dt> </dl>         | Cette propriété est exposée par le pilote en mode utilisateur vidéo WIA standard (wiavusd.dll). La valeur de cette propriété est le chemin d’accès complet du répertoire dans lequel le pilote vidéo WIA place les images par défaut. Les applications doivent définir la propriété [**IWiaVideo :: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) sur cette valeur. <br/> Type : VT \_ BSTR, Access : lecture seule<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_ \_ \_ \_ Chemin de l’appareil DPV DShow**</dt> <dt>VideoDeviceDShowDevicePath</dt> </dl>     | Chemin d’accès complet de l’appareil DirectShow. <br/> Type : VT \_ BSTR, Access : lecture seule<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_ \_ \_ Point de montage DPF**</dt> <dt>FileDeviceMountPoint</dt> </dl>                              | Non implémenté. <br/> Type : **VT \_ I4**, accès : lecture seule, valeurs valides : [WIA \_ prop \_ None](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
