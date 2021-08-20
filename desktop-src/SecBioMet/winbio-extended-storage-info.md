---
title: Structure WINBIO_EXTENDED_STORAGE_INFO ( \_ types WINBIO. h)
description: Contient des informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_STORAGE_INFO
- API du pointeur de structure PWINBIO_EXTENDED_STORAGE_INFO Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8a9f133baf77a77d3db33001e996accc9574f86ad708037900a5db7c0c5e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910380"
---
# <a name="winbio_extended_storage_info-structure"></a>\_Structure des \_ informations de stockage étendu WINBIO \_

Contient des informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**GenericStorageCapabilities**
</dt> <dd>

Fonctionnalités génériques du composant de stockage connecté à une unité biométrique spécifique.

</dd> <dt>

**Facteur**
</dt> <dd>

Type d’unité biométrique pour lequel cette structure contient des informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage. Par exemple, si la valeur du membre **Factor** est **WINBIO \_ type \_ Fingerprint**, la structure **WINBIO \_ Extended \_ Storage \_ info** s’applique à un lecteur d’empreintes digitales et contient les informations pertinentes dans la structure **spécifique. Fingerprint** .

</dd> <dt>

**Plus**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée à un facteur biométrique spécifique.

<dl> <dt>

**Null**
</dt> <dd>

Réservé. Doit être zéro.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée aux caractéristiques du visage.

<dl> <dt>

**Capabilities**
</dt> <dd>

Fonctionnalités de reconnaissance faciale du composant de stockage connecté à une unité biométrique spécifique.

</dd> </dl> </dd> <dt>

**Empreinte digitale**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée aux modèles d’empreintes digitales.

<dl> <dt>

**Capabilities**
</dt> <dd>

Fonctionnalités de reconnaissance d’empreintes digitales du composant de stockage connecté à une unité biométrique spécifique

</dd> </dl> </dd> <dt>

**IRI**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée aux modèles d’IRIS.

<dl> <dt>

**Capabilities**
</dt> <dd>

Fonctionnalités de reconnaissance de l’iris du composant de stockage connecté à une unité biométrique spécifique

</dd> </dl> </dd> <dt>

**Voice**
</dt> <dd>

Informations sur les fonctionnalités et les exigences d’inscription de la carte de stockage pour une unité biométrique liée aux modèles vocaux.

<dl> <dt>

**Capabilities**
</dt> <dd>

Fonctionnalités de reconnaissance vocale du composant de stockage connecté à une unité biométrique spécifique

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Constantes de type de biométrie WINBIO \_**](winbio-biometric-type-constants.md)
</dt> <dt>

[**\_Constantes de capacité WINBIO**](winbio-capability-constants.md)
</dt> </dl>

 

 





