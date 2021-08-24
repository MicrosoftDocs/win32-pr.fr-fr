---
description: Désactive l’utilisation des plug-ins de la caméra de l’après-traitement par le lecteur source.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: Attribut MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66ae9c69d13b6af3e368b57a3f864f031d0cc7e63716d2267ae5d3869d102b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600289"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a>\_ \_ \_ Attribut plug-ins de désactivation de l' \_ appareil source \_ MF

Désactive l’utilisation des plug-ins de la caméra de l’après-traitement par le [lecteur source](source-reader.md).

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique lorsque le lecteur source est utilisé avec une source de capture vidéo. Si cet attribut a la **valeur true**, il empêche le lecteur source de charger les plug-ins de publication que l’appareil photo peut fournir. Dans le cas contraire, le lecteur source les chargera par défaut.

La valeur par défaut de cet attribut est **false**. Définissez l’attribut lorsque vous créez le lecteur source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du lecteur source](source-reader-attributes.md)
</dt> </dl>

 

 




