---
description: La structure SESSIONSTATS fournit des statistiques sur une session.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: SESSIONSTATS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229614"
---
# <a name="sessionstats-structure"></a>SESSIONSTATS, structure

La structure **SESSIONSTATS** fournit des statistiques sur une [*session*](s.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a>Membres

<dl> <dt>

**NextSession**
</dt> <dd>

Index de la session suivante du propriétaire de la station.

</dd> <dt>

**StationOwner**
</dt> <dd>

Index d’une station propriétaire dans le tableau de structures [STATIONSTATS](stationstats.md) associées. La station propriétaire est la station qui a initié la session, la station qui a envoyé les paquets de la session.

</dd> <dt>

**StationPartner**
</dt> <dd>

Index de l’autre station dans le tableau de structures [STATIONSTATS](stationstats.md) associé. La station partenaire est la station qui a reçu les paquets de la session.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Ce membre est obsolète.

</dd> <dt>

**TotalPacketsSent**
</dt> <dd>

Nombre de paquets envoyés dans la session.

</dd> </dl>

## <a name="remarks"></a>Notes

Moniteur réseau stocke les informations de session et de station dans deux tableaux associés, dont les éléments sont respectivement des structures **SESSIONSTATS** et [STATIONSTATS](stationstats.md) . Les membres de ces structures peuvent être utilisés pour naviguer entre eux. Par exemple, pour passer à la session suivante pour un propriétaire de station spécifique, utilisez **NextSession**. Pour accéder au propriétaire et à la station partenaire de la session dans le tableau STATIONSTATS, utilisez l’index fourni dans **StationOwner** et **StationPartner**.

> [!Note]  
> Le tableau SESSIONSTATS contient un élément pour chaque session dans la capture en cours. L’algorithme Moniteur réseau utilise pour ajouter des éléments au tableau SESSIONSTATS est basé sur l’enregistrement efficace des informations lorsque la capture est en cours. Par conséquent, la session suivante pour une station propriétaire spécifique n’est pas toujours l’élément suivant dans le tableau.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




