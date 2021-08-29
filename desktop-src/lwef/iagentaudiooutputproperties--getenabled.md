---
title: IAgentAudioOutputProperties GetEnabled
description: IAgentAudioOutputProperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8f5247a767f82a66920f4c27b48d33044336d5b6d179b68587b06c95c2b502
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062039"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a>IAgentAudioOutputProperties :: GetEnabled

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

Récupère une valeur indiquant si la sortie vocale des caractères est activée.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Adresse d’une variable qui reçoit la **valeur true** si la sortie vocale est actuellement activée et **false** si elle est désactivée.

</dd> </dl>

Étant donné que ce paramètre affecte la sortie orale (TTS et fichier audio) pour tous les caractères, seul l’utilisateur peut modifier cette propriété dans la feuille de propriétés de l’agent Microsoft.

 

 




