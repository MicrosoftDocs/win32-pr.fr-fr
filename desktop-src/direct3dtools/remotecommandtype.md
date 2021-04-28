---
description: '<span id="vspixengine.remotecommandtype"></span>Énumération RemoteCommandType : énumération utilisée pour communiquer entre le moteur de capture et un hôte (tel que Visual Studio Graphics Diagnostics).'
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
ms.openlocfilehash: ed57b9b044613351e99096a8c8cb741b8ad7a269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110503"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span data-ttu-id="c4689-103"><span id="vspixengine.remotecommandtype"></span>Énumération RemoteCommandType</span><span class="sxs-lookup"><span data-stu-id="c4689-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType enumeration</span></span>

<span data-ttu-id="c4689-104">Énumération utilisée pour communiquer entre le moteur de capture et un hôte (tel que Visual Studio Graphics Diagnostics).</span><span class="sxs-lookup"><span data-stu-id="c4689-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4689-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4689-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="c4689-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c4689-106">Constants</span></span>

<span data-ttu-id="c4689-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span><span class="sxs-lookup"><span data-stu-id="c4689-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span></span>  
<span data-ttu-id="c4689-108">Démarre la communication.</span><span class="sxs-lookup"><span data-stu-id="c4689-108">Starts communication.</span></span>

<span data-ttu-id="c4689-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span><span class="sxs-lookup"><span data-stu-id="c4689-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span></span>  
<span data-ttu-id="c4689-110">Démarre une session de capture Graphics Diagnostics (une expérience).</span><span class="sxs-lookup"><span data-stu-id="c4689-110">Starts a Graphics Diagnostics capture session (an experiment).</span></span>

<span data-ttu-id="c4689-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span><span class="sxs-lookup"><span data-stu-id="c4689-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span></span>  
<span data-ttu-id="c4689-112">Démarre une capture (identique à l’affichage de l’écran d’impression).</span><span class="sxs-lookup"><span data-stu-id="c4689-112">Starts a capture (same as hitting print screen).</span></span> <span data-ttu-id="c4689-113">Envoyé par un hôte lors de la capture d’un frame.</span><span class="sxs-lookup"><span data-stu-id="c4689-113">Sent by a host when capturing a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4689-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4689-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c4689-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4689-115">Header</span></span></p></td><td><span data-ttu-id="c4689-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c4689-116">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



