---
description: Spécifie les membres de la structure NMCOLUMNVARIANT.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: NMCOLUMNTYPE, énumération (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5e3877a15a55ac1d942a068843173e2771202047691f3df96601fe4b9de3152a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799499"
---
# <a name="nmcolumntype-enumeration"></a>Énumération NMCOLUMNTYPE

L’énumération **NMCOLUMNTYPE** spécifie les membres de la structure [**NMCOLUMNVARIANT**](nmcolumnvariant.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE \_ UINT8**
</dt> <dd>

entier non signé 8 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE \_ SINT8**
</dt> <dd>

entier signé 8 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE \_ UINT16**
</dt> <dd>

entier non signé 16 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE \_ SINT16**
</dt> <dd>

entier signé 16 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE \_ UInt32**
</dt> <dd>

entier non signé 32 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE \_ SINT32**
</dt> <dd>

Entier signé 32 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE \_ FLOAT64**
</dt> <dd>

virgule flottante 64 bits.

</dd> <dt>

<span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**\_Frame NMCOLUMNTYPE**
</dt> <dd>

Numéro de frame.

</dd> <dt>

<span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE \_ YesNo**
</dt> <dd>

« Oui » ou « non ».

</dd> <dt>

<span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE \_ microphone**
</dt> <dd>

« On » ou « OFF »

</dd> <dt>

<span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE \_ truefalse**
</dt> <dd>

« True » ou « false ».

</dd> <dt>

<span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE \_ MACADDR**
</dt> <dd>

Adresse MAC.

</dd> <dt>

<span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE \_ IPXADDR**
</dt> <dd>

Adresse IPX.

</dd> <dt>

<span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE \_ ipaddr**
</dt> <dd>

Adresse IP.

</dd> <dt>

<span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE \_ VARTIME**
</dt> <dd>

Heure de la variante.

</dd> <dt>

<span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**\_chaîne NMCOLUMNTYPE**
</dt> <dd>

Pointeur vers une chaîne.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




