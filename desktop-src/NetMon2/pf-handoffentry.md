---
description: La \_ structure HANDOFFENTRY de PF définit un protocole qui Moniteur réseau ajoute au jeu de remise d’un analyseur.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Structure de PF_HANDOFFENTRY (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: faf98490424754d6ae2223ca063e0e3a4eec69c113b1a220e9657b7db5edbb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778669"
---
# <a name="pf_handoffentry-structure"></a>PF \_ HANDOFFENTRY, structure

La **structure \_ HANDOFFENTRY de PF** définit un protocole qui Moniteur réseau ajoute au jeu de remise d’un analyseur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**szIniFile**
</dt> <dd>

Nom du fichier INI associé au protocole.

</dd> <dt>

**szIniSection**
</dt> <dd>

Étiquette de section dans le fichier INI.

</dd> <dt>

**szProtocol**
</dt> <dd>

Nom du protocole.

</dd> <dt>

**dwHandOffValue**
</dt> <dd>

Valeur associée au protocole.

</dd> <dt>

**ValueFormatBase**
</dt> <dd>

Base numérique de la valeur de protocole spécifiée dans **dwHandOffValue**. La fonction **ValueFormatBase** doit être définie sur l’un des éléments suivants :



| Valeur                                                                                                                                                                                                                        | Signification                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**BASE de format de valeur de transfert \_ \_ \_ \_ inconnue**</dt> </dl> | Base inconnue<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**FORMAT de la valeur de transfert \_ \_ \_ décimal de base \_**</dt> </dl> | Base décimale<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**\_hexadécimal de \_ base de format de valeur de transfert \_ \_**</dt> </dl>             | Base hexadécimale<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Un tableau des structures **\_ HANDOFFENTRY PF** est utilisé dans la structure [ \_ HANDOFFSET de PF](pf-handoffset.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_HANDOFFSET PF](pf-handoffset.md)
</dt> </dl>

 

 




