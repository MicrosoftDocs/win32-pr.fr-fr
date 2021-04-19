---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511046"
---
# <a name="iagentcharactergetttspitch"></a>IAgentCharacter::GetTTSPitch

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

Récupère le paramètre de tonalité de sortie TTS du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*
</dt> <dd>

Adresse d’une variable qui reçoit la valeur actuelle de l’espace de synthèse vocale du caractère en Hertz.

</dd> </dl>

Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure des balises de hauteur dans votre texte de sortie, ce qui augmentera temporairement le pas pour une énoncé particulière. Cette méthode s’applique uniquement aux caractères configurés pour la sortie TTS. Si le moteur de synthèse vocale (TTS) n’est pas activé (ou installé) ou si le caractère ne prend pas en charge la sortie TTS, cette méthode retourne zéro (0).

 

 




