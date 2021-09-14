---
title: Vérifier que le serveur est Qui il prétend être
description: Il est préférable d’utiliser l’authentification mutuelle et, par conséquent, de vérifier l’identité du serveur.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118973"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a>Vérifier que le serveur est Qui il prétend être

Il est préférable d’utiliser l’authentification mutuelle et, par conséquent, de vérifier l’identité du serveur. Voici un exemple d’erreur courante qui ne parvient pas à effectuer cette opération : les applications qui ont un service local dans lequel les clients appellent. Dans certaines configurations, un administrateur peut décider que le service système n’est pas vraiment utile et peut choisir de l’arrêter. Une personne malveillante inventif sur un ordinateur Terminal Server peut lancer un processus qui écoute sur le même point de terminaison, et lorsqu’un client se connecte à un point de terminaison, autorisant l’emprunt d’identité sur le serveur sans authentification mutuelle du serveur, l’attaquant peut emprunter l’identité du client et accéder aux données du client, ou effectuer des appels réseau pour le compte du client. La plupart des services système s’exécutent sous un compte bien connu, tel que LocalSysyem, LocalService ou NetworkService, qui peut être vérifié à l’aide de l’authentification mutuelle.

 

 




