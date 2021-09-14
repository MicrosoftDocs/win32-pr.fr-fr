---
title: IAgentSpeechInputProperties GetEnabled
description: IAgentSpeechInputProperties GetEnabled
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95613398bf79b2446d2bc572864f69ad1ad92ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291947"
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

 

 




