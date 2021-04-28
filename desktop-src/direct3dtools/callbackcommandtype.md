---
description: '<span id="vspixengine.callbackcommandtype"></span>Énumération CallbackCommandType : énumération utilisée pour communiquer entre le moteur de capture et un hôte (tel que Visual Studio Graphics Diagnostics).'
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération CallbackCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 78E0CD6C-5264-4F66-BAB9-20DC9C0C1EC1
api_name:
- CallbackCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85e1b7d396d125add00824e9b7c94086e0da6be2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090127"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span id="vspixengine.callbackcommandtype"></span>Énumération CallbackCommandType

Énumération utilisée pour communiquer entre le moteur de capture et un hôte (tel que Visual Studio Graphics Diagnostics).

## <a name="syntax"></a>Syntaxe


```C++
};
```

## <a name="constants"></a>Constantes

<span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**  
Résultats de BeginCommunication.

<span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**  
Erreurs.

<span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**  
Avertissements.

<span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**  
Messages.

<span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**  
Résultat de RunExperiment.

<span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**  
Résultat de RunAction.

<span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**  
Valeur qui indique un rappel à appeler quand de nouveaux frames ont été capturés et prêts à être affichés.

<span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**  
Résultats d’une version antérieure de BeginCommunication utilisée sur Windows 7 et Windows 8.

<span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**  
Résultat de RunExperiementProgress.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



