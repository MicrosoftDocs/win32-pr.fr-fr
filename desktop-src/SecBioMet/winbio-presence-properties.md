---
title: WINBIO_PRESENCE_PROPERTIES Union ( \_ types WINBIO. h)
description: Contient des valeurs biométriques que le Windows Biometric Framework utilisé pour déterminer qu’un individu était présent.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- API Windows Biometric Framework WINBIO_PRESENCE_PROPERTIES Union
- API Windows Biometric Framework du pointeur d’Union PWINBIO_PRESENCE_PROPERTIES
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464606"
---
# <a name="winbio_presence_properties-union"></a>WINBIO \_ Propriétés de présence de l' \_ Union

Contient des valeurs biométriques que le Windows Biometric Framework utilisé pour déterminer qu’un individu était présent.

## <a name="syntax"></a>Syntaxe


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a>Membres

<dl> <dt>

**FacialFeatures**
</dt> <dd>

Valeurs pour l’emplacement des caractéristiques du visage que le Windows Biometric Framework utilisé pour déterminer qu’un individu était présent.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Position dans le cadre de l’appareil photo de la personne, en pixels. La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position. Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** . Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.

</dd> <dt>

**Distance**
</dt> <dd>

Distance entre l’emplacement réel de la face et la distance focale idéale pour la face. Cette valeur est comprise entre-100 et 100. 0 indique la distance idéale, les valeurs positives indiquent que l’emplacement réel du visage est trop éloigné, et les valeurs négatives indiquent que l’emplacement réel est trop proche.

</dd> </dl> </dd> <dt>

**IRI**
</dt> <dd>

Valeurs de l’emplacement de l’IRIS que le Windows Biometric Framework utilisé pour déterminer qu’un individu était présent.

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

Position dans le cadre de l’appareil photo de l’un des Irises de l’individu à inscrire, en pixels. Si le système de reconnaissance de l’iris n’analyse qu’un œil, cette position est du diaphragme de cet oeil. Si le système de reconnaissance de l’iris surveille les deux yeux, mais qu’un seul œil est dans le cadre de l’appareil photo, cette position est du diaphragme de l’oeil dans le cadre de l’appareil photo. Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est probablement celle du diaphragme de l’œil droit de l’individu.

La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position. Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** . Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

Position dans le cadre de l’appareil photo de l’un des Irises de l’individu à inscrire, en pixels. Si le système de reconnaissance de l’iris n’analyse qu’un œil, ou si un seul œil est présent dans le cadre de l’appareil photo, cette valeur est vide. Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est probablement du diaphragme de l’œil gauche de la personne.

La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position. Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** . Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.

</dd> <dt>

**PupilCenter \_ 1**
</dt> <dd>

Position du centre de l’une des pupilles de la personne à inscrire. Si le système de reconnaissance de l’iris n’analyse qu’un œil, cette position est au centre de l’élève de cet oeil. Si le système de reconnaissance de l’iris surveille les yeux, mais qu’un seul œil est dans le cadre de l’appareil photo, cette position est au centre de l’élève de l’oeil dans le cadre de l’appareil photo. Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est sans doute le centre de la pupille du droit de l’individu.

</dd> <dt>

**PupilCenter \_ 2**
</dt> <dd>

Position du centre de l’une des pupilles de la personne à inscrire. Si le système de reconnaissance de l’iris n’analyse qu’un œil, ou si un seul œil est présent dans le cadre de l’appareil photo, cette valeur est vide. Si le système de reconnaissance de l’iris surveille les yeux et si les deux yeux se trouvent dans le cadre de l’appareil photo, cette position est sans doute le centre de la pupille de l’œil gauche de la personne.

</dd> <dt>

**Distance**
</dt> <dd>

Distance entre l’emplacement réel du diaphragme et la distance focale idéale pour le diaphragme. Cette valeur est comprise entre-100 et 100. 0 indique la distance idéale, les valeurs positives indiquent que l’emplacement réel de l’iris est trop éloigné, et les valeurs négatives indiquent que l’emplacement réel est trop proche.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



 

 





