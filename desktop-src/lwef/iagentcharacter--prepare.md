---
title: Préparer IAgentCharacter
description: Préparer IAgentCharacter
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebee8d2ea99c8782e9506e0e4a812cfb277487
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031206"
---
# <a name="iagentcharacterprepare"></a>IAgentCharacter ::P la même parenthèse

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

Récupère les données d’animation d’un caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi. Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.

<dl> <dt>

<span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*
</dt> <dd>

Valeur qui indique le type de données d’animation à charger qui doit être l’un des éléments suivants :



| Valeur                                                           | Description                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| **const non signed Short** **Prepare \_ animation = 0 ;**<br/> | Données d’animation d’un caractère.                              |
| **const non signé Short** **Prepare \_ State = 1 ;**<br/>     | Données d’état d’un caractère.                                  |
| **const non signé Short** **Prepare \_ Wave = 2**<br/>       | Fichier son d’un caractère (. WAV ou. LWV) pour la sortie parlée. |



 

</dd> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

Nom de l’animation ou de l’État.

Le nom de l’animation est basé sur celui défini pour le caractère lorsqu’il a été enregistré à l’aide de l’éditeur de caractères Microsoft Agent.

Pour les États, la valeur peut être l’une des suivantes :



|                      |                                                 |
|----------------------|-------------------------------------------------|
| **"Gesturing"**      | Pour récupérer toutes les animations d’état **gesturing** . |
| **"GesturingDown"**  | Pour récupérer les animations **GesturingDown** .       |
| **"GesturingLeft"**  | Pour récupérer les animations **GesturingLeft** .       |
| **"GesturingRight"** | Pour récupérer les animations **GesturingRight** .      |
| **"GesturingUp"**    | Pour récupérer les animations **GesturingUp** .         |
| **Masquage**         | Pour récupérer les animations d’état de **masquage** .    |
| **Entendre**        | Pour récupérer les animations d’état **auditif** .   |
| **Tournant**         | Pour récupérer toutes les animations d’état de **ralenti** .    |
| **"IdlingLevel1"**   | Pour récupérer toutes les animations **IdlingLevel1** .    |
| **"IdlingLevel2"**   | Pour récupérer toutes les animations **IdlingLevel2** .    |
| **"IdlingLevel3"**   | Pour récupérer toutes les animations **IdlingLevel3** .    |
| **Listen**      | Pour récupérer les animations d’état d' **écoute** . |
| **Passer**         | Pour récupérer toutes les animations d’état de **déplacement** .    |
| **"MovingDown"**     | Pour récupérer toutes les animations **mobiles** .          |
| **"MovingLeft"**     | Pour récupérer toutes les animations **MovingLeft** .      |
| **"MovingRight"**    | Pour récupérer toutes les animations **MovingRight** .     |
| **"MovingUp"**       | Pour récupérer toutes les animations **MovingUp** .        |
| **Proposant**        | Pour récupérer les animations d’état d' **émission** .   |
| **Parlez**       | Pour récupérer les animations d’état de **conversation** .  |



 

Pour. Fichiers WAV, définissez *bszName* sur l’URL ou la spécification de fichier pour le. Fichier WAV. Si la spécification n’est pas terminée, elle est interprétée comme étant relative à la spécification utilisée dans la méthode [**Load**](https://www.bing.com/search?q=**Load**) .

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*
</dt> <dd>

Valeur booléenne qui spécifie si le serveur met en file d’attente la demande de [**préparation**](/windows/desktop/lwef/iagentcharacter--prepare) . **True** met la demande en file d’attente et provoque le chargement des requêtes d’animation qui le suivent jusqu’à ce que les données d’animation qu’elle spécifient soient chargées. **False** récupère les données d’animation de manière asynchrone.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de la demande de [**préparation**](/windows/desktop/lwef/iagentcharacter--prepare) .

</dd> </dl>

Si vous chargez un caractère à l’aide du protocole HTTP (. Fichier ACF), vous devez utiliser la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour récupérer des données d’animation avant de pouvoir lire l’animation. Vous ne pouvez pas utiliser cette méthode si vous avez chargé le caractère à l’aide du protocole UNC (un. Fichier ACS). Vous ne pouvez pas non plus récupérer les données HTTP d’un caractère à l’aide de **Prepare** si vous avez chargé ce caractère à l’aide du protocole UNC (. Fichier de caractères ACS).

Les données audio ou d’animation récupérées avec la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) sont stockées dans le cache du navigateur. Les appels suivants vérifient le cache et, si les données d’animation y sont déjà, le contrôle charge les données directement à partir du cache. Une fois chargées, les données de l’animation ou du son peuvent être lues avec les méthodes [**Play**](/windows/desktop/lwef/iagentcharacter--play) ou [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .

Vous pouvez spécifier plusieurs animations et États en les séparant par des virgules. Toutefois, vous ne pouvez pas mélanger des types dans la même instruction [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .

 

