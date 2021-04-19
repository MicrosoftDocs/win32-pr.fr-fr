---
description: L' \_ opération wpd \_ indique les valeurs d’énumération qui décrivent l’état actuel d’une opération en cours.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Énumération WPD_OPERATION_STATES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535303"
---
# <a name="wpd_operation_states-enumeration"></a>\_Énumération des États de l’opération wpd \_

L' **\_ opération wpd \_ indique** les valeurs d’énumération qui décrivent l’état actuel d’une opération en cours.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**État de l' \_ opération wpd \_ \_ non spécifié**
</dt> <dd>

L’opération actuelle est dans un État non spécifié (non défini) et inconnu.

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**État de l' \_ opération wpd \_ \_ démarré**
</dt> <dd>

L’opération est démarrée.

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**État de l' \_ opération wpd \_ \_ en cours d’exécution**
</dt> <dd>

L’opération est en cours d’exécution.

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**État de l' \_ opération wpd \_ \_ suspendu**
</dt> <dd>

L’opération est suspendue.

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**État de l' \_ opération wpd \_ \_ annulé**
</dt> <dd>

L’opération est annulée.

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**État de l' \_ opération wpd \_ \_ terminé**
</dt> <dd>

L’opération est terminée.

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**État de l' \_ opération wpd \_ \_ abandonné**
</dt> <dd>

L’opération est abandonnée.

</dd> </dl>

## <a name="remarks"></a>Notes

Ces valeurs sont reçues dans le rappel défini par l’application ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




