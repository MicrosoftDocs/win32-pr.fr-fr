---
description: La structure HANDOFFENTRY définit une entrée de protocole spécifique dans une structure HANDOFFTABLE.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: HANDOFFENTRY, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 692b9e925442920a67434f74c9e8a8ebd225fc417cbbf419b6eb568aa9eee2df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981412"
---
# <a name="handoffentry-structure"></a>HANDOFFENTRY, structure

La structure **HANDOFFENTRY** définit une entrée de protocole spécifique dans une structure **HANDOFFTABLE** .

Cette structure est renseignée par Moniteur réseau en fonction des informations contenues dans un fichier .ini fourni par l’utilisateur fourni lors de l’appel de la fonction [**CreateHandoffTable**](createhandofftable.md) . Cette structure ne doit jamais être modifiée explicitement par une application.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**visionnant \_ SIG**
</dt> <dd>

Signature qui identifie cette entrée en tant qu’entrée de table de remise.

</dd> <dt>

**visionnant \_ ProtIdentNumber**
</dt> <dd>

Numéro de protocole fourni par l’utilisateur .ini fichier.

</dd> <dt>

**visionnant \_ ProtocolHandle**
</dt> <dd>

Handle de protocole créé à l’aide du nom de protocole fourni par l’utilisateur .ini fichier fourni.

</dd> <dt>

**visionnant \_ ProtocolData**
</dt> <dd>

Données d’instance de protocole fournies par l’utilisateur .ini fichier.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est renseignée par Moniteur réseau lorsque Moniteur réseau crée une table de remise.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




