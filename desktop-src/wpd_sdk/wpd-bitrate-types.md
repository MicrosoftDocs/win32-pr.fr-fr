---
description: Le \_ \_ type d’énumération des types de débits wpd fournit une description du type de compression fichiers audio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Énumération WPD_BITRATE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5b50b56222014119a50c9d4ecb0fd7eb96694b30f35fbcbb72dc6550fdf88606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704049"
---
# <a name="wpd_bitrate_types-enumeration"></a>\_Énumération des types de débit wpd \_

Le type d’énumération des **\_ \_ types de débits wpd** fournit une description du type de compression d’un fichier audio.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**\_type de débit wpd \_ \_ non utilisé**
</dt> <dd>

Cette valeur n’a pas été spécifiée.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_type de débit wpd \_ \_ discret**
</dt> <dd>

Compression à vitesse de transmission constante.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**VARIABLE de type de vitesse de \_ transmission wpd \_ \_**
</dt> <dd>

Compression à vitesse de transmission variable.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**\_type de vitesse de transmission wpd \_ \_ libre**
</dt> <dd>

Taux binaire de format libre. Il s’agit d’une vitesse binaire constante inférieure à la vitesse de transmission maximale autorisée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




