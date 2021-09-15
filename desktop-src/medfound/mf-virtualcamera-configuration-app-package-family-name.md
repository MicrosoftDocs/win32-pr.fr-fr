---
description: Spécifie le nom de la famille de packages d’application pour une application de configuration de caméra virtuelle.
title: Attribut MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME (Mfapi. h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523604"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a>\_Attribut de \_ \_ nom de famille de package d’application VIRTUALCAMERA \_ MF \_

Spécifie le nom de la famille de packages d’application pour une application de configuration de caméra virtuelle. lorsqu’il est fourni, le pipeline associe l’application de configuration à la caméra virtuelle et fournit un point de lancement dans la page de Paramètres de l’appareil photo.

## <a name="data-type"></a>Type de données

[MF_ATTRIBUTE_STRING](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a>Notes

Cet attribut peut être exposé par la source de média personnalisée de la caméra virtuelle à partir du magasin d’attributs sources du média [IMFMediaSourceEx :: GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).  

Si l’application de configuration n’est pas encore installée sur l’ordinateur, l’application du Windows Store est lancée et naviguée vers la page d’application spécifiée par le nom de la famille de packages. Dans le cas contraire, l’application installée sera lancée pour l’utilisateur.


## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Build 22000<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Build 22000<br/>                      |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes :: SetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




