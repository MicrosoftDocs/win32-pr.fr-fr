---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380743"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>IAgentAudioOutputPropertiesEx :: GetStatus

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

Récupère l’état du canal audio.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

État du canal de sortie audio, qui peut prendre l’une des valeurs suivantes :



| Valeur                                                                         | Description                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| État audio **abrégé non signé const** **\_ \_ disponible = 0 ;**<br/>         | Le canal de sortie audio est disponible (inoccupé).                                                              |
| **const unsigned short** **audio \_ Status \_ noaudio = 1 ;**<br/>           | Il n’existe pas de prise en charge de la sortie audio. par exemple, parce qu’il n’y a pas de carte audio.                             |
| **const unsigned short** **audio \_ Status \_ CANTOPENAUDIO = 2 ;**<br/>     | Impossible d’ouvrir le canal de sortie audio (est occupé). par exemple, parce qu’une autre application est en train de diffuser du contenu audio. |
| **const unsigned short** **audio \_ Status \_ USERSPEAKING = 3 ;**<br/>      | Le canal de sortie audio est occupé car le serveur traite l’entrée vocale de l’utilisateur                            |
| **const unsigned short** **audio \_ Status \_ CHARACTERSPEAKING = 4 ;**<br/> | Le canal de sortie audio est occupé car un caractère est actuellement en cours de discours.                                    |
| **const unsigned short** **audio \_ Status \_ SROVERRIDEABLE = 5 ;**<br/>    | Le canal de sortie audio n’est pas occupé, mais il attend une entrée vocale de l’utilisateur.                                 |
| erreur d’État audio **short non signé const** **\_ \_ = 6 ;**<br/>             | Un autre problème (inconnu) s’est produit lors de la tentative d’accès au canal de sortie audio.                       |



 

</dd> </dl>

Ce paramètre permet à votre application cliente d’interroger l’état du canal de sortie audio. Vous pouvez l’utiliser pour déterminer si votre caractère doit être parlant ou pour activer le mode d’écoute (à l’aide de **IAgentCharacterEx :: Listen**).

 

 





