---
description: La \_ structure d’informations sur le port \_ 2 identifie un port d’imprimante pris en charge.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Structure PORT_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520024"
---
# <a name="port_info_2-structure"></a>\_Structure des informations sur le port \_ 2

La structure d' **\_ informations sur le port \_ 2** identifie un port d’imprimante pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a>Membres

<dl> <dt>

**pPortName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie un port imprimante pris en charge (par exemple, « LPT1 : »).

</dd> <dt>

**pMonitorName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie une analyse installée (par exemple, « PJL Monitor »). Il peut s’agir de la **valeur null**.

</dd> <dt>

**pDescription**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui décrit le port plus en détail (par exemple, si **pPortName** est « LPT1 : », **pDescription** est « port imprimante »). Il peut s’agir de la **valeur null**.

</dd> <dt>

**fPortType**
</dt> <dd>

Masque de masque décrivant le type de port. Ce membre peut être une combinaison des valeurs suivantes :

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**\_écriture du type de port \_**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**TYPE de PORT \_ \_ lu**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**TYPE de PORT \_ \_ Redirigé**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**TYPE de PORT \_ \_ NET \_ attaché**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Réservé doit être égal à zéro.

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez la **structure \_ informations \_ sur le port 2** lors de l’appel de [**EnumPorts**](enumports.md) si plusieurs moniteurs prennent en charge les mêmes ports.

Le membre **fPortType** peut être interrogé pour déterminer les informations relatives au port. Notez que les paramètres de port n’affectent pas les attributs d’imprimante (tels qu’ils sont retournés par le membre **attributs** de [**Printer \_ info \_ 2**](printer-info-2.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Informations sur \_ le port 2S** (Unicode) et **\_ \_ informations sur le port \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




