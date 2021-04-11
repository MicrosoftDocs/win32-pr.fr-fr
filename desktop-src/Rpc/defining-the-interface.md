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
# <a name="defining-the-interface"></a><span data-ttu-id="c92dd-104">Définition de l’interface</span><span class="sxs-lookup"><span data-stu-id="c92dd-104">Defining the Interface</span></span>

<span data-ttu-id="c92dd-105">Une définition d’interface est une spécification formelle de la manière dont une application cliente et une application serveur communiquent entre elles.</span><span class="sxs-lookup"><span data-stu-id="c92dd-105">An interface definition is a formal specification for how a client application and a server application communicate with each other.</span></span> <span data-ttu-id="c92dd-106">L’interface définit la façon dont le client et le serveur se reconnaissent mutuellement, les procédures distantes que l’application cliente peut appeler, ainsi que les types de données pour les paramètres et les valeurs de retour de ces procédures.</span><span class="sxs-lookup"><span data-stu-id="c92dd-106">The interface defines how the client and server recognize each other, the remote procedures that the client application can call, and the data types for those procedures' parameters and return values.</span></span> <span data-ttu-id="c92dd-107">Il spécifie également la manière dont les données sont transmises entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="c92dd-107">It also specifies how the data is transmitted between client and server.</span></span>

<span data-ttu-id="c92dd-108">Vous définissez cette interface dans le Microsoft Interface Definition Language (MIDL) qui se compose de définitions de langage C augmentées de mots clés, appelés attributs, qui décrivent comment les données sont transmises sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="c92dd-108">You define this interface in the Microsoft Interface Definition Language (MIDL) which consists of C-language definitions augmented with keywords, called attributes, which describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="c92dd-109">Le fichier de définition d’interface (IDL) contient des définitions de type, des attributs et des prototypes de fonction qui décrivent la manière dont les données sont transmises sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="c92dd-109">The interface definition (IDL) file contains type definitions, attributes and function prototypes that describe how data is transmitted on the network.</span></span> <span data-ttu-id="c92dd-110">Le fichier de configuration d’application (ACF) contient des attributs qui configurent votre application pour un environnement d’exploitation particulier sans affecter ses caractéristiques réseau.</span><span class="sxs-lookup"><span data-stu-id="c92dd-110">The application configuration (ACF) file contains attributes that configure your application for a particular operating environment without affecting its network characteristics.</span></span>

 

 




