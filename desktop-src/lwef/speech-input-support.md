---
title: Prise en charge des entrées vocales
description: Prise en charge des entrées vocales
ms.assetid: 4702b941-fcc9-4d00-aba2-eca624b6d417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd777f5dca0df91a4660249b0cdda380f2f20c37ba5c1c38a04264bb871ab3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746250"
---
# <a name="speech-input-support"></a>Prise en charge des entrées vocales

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Outre la prise en charge de l’interaction de la souris et du clavier, Microsoft Agent offre une prise en charge directe des entrées vocales. Étant donné que la prise en charge de l’entrée vocale par Microsoft Agent est basée sur Microsoft SAPI (Speech Application Programming Interface), vous pouvez utiliser Microsoft Agent avec la commande de reconnaissance vocale et les moteurs de contrôle qui incluent la prise en charge de SAPI-required. Pour plus d’informations sur la configuration requise du moteur de reconnaissance vocale, consultez [spécifications de prise en charge du moteur vocal](requirements-for-speech-recognition-engines.md).

Microsoft fournit un moteur de reconnaissance vocale de contrôle et de commande que vous pouvez utiliser avec Microsoft Agent. Pour plus d’informations, consultez [sélection du moteur de reconnaissance vocale](speech-engine-selection.md).

L’utilisateur peut lancer des entrées vocales en appuyant sur le raccourci d’écoute Push-to-débats et en le maintenant enfoncé. Dans ce mode d’écoute, si le moteur de reconnaissance vocale reçoit le début de l’entrée parlée, il maintient le canal audio ouvert jusqu’à ce qu’il détecte la fin de l’énoncé. Toutefois, lorsqu’il ne reçoit pas d’entrée, il ne bloque pas la sortie audio. Cela permet à l’utilisateur d’émettre plusieurs commandes vocales tout en maintenant la touche enfoncée, et le caractère peut répondre lorsque l’utilisateur n’est pas en train de parler.

Le mode d’écoute expire une fois que l’utilisateur relâche la touche d’écoute. L’utilisateur peut ajuster le délai d’expiration pour ce mode à l’aide des options de caractères avancés. Vous ne pouvez pas définir ce délai d’attente à partir du code de votre application cliente.

Si un caractère tente de parler pendant que l’utilisateur parle, la sortie audible du caractère échoue bien que le texte puisse toujours s’afficher dans sa bulle de mot. Si le caractère est le canal audio pendant que la touche d’écoute est enfoncée, le serveur transfère automatiquement le contrôle à l’utilisateur après le traitement du texte dans la méthode [**Speak**](speak-method.md) . Un ton MIDI facultatif est joué pour signaler à l’utilisateur de commencer à parler. Cela permet à l’utilisateur de fournir une entrée même si l’application qui pilote le caractère n’a pas pu fournir des pauses logiques dans sa sortie.

Vous pouvez également utiliser la méthode [**Listen**](listen-method.md) pour initier une entrée vocale. L’appel de cette méthode active la reconnaissance vocale pour une période prédéfinie. S’il n’y a aucune entrée au cours de cet intervalle, Microsoft Agent désactive automatiquement le moteur de reconnaissance vocale et libère le canal audio. Cela évite le blocage de l’entrée ou de la sortie du périphérique audio et minimise la surcharge du processeur que la reconnaissance vocale utilise lorsqu’elle est activée. Vous pouvez également utiliser la méthode **Listen** pour désactiver l’entrée vocale. Toutefois, gardez à l’esprit que, étant donné que le moteur de reconnaissance vocale fonctionne de façon asynchrone, l’effet peut ne pas être immédiat. Par conséquent, il est possible de recevoir un événement de [**commande**](command-event.md) même après que votre code a appelé **Listen** pour désactiver l’entrée vocale.

Pour prendre en charge l’entrée vocale, vous définissez une *grammaire*, un ensemble de mots que le moteur de reconnaissance vocale doit écouter et faire correspondre comme paramètre **vocal** pour une [**commande**](/windows/desktop/lwef/the-command-object) dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) . Vous pouvez inclure des mots facultatifs et alternatifs et des séquences répétées dans votre grammaire. Notez que l’agent n’active pas la touche d’accès rapide d’écoute tant que l’un de ses clients n’a pas chargé avec succès un moteur de reconnaissance vocale ou a créé une **voix** pour l’un de ses objets de **commande** .

Que l’utilisateur appuie sur la touche d’écoute ou que votre application cliente appelle la méthode [**Listen**](listen-method.md) pour initier l’entrée vocale, le moteur de reconnaissance vocale tente de faire correspondre l’entrée d’un énoncé d’énoncé à la grammaire pour les commandes qui ont été définies et transmet les informations au serveur. Le serveur notifie ensuite l’application cliente à l’aide de l’événement de [**commande**](command-event.md) ([**IAgentNotifySink :: Command**](iagentnotifysink--command.md)); retour de l’objet [**UserInput**](/windows/desktop/lwef/iagentuserinput) qui comprend l’ID de commande de la meilleure correspondance et les deux autres correspondances (le cas échéant), un score de confiance et le texte correspondant pour chaque correspondance.

Le serveur signale également à votre application cliente qu’elle met en correspondance l’entrée vocale avec l’une des commandes fournies. Si l’ID de commande est **null**, vous obtenez toujours le score de confiance et le texte correspondant. En mode d’écoute, le serveur lit automatiquement l’animation assignée à l’état d' **écoute** du caractère. Ensuite, lorsqu’un énoncé est effectivement détecté, le serveur lit l’animation de l’état **auditif** du caractère. Le serveur conserve le caractère dans un état précis jusqu’à la fin de l’énoncé. Cela fournit les commentaires sociaux appropriés pour signaler à l’utilisateur l’entrée.

Si l’utilisateur désactive l’entrée vocale dans les options de caractères avancées, la touche d’écoute est également désactivée. De même, toute tentative d’appel de la méthode [**Listen**](listen-method.md) lorsque l’entrée vocale est désactivée entraîne l’échec de la méthode.

 

 