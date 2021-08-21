---
title: Empêcher plusieurs chargements
description: Lorsque vous téléchargez un fichier, le service BITS crée un ID de session qui identifie la session de téléchargement sur le client BITS et le serveur BITS.
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c08555acf8bcdc99576675b0ec5852f322f7b37fea9821f3f0156352a29b61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701699"
---
# <a name="preventing-multiple-uploads"></a>Empêcher plusieurs chargements

Lorsque vous téléchargez un fichier, le service BITS crée un ID de session qui identifie la session de téléchargement sur le client BITS et le serveur BITS. Si la connexion entre le client BITS et le serveur est interrompue pendant que BITS charge un fichier, le client utilise l’ID de session pour tenter de reprendre le téléchargement.

Si le client BITS se connecte au même serveur qu’auparavant, le serveur reconnaîtra l’ID de session et le chargement reprendra à partir du point d’interruption. Toutefois, si le client se connecte à un autre serveur, le client doit démarrer le téléchargement depuis le début, car le nouveau serveur n’a pas le contexte de session ou les données précédemment chargées. BITS peut se connecter à un autre serveur lorsque le serveur BITS est hébergé sur une batterie de serveurs Web et que la propriété d’extension IIS BITS, [BITSHostId](bits-iis-extension-properties.md), n’est pas définie. La propriété BITSHostId empêche le redémarrage en forçant le client BITS à se connecter à l’adresse unique du serveur précédent au lieu de l’adresse du serveur partagé.

Le serveur BITS tentera d’envoyer le fichier de téléchargement une seule fois à l’application serveur, mais il est possible que le fichier soit envoyé plusieurs fois. Cela peut se produire, par exemple, si le serveur BITS envoie le fichier à l’application serveur, puis se termine en attendant la réponse de l’application serveur. Le client BITS reçoit un code d’erreur de la couche HTTP et réessaie le chargement après un certain délai. Si le serveur reste hors connexion pendant une durée plus longue que le délai d’expiration de [BITSHostIdFallbackTimeout](bits-iis-extension-properties.md) , le client envoie à nouveau la requête à l’adresse du serveur partagé. un autre serveur BITS recevra le fichier et le remetra à nouveau à l’application serveur.

Un même cas de figure peut se produire même avec un serveur frontal unique. Par exemple, lorsque le client a téléchargé la totalité du fichier sur le serveur, le bloc final fait en sorte que le serveur transfère le fichier à l’application serveur. Si le serveur BITS ou l’application serveur se termine après le traitement du fichier mais avant que l’accusé de réception ne soit envoyé au client, le client recevra un code d’erreur et réessaiera ultérieurement. Lorsque le client effectue une nouvelle tentative, le serveur BITS voit que le dernier bloc a été chargé, et il transfère à nouveau le fichier à l’application serveur. Si la réception du fichier de téléchargement à plusieurs moments est un problème pour votre application serveur, vous devez envisager d’inclure un identificateur de transaction dans les données.

 

 




