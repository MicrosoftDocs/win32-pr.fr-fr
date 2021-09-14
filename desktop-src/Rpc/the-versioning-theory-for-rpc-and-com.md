---
title: La théorie de la gestion des versions pour RPC et COM
description: Théorie de la gestion des versions pour l’appel de procédure distante (RPC) et COM.
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- RPC appel de procédure distante, meilleures pratiques, contrôle de version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b23c91bf69fbc3c4f72366b80812fd54330d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194031"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>La théorie de la gestion des versions pour RPC et COM

Seules deux méthodes entièrement infaillibles prennent en charge de nouvelles fonctionnalités sans risque de problèmes de compatibilité de câble :

-   Modifiez la version de l’interface en fonction des règles. Cela empêche les nouveaux clients de communiquer avec un ancien serveur et peut ou non empêcher un ancien client de communiquer avec le nouveau serveur. Cela est clarifié plus loin dans cette section.
-   Introduisez une autre interface pour traiter les nouvelles fonctionnalités.

Une interface RPC standard est identifiée par un GUID et une combinaison de numéros de version ; une interface COM est identifiée par son GUID. La version comprend des parties majeures et secondaires. Pour les interfaces standard avec le même GUID et les numéros de version différents, une connexion est possible uniquement lorsque la version principale est la même, et que le client n’est pas supérieur à la version mineure du serveur.

En conséquence, la modification du GUID de l’interface RPC interrompt la compatibilité des câbles, contrairement à la modification du nom de l’interface.

Dans le protocole RPC standard, un chemin d’accès pour les mises à niveau et les extensions est bien défini, et requiert essentiellement que de nouvelles méthodes soient ajoutées à la fin de l’interface et que les nouveaux types soient utilisés uniquement dans les nouvelles méthodes. Si de tels ajouts sont nécessaires, la version mineure doit être augmentée. Toute autre modification nécessite une modification de la version principale, car le logiciel client et serveur est incompatible avec le réseau. L’adhésion à ces règles garantit qu’à chaque connexion entre un nouveau client et un ancien serveur, ou vice versa, les deux côtés sont entièrement compatibles.

Pour une interface COM, l’attribut version ne peut pas être utilisé. La création d’interfaces et l’héritage des anciennes interfaces revient à manipuler la version dans RPC. En général, la meilleure approche dans COM consiste à créer une nouvelle interface pour les fonctionnalités étendues. L’équivalent de la version mineure est la nouvelle interface qui hérite de l’ancienne. La modification d’anciennes méthodes ou de types de données anciens requiert une interface COM entièrement nouvelle, c’est-à-dire une interface qui n’hérite pas de l’ancienne.

Pour COM, la fonction [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) est une méthode établie permettant de vérifier si un serveur prend en charge une interface ; par conséquent, les situations où un client peut communiquer avec une ancienne et une nouvelle version d’une interface peuvent être facilement résolues.

 

 