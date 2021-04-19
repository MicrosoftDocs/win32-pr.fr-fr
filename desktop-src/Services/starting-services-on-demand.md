---
description: L’utilisateur peut démarrer un service à l’aide de l’utilitaire panneau de configuration des services. L’utilisateur peut spécifier des arguments pour le service dans le champ paramètres de démarrage. Un programme de contrôle de service peut démarrer un service et spécifier ses arguments avec la fonction StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Démarrage des services à la demande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521949"
---
# <a name="starting-services-on-demand"></a>Démarrage des services à la demande

L’utilisateur peut démarrer un service à l’aide de l’utilitaire panneau de configuration des services. L’utilisateur peut spécifier des arguments pour le service dans le champ **paramètres de démarrage** . Un programme de contrôle de service peut démarrer un service et spécifier ses arguments avec la fonction [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .

Lorsque le service est démarré, le SCM effectue les étapes suivantes :

-   Récupérez les informations de compte stockées dans la base de données.
-   Connectez-vous au compte de service.
-   Chargez le profil utilisateur.
-   Créez le service dans l’état suspendu.
-   Attribuez le jeton d’ouverture de session au processus.
-   Autorisez l’exécution du processus.

 

 



