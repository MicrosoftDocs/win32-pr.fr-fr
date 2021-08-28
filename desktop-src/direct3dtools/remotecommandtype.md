---
description: '<span id="vspixengine.remotecommandtype"></span>énumération RemoteCommandType : énumération utilisée pour communiquer entre le moteur de capture et un hôte (comme Visual Studio Graphics Diagnostics).'
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération RemoteCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B517F70C-2BFB-42E7-8597-AC5915AB2DE0
api_name:
- RemoteCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 73accd6f73a7c33219c83a3285837d2e1c7c133a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631717"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span id="vspixengine.remotecommandtype"></span>Énumération RemoteCommandType

énumération utilisée pour communiquer entre le moteur de capture et un hôte (par exemple, Visual Studio Graphics Diagnostics).

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**  
Démarre la communication.

<span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**  
Démarre une session de capture Graphics Diagnostics (une expérience).

<span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**  
Démarre une capture (identique à l’affichage de l’écran d’impression). Envoyé par un hôte lors de la capture d’un frame.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



