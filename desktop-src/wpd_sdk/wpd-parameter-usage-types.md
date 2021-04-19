---
description: Le \_ \_ \_ type d’énumération des types d’utilisation de paramètre wpd décrit comment un paramètre de méthode est utilisé dans une méthode donnée.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: Énumération WPD_PARAMETER_USAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539623"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>\_ \_ Énumération des types d’utilisation des paramètres wpd \_

Le type d’énumération des [**\_ types d' \_ utilisation \_ de paramètre wpd**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) décrit comment un paramètre de méthode est utilisé dans une méthode donnée.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_retour de \_ l’utilisation des paramètres wpd \_**
</dt> <dd>

Le paramètre reçoit la valeur de retour, si elle est spécifiée par la méthode.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_ \_ utilisation des paramètres wpd \_ dans**
</dt> <dd>

Le paramètre contient une valeur d’entrée avant l’appel de la méthode.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**\_utilisation du paramètre wpd \_ \_ out**
</dt> <dd>

Le paramètre contient une valeur de sortie lorsque la méthode est retournée.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_utilisation du paramètre wpd \_ \_ INOUT**
</dt> <dd>

Le paramètre contient une valeur d’entrée avant que la méthode soit appelée et une valeur de sortie lors de son retour.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

