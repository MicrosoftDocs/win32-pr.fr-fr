---
description: Stocke des informations sur les sections de la mémoire partagée.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: Structure SHAREDMEMORY_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529311"
---
# <a name="sharedmemory_header-structure"></a>\_Structure d’en-tête SHAREDMEMORY

Stocke des informations sur les sections de la mémoire partagée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbTotal**
</dt> <dd>

Taille, en octets, des données référencées par cette structure d’en-tête.

</dd> <dt>

**cbOffsetSns**
</dt> <dd>

Taille, en octets, du décalage des numéros de série par rapport à la structure d’en-tête.

</dd> <dt>

**idxEvent**
</dt> <dd>

Index d’événements. Cette valeur est incrémentée avec des événements successifs.

</dd> <dt>

**dwEvent**
</dt> <dd>

Événement associé à cet en-tête.

</dd> <dt>

**confirmation**
</dt> <dd>

Identificateur de curseur référencé par l’en-tête de mémoire partagée.

</dd> <dt>

**sn**
</dt> <dd>

Numéro de série de l’en-tête de mémoire partagée.

</dd> <dt>

**sysEvt**
</dt> <dd>

Événement système, préfixe SE \_ \* , associé à cet en-tête. Pour plus d’informations, consultez la section Notes.

</dd> <dt>

**sysEvtData**
</dt> <dd>

Structure [**de \_ \_ données d’événement système**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) associée à l’événement système.

</dd> <dt>

**cPackets**
</dt> <dd>

Nombre de paquets associés à la mémoire partagée en cours.

</dd> <dt>

**cbPackets**
</dt> <dd>

Taille, en octets, des paquets associés à la section de la mémoire partagée actuelle.

</dd> <dt>

**fSnsPresent**
</dt> <dd>

Indicateur qui spécifie si les numéros de série sont présents dans la section de la mémoire partagée actuelle.

</dd> </dl>

## <a name="remarks"></a>Notes

Les valeurs suivantes sont définies pour le membre **sysEvt** .


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_données d’événement système \_**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



