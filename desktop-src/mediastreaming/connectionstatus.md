---
title: Énumération ConnectionStatus
description: Représente l’état de l’appareil dans le réseau en dernier vu.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- API de diffusion multimédia par l’énumération ConnectionStatus
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540481"
---
# <a name="connectionstatus-enumeration"></a>Énumération ConnectionStatus

Représente l’état de l’appareil dans le réseau en dernier vu.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Service**
</dt> <dd>

L’appareil est en ligne et actif sur le réseau.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion**
</dt> <dd>

L’appareil est hors connexion.

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**En veille**
</dt> <dd>

L’appareil est actuellement hors connexion, mais peut se réveiller automatiquement lorsqu’une tentative est faite pour communiquer avec lui.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| MIDL<br/> | <dl> <dt>Windows. Media. streaming. idl (référence Windows. Media. streaming. idl)</dt> </dl> |



 

 





