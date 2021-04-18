---
title: Énumération TransportStatus
description: Définit l’état de transport disponible tel que défini par les instructions UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- API de diffusion multimédia par l’énumération TransportStatus
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526666"
---
# <a name="transportstatus-enumeration"></a>Énumération TransportStatus

Définit l’état de transport disponible tel que défini par les instructions UPnP.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Connue**
</dt> <dd>

État du périphérique erroné.

</dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Bien**
</dt> <dd>

L’appareil est dans un état correct.

</dd> <dt>

<span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**
</dt> <dd>

Une erreur s’est produite sur l’appareil.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Famille**
</dt> <dd>

État antérieur de l’appareil à l’état de transport actuel.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| MIDL<br/> | <dl> <dt>Windows. Media. streaming. idl (référence Windows. Media. streaming. idl)</dt> </dl> |



 

 





