---
description: La structure PROTOCOLINFO décrit un protocole.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: PROTOCOLINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311898"
---
# <a name="protocolinfo-structure"></a>PROTOCOLINFO, structure

La structure **PROTOCOLINFO** décrit un protocole.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**ProtocolID**
</dt> <dd>

Identificateur de protocole attribué par le système de la session d’exécution spécifiée.

</dd> <dt>

**Propriétédescription**
</dt> <dd>

Base de données de propriétés du protocole spécifié.

</dd> <dt>

**ProtocolName**
</dt> <dd>

Nom de protocole abrégé.

</dd> <dt>

**HelpFile**
</dt> <dd>

Nom de fichier d’aide facultatif associé au protocole.

</dd> <dt>

**Commentaire**
</dt> <dd>

Commentaire décrivant le protocole.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




