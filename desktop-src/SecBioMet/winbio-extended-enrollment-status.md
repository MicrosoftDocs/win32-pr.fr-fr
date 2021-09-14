---
title: Structure WINBIO_EXTENDED_ENROLLMENT_STATUS ( \_ types WINBIO. h)
description: Contient des informations supplémentaires sur l’état d’une inscription en cours.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_ENROLLMENT_STATUS
- API du pointeur de structure PWINBIO_EXTENDED_ENROLLMENT_STATUS Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095950"
---
# <a name="winbio_extended_enrollment_status-structure"></a>WINBIO \_ \_ structure d’état d’inscription étendue \_

Contient des informations supplémentaires sur l’état d’une inscription en cours.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a>Membres

<dl> <dt>

**TemplateStatus**
</dt> <dd>

État de l’exemple de collection pour le modèle d’inscription. Les valeurs suivantes sont possibles pour ce membre.



| Valeur                                                                                                                                                                                                  | Signification                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**\_OK**</dt> </dl>                                                                     | L’inscription est prête à être enregistrée.<br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ opération non valide \_**</dt> </dl> | Aucune inscription n’est en cours.<br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ d' \_ autres \_ données**</dt> </dl>                         | D’autres exemples sont requis pour terminer le modèle.<br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E \_ mauvaise \_ capture**</dt> </dl>                   | L’exemple le plus récent n’est pas utilisable.<br/>               |



 

</dd> <dt>

**RejectDetail**
</dt> <dd>

La raison pour laquelle l’exemple le plus récent est inutilisable, si la valeur du membre **TemplateStatus** est **WINBIO \_ E \_ Bad \_ capture**.

</dd> <dt>

**PercentComplete**
</dt> <dd>

Meilleure estimation de l’adaptateur de moteur pour le pourcentage du modèle complet, en tant que valeur comprise entre 0 et 100.

</dd> <dt>

**Facteur**
</dt> <dd>

Type d’unité biométrique pour lequel cette structure contient des informations sur les fonctionnalités et les exigences d’inscription de l’adaptateur de moteur. Par exemple, si la valeur du membre **Factor** est **WINBIO \_ type \_ Fingerprint**, la structure [**WINBIO \_ Extended \_ Engine \_ info**](winbio-extended-engine-info.md) s’applique à un lecteur d’empreintes digitales et contient les informations pertinentes dans la structure **spécifique. Fingerprint** .

</dd> <dt>

**Sous-fait**
</dt> <dd>

Valeur **de \_ sous- \_ type biométrique WINBIO** qui fournit des informations supplémentaires sur l’inscription.

</dd> <dt>

**Plus**
</dt> <dd>

Informations sur l’état d’une inscription en cours pour un facteur biométrique spécifique.

<dl> <dt>

**Null**
</dt> <dd>

Réservé. Doit être zéro.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informations sur l’état d’une inscription en cours pour les caractéristiques du visage.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Position dans le cadre de l’appareil photo de la personne à inscrire, en pixels. La taille du cadre de l’appareil photo détermine la limite supérieure du nombre de pixels pour cette position. Pour déterminer la taille du cadre de l’appareil photo, accédez à la propriété **WINBIO \_ étendue des \_ \_ \_ informations de capteur** . Un client qui utilise le moniteur de présence doit effectuer l’opération de mise à l’échelle pour mapper la position au frame de l’appareil photo.

</dd> <dt>

**Distance**
</dt> <dd>

Distance entre l’emplacement réel de la face et la distance focale idéale pour la face. Cette valeur est comprise entre-100 et 100. 0 indique la distance idéale, les valeurs positives indiquent que l’emplacement réel du visage est trop éloigné, et les valeurs négatives indiquent que l’emplacement réel est trop proche.

</dd> </dl> </dd> <dt>

**Empreinte digitale**
</dt> <dd>

Informations sur l’état d’une inscription en cours pour les modèles d’empreintes digitales.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

Nombre total d’échantillons requis pour créer un modèle d’empreinte digitale.

</dd> <dt>

**Gestionnaire**
</dt> <dd>

Nombre d’échantillons pour le centre de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> <dt>

**Périphérie**
</dt> <dd>

Nombre d’échantillons pour le bord supérieur de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Nombre d’échantillons pour le bord inférieur de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Nombre d’échantillons pour le bord gauche de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> <dt>

**RightEdge**
</dt> <dd>

Nombre d’échantillons pour le bord droit de l’empreinte digitale requis pour créer un modèle d’empreinte digitale.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informations sur l’état d’une inscription en cours pour les modèles d’IRIS.

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

</dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informations sur l’état d’une inscription en cours pour les modèles vocaux.

<dl> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



 

 





