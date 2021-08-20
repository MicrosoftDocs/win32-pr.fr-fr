---
title: DOSwarmStats, structure (Deliveryoptimization. h)
description: Contient des champs pour les statistiques de téléchargement et de téléchargement d’un fichier.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- DOSwarmStats, structure
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e148ecb77508fcacfbe5c22d0ed4cdb7c4b2845c53b710d21ebc5e544f98c04a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101681"
---
# <a name="doswarmstats-structure"></a>DOSwarmStats, structure

Contient des champs pour les statistiques de téléchargement et de téléchargement d’un fichier.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a>Membres

<dl> <dt>

**Combinaison**
</dt> <dd>

Chaîne terminée par le caractère null qui a été spécifiée avec l’appel **AddFileWithRanges** .

</dd> <dt>

**sourceURL**
</dt> <dd>

Chaîne terminée par le caractère null qui contient le nom du fichier sur le serveur (par exemple, https:// &lt; Server &gt; / &lt; path &gt; /file.ext).

</dd> <dt>

**Taille**
</dt> <dd>

Taille du fichier en octets.

</dd> <dt>

**totalBytesDownloaded**
</dt> <dd>

Nombre total d’octets transférés.

</dd> <dt>

**bytesFromLanPeers**
</dt> <dd>

Nombre d’octets transférés à partir d’homologues LAN.

</dd> <dt>

**bytesFromGroupPeers**
</dt> <dd>

Nombre d’octets transférés à partir des pairs du groupe.

</dd> <dt>

**bytesFromInternetPeers**
</dt> <dd>

Nombre d’octets transférés à partir d’homologues Internet.

</dd> <dt>

**bytesFromHttp**
</dt> <dd>

Nombre d’octets transférés à partir de http.

</dd> <dt>

**bytesFromDoinc**
</dt> <dd>

À usage interne uniquement.

</dd> <dt>

**bytesToLanPeers**
</dt> <dd>

Nombre d’octets transférés aux homologues LAN.

</dd> <dt>

**bytesToGroupPeers**
</dt> <dd>

Nombre d’octets transférés aux pairs du groupe.

</dd> <dt>

**bytesToInternetPeers**
</dt> <dd>

Nombre d’octets transférés aux pairs Internet.

</dd> <dt>

**httpConnectionCount**
</dt> <dd>

Nombre de connexions http.

</dd> <dt>

**doincConnectionCount**
</dt> <dd>

À usage interne uniquement.

</dd> <dt>

**lanConnectionCount**
</dt> <dd>

Nombre de connexions LAN.

</dd> <dt>

**groupConnectionCount**
</dt> <dd>

Nombre de connexions de groupe.

</dd> <dt>

**internetConnectionCount**
</dt> <dd>

Nombre de connexions Internet.

</dd> <dt>

**downloadDuration**
</dt> <dd>

Durée du transfert de fichiers en millisecondes.

</dd> <dt>

**downloadMode**
</dt> <dd>

Le mode de téléchargement utilisé, consultez [**DownloadMode**](downloadmode.md).

</dd> <dt>

**statut**
</dt> <dd>

L’état d’un transfert de fichiers, consultez [**SwarmStatus**](swarmstatus.md).

</dd> <dt>

**isBackground**
</dt> <dd>

True, s’il s’agit d’un transfert en arrière-plan.

</dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





