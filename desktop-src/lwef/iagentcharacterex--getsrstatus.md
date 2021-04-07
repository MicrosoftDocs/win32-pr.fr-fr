---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029024"
---
# <a name="iagentcharacterexgetsrstatus"></a>IAgentCharacterEx::GetSRStatus

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

Récupère l’état de la condition nécessaire pour prendre en charge l’entrée vocale.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Adresse d’une variable qui reçoit l’une des valeurs suivantes pour le paramètre d’État :



| Valeur                                                                               | Description                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| État d’écoute **longue non signée const** **\_ \_ CANLISTEN = 0 ;**<br/>               | Les conditions prennent en charge l’entrée vocale.                                                                                                                                                                                                          |
| **const unsigned long** **Listen \_ Status \_ noaudio = 1 ;**<br/>                 | Aucun périphérique d’entrée audio n’est disponible sur ce système. (Notez que cela ne détecte pas si un microphone est installé ; il peut détecter uniquement si l’utilisateur dispose d’une carte son compatible avec un pilote opérationnel.) |
| État d’écoute **longue non signée const** **\_ \_ NOTTOPMOST = 2 ;**<br/>              | Un autre client est le client actif de ce caractère, ou le caractère actuel n’est pas au premier plan.                                                                                                                                           |
| État d’écoute **longue non signée const** **\_ \_ CANTOPENAUDIO = 3 ;**<br/>           | Le canal d’entrée ou de sortie audio est actuellement occupé, mais une autre application utilise l’audio.                                                                                                                                               |
| État d’écoute **longue non signée const** **\_ \_ COULDNTINITIALIZESPEECH = 4 ;**<br/> | Une erreur non spécifiée s’est produite lors de l’initialisation du sous-système de reconnaissance vocale. Cela inclut la possibilité qu’aucun moteur vocal ne soit disponible correspondant au paramètre de langue du caractère.                          |
| État d’écoute **longue non signée const** **\_ \_ SPEECHDISABLED = 5 ;**<br/>          | L’utilisateur a désactivé l’entrée vocale dans la fenêtre Options de caractères avancés.                                                                                                                                                              |
| erreur d’état d’écoute **longue non signée const** **\_ \_ = 6 ;**<br/>                   | Une erreur s’est produite lors de la vérification de l’État audio, mais la cause de l’erreur n’a pas été retournée par le système.                                                                                                                                |



 

</dd> </dl>

Cette fonction vous permet d’interroger si les conditions actuelles prennent en charge l’entrée de reconnaissance vocale, y compris l’état du périphérique audio. Si votre application utilise la méthode [**IAgentCharacterEx :: Listen**](iagentcharacterex--listen.md) , vous pouvez utiliser cette fonction pour mieux garantir le bon fonctionnement de l’appel. L’appel de cette méthode charge également le moteur de reconnaissance vocale s’il n’est pas déjà chargé. Toutefois, il n’active pas le mode d’écoute.

Lorsque l’entrée vocale est activée dans la feuille de propriétés de l’agent (options de caractères avancés), l’interrogation de l’état chargera le moteur associé (s’il n’est pas déjà chargé) et démarrez Speech services. Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est affichable. (La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux.

Cette fonction retourne uniquement le paramètre de l’utilisation du caractère par l’application cliente ; le paramètre ne reflète pas les autres clients du caractère ou d’autres caractères de votre application cliente.

 

 





