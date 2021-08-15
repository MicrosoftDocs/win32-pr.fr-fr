---
title: Prise en charge de la parole synthétisée
description: Prise en charge de la parole synthétisée
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c31fcb655ccb5a8fbb2ffbbb8d01d1da317209fbfa3e270a76d92208c06777df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475321"
---
# <a name="synthesized-speech-support"></a>Prise en charge de la parole synthétisée

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Si vous utilisez la synthèse vocale, votre caractère peut indiquer presque tout, ce qui offre la plus grande flexibilité. Avec l’audio enregistré, vous pouvez attribuer au caractère une voix spécifique ou unique. Pour spécifier la sortie, fournissez le texte parlé comme paramètre de la méthode [**Speak**](speak-method.md) .

Étant donné que l’architecture de Microsoft Agent utilise Microsoft SAPI pour la synthèse vocale synthétisée, vous pouvez utiliser n’importe quel moteur conforme à cette spécification et prend en charge la sortie de l’alphabet phonétique international (Loi) à l’aide de la méthode [**visuelle**](https://www.bing.com/search?q=**Visual**) de l’interface [**ITTSNotifySinkW**](ittsnotifysinkw.md) . Pour plus d’informations sur le moteur, consultez [spécifications de prise en charge du moteur de reconnaissance vocale](requirements-for-text-to-speech-engines.md).

Le paramètre ID de langue d’un caractère détermine sa sortie TTS. Si un client ne spécifie pas d’ID de langue pour le caractère, l’ID de langue du caractère est défini sur l’ID de langue par défaut de l’utilisateur. Si la définition du caractère comprend un moteur spécifique et que ce moteur peut être chargé et qu’il correspond au paramètre de langue du caractère, ce moteur est utilisé. Dans le cas contraire, Microsoft Agent énumère les autres moteurs disponibles et demande une meilleure correspondance SAPI en fonction de la langue, du sexe et de l’âge (dans cet ordre). Si aucun moteur correspondant n’est disponible, il n’y a pas de sortie TTS pour l’utilisation du caractère par le client. L’agent tente de charger le moteur TTS sur le premier appel [**Speak**](speak-method.md) ou lorsque vous interrogez ou définissez correctement son ID de mode.

Une application cliente peut également spécifier un moteur TTS pour son caractère (à l’aide de la propriété [**TTSModeID**](ttsmodeid-property.md) ). Cela remplace la tentative du serveur de trouver automatiquement un moteur correspondant en fonction de l’ID de mode TTS préféré du caractère ou du paramètre ID de langue actuel du caractère. Toutefois, si ce moteur n’est pas installé (ou ne peut pas être chargé autrement), l’appel échoue (et génère une erreur dans le contrôle). Le serveur tente alors de charger un autre moteur en fonction de l’ID de langue, du paramètre TTS de caractères compilés et des moteurs TTS disponibles. Si aucune correspondance n’est trouvée, TTS n’est pas disponible pour ce client, mais le caractère peut toujours parler dans sa bulle de mot.

Seuls les moteurs TTS en cours d’utilisation par un client restent chargés. Par exemple, si un caractère a une préférence définie pour un moteur spécifique et que le moteur est disponible, mais que votre application cliente a spécifié un moteur différent (en définissant l’ID de langue d’un caractère différemment du moteur ou en spécifiant un ID de mode différent), seul le moteur spécifié par votre application reste chargé. Le moteur correspondant à la préférence définie du caractère pour un paramètre TTS est déchargé (sauf si un autre client utilise le paramètre de moteur compilé du caractère).

 

 




