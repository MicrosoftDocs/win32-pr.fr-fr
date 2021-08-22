---
title: Définition de l’interface
description: Une définition d’interface est une spécification formelle de la manière dont une application cliente et une application serveur communiquent entre elles.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- Appel de procédure distante RPC, tâches, définition de l’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654c6690e6980e659df8a68652aec59b296b7d88543eca02605f489a2c3a909c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930804"
---
# <a name="defining-the-interface"></a>Définition de l’interface

Une définition d’interface est une spécification formelle de la manière dont une application cliente et une application serveur communiquent entre elles. L’interface définit la façon dont le client et le serveur se reconnaissent mutuellement, les procédures distantes que l’application cliente peut appeler, ainsi que les types de données pour les paramètres et les valeurs de retour de ces procédures. Il spécifie également la manière dont les données sont transmises entre le client et le serveur.

Vous définissez cette interface dans le Microsoft Interface Definition Language (MIDL) qui se compose de définitions de langage C augmentées de mots clés, appelés attributs, qui décrivent comment les données sont transmises sur le réseau.

Le fichier de définition d’interface (IDL) contient des définitions de type, des attributs et des prototypes de fonction qui décrivent la manière dont les données sont transmises sur le réseau. Le fichier de configuration d’application (ACF) contient des attributs qui configurent votre application pour un environnement d’exploitation particulier sans affecter ses caractéristiques réseau.

 

 




