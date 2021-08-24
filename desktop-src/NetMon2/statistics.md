---
description: La structure des statistiques fournit des statistiques pour la capture. Certaines de ces statistiques sont générées par Moniteur réseau, tandis que d’autres sont générées par la carte réseau à laquelle le NPP est connecté.
ms.assetid: 5e30ae30-d8ad-4336-9e4d-fa10ceefc966
title: Structure des statistiques (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATISTICS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 273e6ba9e32337cc65b3dce979d2ff407b904595237b60025e42fc58e57d9823
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778279"
---
# <a name="statistics-structure"></a>Structure des statistiques

La structure des **statistiques** fournit des statistiques pour la capture. Certaines de ces statistiques sont générées par Moniteur réseau, tandis que d’autres sont générées par la carte réseau à laquelle le NPP est connecté.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STATISTICS {
  __int64 TimeElapsed;
  DWORD   TotalFramesCaptured;
  DWORD   TotalBytesCaptured;
  DWORD   TotalFramesFiltered;
  DWORD   TotalBytesFiltered;
  DWORD   TotalMulticastsFiltered;
  DWORD   TotalBroadcastsFiltered;
  DWORD   TotalFramesSeen;
  DWORD   TotalBytesSeen;
  DWORD   TotalMulticastsReceived;
  DWORD   TotalBroadcastsReceived;
  DWORD   TotalFramesDropped;
  DWORD   TotalFramesDroppedFromBuffer;
  DWORD   MacFramesReceived;
  DWORD   MacCRCErrors;
  __int64 MacBytesReceivedEx;
  DWORD   MacFramesDropped_NoBuffers;
  DWORD   MacMulticastsReceived;
  DWORD   MacBroadcastsReceived;
  DWORD   MacFramesDropped_HwError;
} STATISTICS, *LPSTATISTICS;
```



## <a name="members"></a>Membres

<dl> <dt>

**TimeElapsed**
</dt> <dd>

Temps écoulé, en microsecondes.

</dd> <dt>

**TotalFramesCaptured**
</dt> <dd>

Nombre total de frames actuellement stockés. Ce nombre est limité par la taille du fichier de capture ou de la mémoire tampon utilisée pour stocker les frames.

</dd> <dt>

**TotalBytesCaptured**
</dt> <dd>

Nombre total d’octets actuellement stockés. Ce nombre est limité par la taille du fichier de capture ou de la mémoire tampon utilisée pour stocker les frames.

</dd> <dt>

**TotalFramesFiltered**
</dt> <dd>

Nombre total de trames transmises par le filtre de capture actuel. Si aucun filtre n’est utilisé, cette valeur est la même que **TotalFramesSeen**.

</dd> <dt>

**TotalBytesFiltered**
</dt> <dd>

Nombre total de trames transmises par le filtre de capture actuel. Si aucun filtre n’est utilisé, cette valeur est la même que **TotalBytesSeen**.

</dd> <dt>

**TotalMulticastsFiltered**
</dt> <dd>

Ce membre est obsolète.

</dd> <dt>

**TotalBroadcastsFiltered**
</dt> <dd>

Ce membre est obsolète.

</dd> <dt>

**TotalFramesSeen**
</dt> <dd>

Nombre total de trames gérées par la carte réseau.

</dd> <dt>

**TotalBytesSeen**
</dt> <dd>

Nombre total d’octets gérés par la carte réseau.

</dd> <dt>

**TotalMulticastsReceived**
</dt> <dd>

Ce membre est obsolète.

</dd> <dt>

**TotalBroadcastsReceived**
</dt> <dd>

Ce membre est obsolète.

</dd> <dt>

**TotalFramesDropped**
</dt> <dd>

Nombre total de frames supprimés (frames ayant réussi le filtre mais non enregistrés).

</dd> <dt>

**TotalFramesDroppedFromBuffer**
</dt> <dd>

Nombre d’images supprimées du fichier ou de la mémoire tampon de capture. Lorsque la mémoire tampon est saturée, les trames plus anciennes sont supprimées pour faire de la place pour les nouvelles.

</dd> <dt>

**MacFramesReceived**
</dt> <dd>

Nombre de trames envoyées par la carte réseau.

</dd> <dt>

**MacCRCErrors**
</dt> <dd>

Nombre d’erreurs CRC signalées par la carte réseau.

</dd> <dt>

**MacBytesReceivedEx**
</dt> <dd>

Nombre d’octets reçus par la carte réseau.

</dd> <dt>

**MacFramesDropped \_ Nobuffers**
</dt> <dd>

Nombre de trames signalées par la carte réseau en raison d’un manque d’espace de mémoire tampon.

</dd> <dt>

**MacMulticastsReceived**
</dt> <dd>

Nombre de multidiffusions signalées par la carte réseau.

</dd> <dt>

**MacBroadcastsReceived**
</dt> <dd>

Nombre de diffusions envoyées par la carte réseau.

</dd> <dt>

**MacFramesDropped \_ HwError**
</dt> <dd>

Nombre de trames signalées par la carte réseau en raison d’erreurs matérielles.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est utilisée pour récupérer des [*statistiques totales*](t.md)et pour suspendre ou arrêter la capture actuelle.

Les statistiques totales ne peuvent pas être récupérées lors de l’utilisation de l’interface NPP [IESP](iesp.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IStats::GetTotalStatistics](istats-gettotalstatistics.md)
</dt> <dt>

[IDelaydC ::P ause](idelaydc-pause.md)
</dt> <dt>

[IESP ::P ause](iesp-pause.md)
</dt> <dt>

[IRTC ::P ause](irtc-pause.md)
</dt> <dt>

[IStats ::P ause](istats-pause.md)
</dt> <dt>

[IDelaydC :: Stop](idelaydc-stop.md)
</dt> <dt>

[IESP :: Stop](iesp-stop.md)
</dt> <dt>

[IRTC :: Stop](irtc-stop.md)
</dt> <dt>

[IStatsC :: Stop](istats-stop.md)
</dt> </dl>

 

 




