---
title: Structure WINBIO_EXTENDED_SENSOR_INFO ( \_ types WINBIO. h)
description: Contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_SENSOR_INFO
- API du pointeur de structure PWINBIO_EXTENDED_SENSOR_INFO Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd8c323b4f4e3847c399e314da22048f658fb68c3b07ecf82f71ce0ed327c368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910417"
---
# <a name="winbio_extended_sensor_info-structure"></a>\_Structure d' \_ informations de capteur étendue WINBIO \_

Contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**GenericSensorCapabilities**
</dt> <dd>

Les fonctionnalités génériques du composant de capteur qui est connecté à une unité biométrique spécifique.

</dd> <dt>

**Facteur**
</dt> <dd>

Type d’unité biométrique pour lequel cette structure contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur. Par exemple, si la valeur du membre **Factor** est **WINBIO \_ type \_ empreinte**, la structure d’informations sur le **\_ \_ capteur \_ étendu WINBIO** s’applique à un lecteur d’empreintes digitales et contient les informations pertinentes dans la structure **spécifique. Fingerprint** .

</dd> <dt>

**Plus**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée à un facteur biométrique spécifique.

<dl> <dt>

**Null**
</dt> <dd>

Réservé. Doit être zéro.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée aux caractéristiques du visage.

<dl> <dt>

**Trame**
</dt> <dd>

Taille du cadre de l’appareil photo, indiquée sous la forme d’une longueur et d’une largeur en pixels par les membres à **droite** et en **bas** de la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) . Le point (0,0) représente l’angle supérieur gauche du frame.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Décalage du cadre de l’appareil photo de la caméra vidéo, en pixels. La valeur (0, 0) indique que le cadre de l’appareil photo pour la face et la caméra vidéo se chevauchent complètement.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientation par défaut de l’appareil photo.

</dd> </dl> </dd> <dt>

**Empreinte digitale**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée aux modèles d’empreintes digitales.

<dl> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> </dl> </dd> <dt>

**IRI**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée aux modèles d’IRIS.

<dl> <dt>

**Trame**
</dt> <dd>

Taille du cadre de l’appareil photo, indiquée sous la forme d’une longueur et d’une largeur en pixels par les membres à **droite** et en **bas** de la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) . Le point (0,0) représente l’angle supérieur gauche du frame.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Décalage, en pixels, du cadre de l’appareil photo pour le diaphragme à partir de la caméra vidéo. La valeur (0, 0) indique que le cadre de l’appareil photo pour le diaphragme et la caméra vidéo se chevauchent complètement.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientation par défaut de l’appareil photo.

</dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de capteur pour une unité biométrique liée aux modèles vocaux.

<dl> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Constantes de capacité WINBIO**](winbio-capability-constants.md)
</dt> <dt>

[**\_Constantes de type de biométrie WINBIO \_**](winbio-biometric-type-constants.md)
</dt> <dt>

[**\_Constantes d’orientation WINBIO**](winbio-orientation-constants.md)
</dt> </dl>

 

