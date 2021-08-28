---
description: le capteur de Windows et la plateforme d’emplacement incluent des paramètres de confidentialité pour aider à protéger les informations personnelles des utilisateurs.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: confidentialité et sécurité dans le capteur Windows et la plateforme d’emplacement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5f2109b3f581e48537c135444dae2afa8cb20582fbc559da01809d77e11e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666969"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a>confidentialité et sécurité dans le capteur Windows et la plateforme d’emplacement

le capteur de Windows et la plateforme d’emplacement incluent des paramètres de confidentialité pour aider à protéger les informations personnelles des utilisateurs.

La plateforme permet de s’assurer que les données de capteur restent privées, lorsque la confidentialité est requise, de l’une des manières suivantes :

-   Par défaut, les capteurs sont désactivés. Étant donné que la conception de la plateforme suppose que tous les capteurs peuvent fournir des données personnelles, chaque capteur est désactivé jusqu’à ce que l’utilisateur fournisse un consentement explicite pour accéder aux données de capteur.
-   Windows fournit des messages de divulgation et des informations d’aide pour l’utilisateur. Ce contenu aide les utilisateurs à comprendre comment les capteurs peuvent affecter la confidentialité de leurs données personnelles et aide les utilisateurs à prendre des décisions avisées.
-   L’autorisation d’un capteur nécessite des droits d’administrateur.
-   Lorsqu’il est activé, un périphérique de capteur fonctionne pour tous les programmes s’exécutant sous un compte d’utilisateur particulier (ou pour tous les comptes d’utilisateur). Cela comprend les utilisateurs et les services non interactifs, tels que ASPNET ou SYSTEM. Par exemple, si vous activez un capteur GPS pour votre compte d’utilisateur, seuls les programmes qui s’exécutent sous votre compte d’utilisateur ont accès au GPS. Si vous activez le GPS pour tous les utilisateurs, tout programme s’exécutant sous n’importe quel compte d’utilisateur a accès au GPS.
-   Les programmes qui utilisent des capteurs peuvent appeler une méthode pour ouvrir une boîte de dialogue système qui invite les utilisateurs à activer les périphériques de capteur nécessaires. Cette fonctionnalité permet aux développeurs et aux utilisateurs de s’assurer que les capteurs fonctionnent quand les programmes en ont besoin, tout en conservant le contrôle de la divulgation des données de capteur par l’utilisateur.
-   Les pilotes de capteur utilisent un objet spécial qui traite toutes les demandes d’e/s. Cet objet permet de s’assurer que seuls les programmes qui disposent de l’autorisation utilisateur peuvent accéder aux données de capteur.

 

 



