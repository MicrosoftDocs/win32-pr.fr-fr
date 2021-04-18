---
description: Le \_ \_ \_ \_ type d’énumération des valeurs d’état de couleur wpd corrigées décrit l’état de correction de couleur d’un fichier image ou vidéo.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: Énumération WPD_COLOR_CORRECTED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528921"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a>\_ \_ \_ Énumération des valeurs d’État corrigées de couleurs wpd \_

Le type d’énumération des **\_ valeurs d’état de couleur wpd \_ corrigées \_ \_** décrit l’état de correction de couleur d’un fichier image ou vidéo.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_État corrigé de la couleur wpd \_ corrigé \_ \_ \_**
</dt> <dd>

La couleur de l’image n’a pas été corrigée.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**\_ \_ État corrigé de la couleur \_ \_ wpd corrigé**
</dt> <dd>

La couleur de l’image a été corrigée.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**l' \_ État de la couleur wpd \_ corrigé \_ \_ \_ ne doit pas \_ être \_ corrigé**
</dt> <dd>

L’image n’a pas été et ne doit pas être corrigée.

</dd> </dl>

## <a name="remarks"></a>Notes

Indique l’état de couleur corrigé d’une image. Cette énumération est utilisée par la propriété de l' [ \_ \_ \_ \_ État couleur corrigée de l’image wpd](image-properties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




