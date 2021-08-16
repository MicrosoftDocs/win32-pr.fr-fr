---
title: Mise à jour à partir de la version précédente
description: Mise à jour à partir de la version précédente
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de894f220db7ee09847a8fa767e1f99c38cee8014cb86b65c1251e0579eaabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745722"
---
# <a name="updating-from-previous-version"></a>Mise à jour à partir de la version précédente

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Les applications générées et compilées avec la version 1,5 précédente de Microsoft Agent doivent s’exécuter sans modification sous la nouvelle version 2,0. La propriété [**Connected**](connected-property.md) ne peut plus avoir la valeur **false**; certaines propriétés de l’objet SpeechInput qui ont été remplacées existent toujours, mais ne transforment plus les valeurs et le serveur ne déclenche plus les événements de [**redémarrage**](https://www.bing.com/search?q=**Restart**) et d' [**arrêt**](https://www.bing.com/search?q=**Shutdown**) .

Toutefois, si vous mettez à jour vos applications pour utiliser le contrôle de l’agent 2,0, vous devrez peut-être modifier votre code. si vous avez installé la version 2,0 de Microsoft agent et que vous chargez un projet Visual Basic utilisez la version antérieure du contrôle de l’agent, Visual Basic comprend une option qui affiche automatiquement un message indiquant qu’il a détecté une nouvelle version du contrôle. Pour garantir le bon fonctionnement de votre application, choisissez toujours d’utiliser la version la plus récente.

pour d’autres langages de programmation (tels que Microsoft Office 97 VBA), pour mettre à jour le contrôle, vous devrez peut-être d’abord supprimer le contrôle de l’Agent 1,5 et enregistrer votre code. Ensuite, quittez l’environnement de programmation, redémarrez l’environnement de programmation, rechargez votre code et insérez le nouveau contrôle. Évitez de modifier une application compatible agent 2,0 dans la même instance de l’environnement de programmation que vous modifiez une application agent 1,5 dans. Certains environnements de programmation peuvent ne pas gérer les différences entre les deux versions des contrôles.

Vous devez être en mesure de désinstaller l’agent 1,5 sur votre système après l’installation de la version de l’agent 2,0. Toutefois, si l’agent 1,5 est installé sur la version 2,0, vous devrez peut-être réinstaller 2,0.

 

 




