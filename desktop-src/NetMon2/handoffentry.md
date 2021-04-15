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
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525126"
---
# <a name="handoffentry-structure"></a>HANDOFFENTRY, structure

La structure **HANDOFFENTRY** définit une entrée de protocole spécifique dans une structure **HANDOFFTABLE** .

Cette structure est renseignée par Moniteur réseau en fonction des informations contenues dans un fichier. ini fourni par l’utilisateur fourni lors de l’appel de la fonction [**CreateHandoffTable**](createhandofftable.md) . Cette structure ne doit jamais être modifiée explicitement par une application.

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

Numéro de protocole fourni par le fichier. ini fourni par l’utilisateur.

</dd> <dt>

**visionnant \_ ProtocolHandle**
</dt> <dd>

Handle de protocole créé à l’aide du nom de protocole fourni par le fichier. ini fourni par l’utilisateur.

</dd> <dt>

**visionnant \_ ProtocolData**
</dt> <dd>

Données d’instance de protocole fournies par le fichier. ini fourni par l’utilisateur.

</dd> </dl>

## <a name="remarks"></a>Notes

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

 

 




