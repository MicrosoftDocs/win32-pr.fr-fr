---
description: Contient des informations sur un processeur.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Structure PROCESSOR_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319170"
---
# <a name="processor_power_information-structure"></a>\_Structure des informations d’alimentation du processeur \_

Contient des informations sur un processeur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nombre**
</dt> <dd>

Numéro du processeur système.

</dd> <dt>

**MaxMhz**
</dt> <dd>

Fréquence d’horloge maximale spécifiée du processeur système, en mégahertz.

</dd> <dt>

**CurrentMhz**
</dt> <dd>

Fréquence d’horloge du processeur, en mégahertz. Ce nombre correspond à la fréquence d’horloge du processeur spécifiée, multiplié par la limite actuelle du processeur.

</dd> <dt>

**MhzLimit**
</dt> <dd>

Limite de fréquence d’horloge du processeur, en mégahertz. Ce nombre correspond à la fréquence d’horloge du processeur spécifiée, multipliée par la limite actuelle de limitation thermique du processeur.

</dd> <dt>

**MaxIdleState**
</dt> <dd>

État d’inactivité maximal de ce processeur.

</dd> <dt>

**CurrentIdleState**
</dt> <dd>

État d’inactivité actuel de ce processeur.

</dd> </dl>

## <a name="remarks"></a>Notes

Notez que cette définition de structure a été omise par erreur dans Winnt. h. Cette erreur sera corrigée à l’avenir. En attendant, pour compiler votre application, incluez la définition de structure contenue dans cette rubrique dans votre code source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




