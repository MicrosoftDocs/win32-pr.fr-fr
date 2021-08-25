---
description: Contient des données qui décrivent un expert lorsqu’il démarre.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: EXPERTSTARTUPINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f49fcf3c87795dbd7c9e65745e1b5560331c96c471d8ff7b2c8a24560b143cb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911049"
---
# <a name="expertstartupinfo-structure"></a>EXPERTSTARTUPINFO, structure

La structure **EXPERTSTARTUPINFO** contient des données qui décrivent un expert lorsqu’il démarre.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Indicateurs**
</dt> <dd>

Indicateurs qui décrivent l’expert.

</dd> <dt>

**hCapture**
</dt> <dd>

Handle vers une capture.

</dd> <dt>

**szCaptureFile**
</dt> <dd>

Nom du fichier de capture.

</dd> <dt>

**dwFrameNumber**
</dt> <dd>

Numéro de frame.

</dd> <dt>

**hProtocol**
</dt> <dd>

Handle du protocole.

</dd> <dt>

**lpPropertyInst**
</dt> <dd>

Pointeur vers une structure [**PROPERTYINST**](propertyinst.md) .

</dd> <dt>

**sBitfield**
</dt> <dd> <dl> <dt>

**BitNumber**
</dt> <dd>

Utilisé uniquement si le membre **DataQualifier** de la structure [**PROPERTYINST**](propertyinst.md) est défini sur Prop \_ Qualys \_ Flags.

</dd> <dt>

**Ble**
</dt> <dd>

Utilisé uniquement si le membre **DataQualifier** de la structure [**PROPERTYINST**](propertyinst.md) est défini sur Prop \_ Qualys \_ Flags.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




