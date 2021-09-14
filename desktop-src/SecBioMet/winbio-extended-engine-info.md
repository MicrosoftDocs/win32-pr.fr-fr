---
title: Structure WINBIO_EXTENDED_ENGINE_INFO ( \_ types WINBIO. h)
description: Contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_ENGINE_INFO
- API du pointeur de structure PWINBIO_EXTENDED_ENGINE_INFO Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095954"
---
# <a name="winbio_extended_engine_info-structure"></a>\_Structure d' \_ informations du moteur étendu WINBIO \_

Contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**GenericEngineCapabilities**
</dt> <dd>

Fonctionnalités génériques du composant moteur qui est connecté à une unité biométrique spécifique.

</dd> <dt>

**Facteur**
</dt> <dd>

Type d’unité biométrique pour lequel cette structure contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur. Par exemple, si la valeur du membre **Factor** est **WINBIO \_ type \_ Fingerprint**, la structure **WINBIO \_ Extended \_ Engine \_ info** s’applique à un lecteur d’empreintes digitales et contient les informations pertinentes dans la structure **spécifique. Fingerprint** .

</dd> <dt>

**Plus**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée à un facteur biométrique spécifique.

<dl> <dt>

**Null**
</dt> <dd>

Réservé. Doit être zéro.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée aux caractéristiques du visage.

<dl> <dt>

**Capabilities**
</dt> <dd>

Réservé. Doit être zéro.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

Réservé. Doit être zéro.

</dd> </dl> </dd> </dl> </dd> <dt>

**Empreinte digitale**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée aux modèles d’empreintes digitales.

<dl> <dt>

**Capabilities**
</dt> <dd>

Réservé. Doit être zéro.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd>

Nombre d’exemples corrects requis pour créer un modèle d’empreinte digitale.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

Nombre total d’exemples corrects nécessaires à la création d’un modèle d’empreinte digitale.

</dd> <dt>

**Gestionnaire**
</dt> <dd>

Nombre d’échantillons corrects pour le centre de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> <dt>

**Périphérie**
</dt> <dd>

Nombre d’échantillons corrects pour le bord supérieur de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Nombre d’échantillons corrects pour le bord inférieur de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Nombre d’échantillons corrects pour le bord gauche de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> <dt>

**RightEdge**
</dt> <dd>

Nombre d’échantillons corrects pour le bord droit de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> </dl> </dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée aux modèles d’IRIS.

<dl> <dt>

**Capabilities**
</dt> <dd>

Réservé. Doit être zéro.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

Réservé. Doit être zéro.

</dd> </dl> </dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur pour une unité biométrique liée aux modèles vocaux.

<dl> <dt>

**Capabilities**
</dt> <dd>

Réservé. Doit être zéro.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

Réservé. Doit être zéro.

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



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
</dt> </dl>

 

 





