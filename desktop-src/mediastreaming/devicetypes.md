---
title: Énumération DeviceTypes
description: Décrit les types d’appareils DLNA pris en charge par l’API de diffusion multimédia en continu.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- API de diffusion multimédia par l’énumération DeviceTypes
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530939"
---
# <a name="devicetypes-enumeration"></a>Énumération DeviceTypes

Décrit les types d’appareils DLNA pris en charge par l’API de diffusion multimédia en continu.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Connue**
</dt> <dd>

Type d’appareil inconnu.

</dd> <dt>

<span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**
</dt> <dd>

Convertisseur de médias numériques DLNA (DMR). La valeur est équivalente au type d’appareil **urn : schemas-UPnP-org : Device : MediaRenderer : 1**.

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**
</dt> <dd>

Serveur de médias numériques DLNA (DMS). La valeur est équivalente au type d’appareil **urn : schemas-UPnP-org : Device : MediaServer : 1**.

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**
</dt> <dd>

Lecteur multimédia numérique DLNA

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| MIDL<br/> | <dl> <dt>Windows. Media. streaming. idl (référence Windows. Media. streaming. idl)</dt> </dl> |



 

 





