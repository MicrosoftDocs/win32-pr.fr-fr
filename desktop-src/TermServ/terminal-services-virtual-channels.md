---
title: Services Bureau à distance des canaux virtuels
description: Les canaux virtuels sont des extensions logicielles qui peuvent être utilisées pour ajouter des améliorations fonctionnelles à une application Services Bureau à distance.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309890"
---
# <a name="remote-desktop-services-virtual-channels"></a>Services Bureau à distance des canaux virtuels

Les *canaux virtuels* sont des extensions logicielles qui peuvent être utilisées pour ajouter des améliorations fonctionnelles à une application services Bureau à distance. Parmi les exemples d’améliorations fonctionnelles, citons notamment la prise en charge de types spéciaux de matériel, de son ou d’autres ajouts à la fonctionnalité de base fournie par le Services Bureau à distance [protocole RDP (Remote Desktop Protocol)](remote-desktop-protocol.md) (RDP). Le protocole RDP offre une gestion multiplexée de plusieurs canaux virtuels.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Utilisation de Services Bureau à distance canaux virtuels](using-terminal-services-virtual-channels.md)
</dt> <dd>

Pour implémenter un canal virtuel, vous fournissez les modules serveur et client de l’application d’un canal virtuel.

</dd> <dt>

[Référence des canaux virtuels dynamiques](dynamic-virtual-channels-reference.md)
</dt> <dd>

Les interfaces clientes de canal virtuel dynamique (DVC) sont prises en charge par Services Bureau à distance.

</dd> <dt>

[Informations de référence sur les canaux virtuels Graphics](graphics-virtual-channels-reference.md)
</dt> <dd>

Les informations de référence sur les canaux virtuels Graphics contiennent des éléments de programmation qui vous permettent de créer un canal graphique virtuel.

</dd> </dl>

Une application de canal virtuel a deux parties : un module client et un module serveur. Le module de serveur est un programme exécutable s’exécutant sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Le module client est une DLL qui doit être chargée en mémoire sur l’ordinateur client lors de l’exécution du programme client Connexion Bureau à distance (RDC).

Les canaux virtuels peuvent ajouter des améliorations fonctionnelles à un client Connexion Bureau à distance (RDC), indépendamment du protocole RDP. Avec la prise en charge des canaux virtuels, de nouvelles fonctionnalités peuvent être ajoutées sans avoir à mettre à jour le logiciel client ou serveur, ni le protocole RDP.

Quatre grandes classes d’utilisateurs de canaux virtuels ont été identifiées :

-   Pilotes généraux en mode noyau, tels que les pilotes série ou d’imprimante.
-   Redirection du système de fichiers (il s’agit simplement d’un cas particulier d’un pilote en mode noyau général).
-   Applications en mode utilisateur, par exemple, couper-coller à distance.
-   Périphériques audio.

Pour plus d’informations, consultez [utilisation de services Bureau à distance canaux virtuels](using-terminal-services-virtual-channels.md).

Si vous avez activé une application de canaux virtuels dans votre déploiement Services Bureau à distance, vous pouvez rendre l’application accessible aux ordinateurs clients qui accèdent au serveur hôte de session Bureau à distance à l’aide de l’Bureau à distance contrôle Microsoft ActiveX. Pour plus d’informations, consultez [canaux virtuels scriptables](scriptable-virtual-channels.md) et [utilisation du contrôle ActiveX Bureau à distance avec des canaux virtuels](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




