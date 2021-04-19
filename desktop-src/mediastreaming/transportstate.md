---
title: Énumération TransportState
description: Définit les États de transport disponibles, comme défini par les instructions UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- API de diffusion multimédia par l’énumération TransportState
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526456"
---
# <a name="transportstate-enumeration"></a>Énumération TransportState

Définit les États de transport disponibles, comme défini par les instructions UPnP.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Connue**
</dt> <dd>

État de l’appareil erroné.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Mis**
</dt> <dd>

Le transport de l’appareil est à l’état arrêté.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Écoute**
</dt> <dd>

Le transport de l’appareil est à l’État en cours d’exécution.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition**
</dt> <dd>

Le transport de l’appareil est dans un état de transition qui entraîne une autre valeur d’État.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Suspendu**
</dt> <dd>

Le transport de l’appareil est dans un état suspendu.

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**D'**
</dt> <dd>

Le transport de l’appareil est dans un état d’enregistrement.

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**
</dt> <dd>

Le transport de l’appareil n’a pas d’URI défini pour la lecture.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Famille**
</dt> <dd>

État antérieur de l’appareil à l’état de transport actuel.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| MIDL<br/> | <dl> <dt>Windows. Media. streaming. idl (référence Windows. Media. streaming. idl)</dt> </dl> |



 

 





