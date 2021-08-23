---
title: Connexion du client et du serveur
description: Pour communiquer, les programmes clients et serveurs doivent établir une session de communication sur le réseau ou les réseaux qui les connectent.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Appel de procédure distante RPC, tâches, connexion du client et du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f477802ffb4b72f33ce951bf811b1cb9b770a8272f646507dfaa450934569f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931226"
---
# <a name="connecting-the-client-and-the-server"></a>Connexion du client et du serveur

Pour communiquer, les programmes clients et serveurs doivent établir une session de communication sur le réseau ou les réseaux qui les connectent. Une fois la connexion établie, le client peut appeler des procédures distantes dans le programme serveur comme si elles étaient locales pour le programme client.

Cette section fournit une vue d’ensemble conceptuelle de l’établissement d’une connexion entre les clients et les serveurs pour les appels de procédure distante. Il ne fournit pas de description détaillée de cette rubrique. Tous les concepts de cette section sont présentés en détail dans les chapitres ultérieurs et dans la section Référence des fonctions RPC.

La discussion présentée dans cette section est composée des rubriques suivantes :

-   [Terminologie des liaisons RPC essentielles](essential-rpc-binding-terminology.md)
-   [Préparation d’une connexion par le serveur](how-the-server-prepares-for-a-connection.md)
-   [Comment le client établit une connexion](how-the-client-establishes-a-connection.md)

Notez que la discussion suppose des handles de liaison explicites. Toutefois, si votre application utilise d’autres types de descripteurs de liaison, vous devrez peut-être modifier les étapes présentées dans cette section. Pour plus d’informations, consultez [liaison et Handles](binding-and-handles.md).

 

 




