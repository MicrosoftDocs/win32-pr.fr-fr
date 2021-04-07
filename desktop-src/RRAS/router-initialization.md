---
title: Initialisation du routeur
description: Les informations de configuration pour le routeur, les gestionnaires de routeur et les protocoles/clients de routage sont divisées en informations globales et par interface et sont stockées dans le registre et le fichier d’annuaire téléphonique du routeur, Router. pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- routeurs RRAS, initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670898"
---
# <a name="router-initialization"></a>Initialisation du routeur

Les informations de configuration pour le routeur, les gestionnaires de routeur et les protocoles/clients de routage sont divisées en informations globales et par interface et sont stockées dans le registre et le fichier d’annuaire téléphonique du routeur, Router. pbk.

Au démarrage du processus de routeur, DIM (gestionnaire d’interface dynamique) lit la configuration du routeur à partir du Registre. DIM crée les interfaces qui sont spécifiées par les informations d’interface.

DIM récupère également les informations globales du gestionnaire de routage. DIM démarre les gestionnaires de routeur qui correspondent à ces informations et leur transmet les informations. Par exemple, si DIM trouve des informations globales pour le gestionnaire de routeur IP dans le registre, DIM démarre le gestionnaire de routeur IP et lui transmet les informations globales. Si aucune information globale n’est présente dans le registre pour un gestionnaire de routage particulier, DIM ne démarre pas ce gestionnaire de routeur.

Les gestionnaires de routeur examinent les informations globales reçues de DIM. Si le gestionnaire de routeur trouve des informations spécifiques à un client particulier dans les informations globales, il charge la DLL du client (par exemple IpNAT.dll) et initialise le client en appelant les fonctions [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) et [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) du client. Le gestionnaire de routeur transmet les informations globales spécifiques au client au client lors de l’appel à [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).

À chaque étape, les informations transmises à l’entité suivante sont opaques pour l’entité qui le précède. Autrement dit, DIM n’interprète pas les informations globales pour le gestionnaire de routeur IP, au-delà du fait que les informations sont destinées au gestionnaire de routeur IP. De même, le gestionnaire de routeur IP n’interprète pas les informations spécifiques au protocole OSPF au-delà du fait qu’il s’agit d’informations OSPF.

 

 




