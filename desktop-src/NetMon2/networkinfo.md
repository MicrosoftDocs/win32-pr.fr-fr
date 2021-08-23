---
description: La structure NETWORKINFO décrit une carte réseau.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: NETWORKINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b5b57d7f051c1409c4b691d78d9173341efda984f35498289cd1eacb8c8b3199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555709"
---
# <a name="networkinfo-structure"></a>NETWORKINFO, structure

La structure NETWORKINFO décrit une carte réseau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**PermanentAddr**
</dt> <dd>

Adresse MAC permanente.

</dd> <dt>

**CurrentAddr**
</dt> <dd>

Adresse MAC actuelle.

</dd> <dt>

**OtherAddress**
</dt> <dd>

Autre adresse qui la prend en charge (par exemple, IP, IPX).

</dd> <dt>

**LinkSpeed**
</dt> <dd>

Vitesse de liaison, en Mbits/s.

</dd> <dt>

**MacType**
</dt> <dd>

Type de média.

</dd> <dt>

**MaxFrameSize**
</dt> <dd>

Taille de trame maximale autorisée.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Ce paramètre peut être l’un des indicateurs d’informations suivants :



| Valeur                                                                                                                                                                                                                                       | Signification                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**\_indicateurs NETWORKINFO \_ PMODE \_ non \_ pris en charge**</dt> </dl>    | La carte réseau ne prend pas en charge le mode de promiscuité, ce qui signifie qu’elle ne capturera que le trafic qui est diffusé par nature ou qui implique uniquement l’ordinateur local.<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**NETWORKINFO \_ indicateurs \_ RAS**</dt> </dl>                                                      | Il s’agit d’une carte réseau virtuelle qui est une connexion RAS (serveur d’accès à distance) par le biais d’un modem ou d’une autre carte réseau.<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**\_ \_ carte à distance drapeaux NETWORKINFO \_**</dt> </dl>                             | La carte réseau ne se trouve pas sur l’ordinateur local, mais elle est capturée sur un ordinateur distant à l’Bequest de l’ordinateur local.<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**\_indicateurs NETWORKINFO \_ distants \_ nal**</dt> </dl>                                | Périmé n’utilisez pas.<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**\_drapeaux NETWORKINFO \_ distants \_ \_ connectés**</dt> </dl> | Périmé n’utilisez pas.<br/>                                                                                                                                          |



 

</dd> <dt>

**TimestampScaleFactor**
</dt> <dd>

Par exemple, la valeur 1 indique 1/1 ms, 10 indique 1/10 ms, 100 indique 1/100 ms, et ainsi de suite.

</dd> <dt>

**NodeName**
</dt> <dd>

Nom de la station de travail distante.

</dd> <dt>

**PModeSupported**
</dt> <dd>

Indicateur de prise en charge du mode P de la carte réseau.

</dd> <dt>

**Commentaire**
</dt> <dd>

Champ de commentaire de l’adaptateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




