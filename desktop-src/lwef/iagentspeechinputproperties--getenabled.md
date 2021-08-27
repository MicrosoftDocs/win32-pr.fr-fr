---
title: IAgentSpeechInputProperties GetEnabled
description: IAgentSpeechInputProperties GetEnabled
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404bd6f0348487c8e039c247f5a9368359133be9e3df76b884115679a2961a97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114669"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a>IAgentSpeechInputProperties :: GetEnabled

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

Récupère une valeur indiquant si le moteur de reconnaissance vocale installé est activé.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Adresse d’une variable qui reçoit la **valeur true** si le moteur de reconnaissance vocale est actuellement activé et **false** s’il est désactivé.

</dd> </dl>

 

 




