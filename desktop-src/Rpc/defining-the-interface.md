---
title: Définition de l’interface
description: Une définition d’interface est une spécification formelle de la manière dont une application cliente et une application serveur communiquent entre elles.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- Appel de procédure distante RPC, tâches, définition de l’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f447847eeca39258b96ba129c46b3f7bcf054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028893"
---
# <a name="defining-the-interface"></a>Définition de l’interface

Une définition d’interface est une spécification formelle de la manière dont une application cliente et une application serveur communiquent entre elles. L’interface définit la façon dont le client et le serveur se reconnaissent mutuellement, les procédures distantes que l’application cliente peut appeler, ainsi que les types de données pour les paramètres et les valeurs de retour de ces procédures. Il spécifie également la manière dont les données sont transmises entre le client et le serveur.

Vous définissez cette interface dans le Microsoft Interface Definition Language (MIDL) qui se compose de définitions de langage C augmentées de mots clés, appelés attributs, qui décrivent comment les données sont transmises sur le réseau.

Le fichier de définition d’interface (IDL) contient des définitions de type, des attributs et des prototypes de fonction qui décrivent la manière dont les données sont transmises sur le réseau. Le fichier de configuration d’application (ACF) contient des attributs qui configurent votre application pour un environnement d’exploitation particulier sans affecter ses caractéristiques réseau.

 

 




