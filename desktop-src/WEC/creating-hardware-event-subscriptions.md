---
title: Création d’abonnements aux événements matériels
description: Sur les ordinateurs sur lesquels est installé un contrôleur de gestion de la carte de base (BMC), les événements matériels sont générés et consignés dans le journal des événements système (SEL), qui est le magasin d’événements du contrôleur BMC stocké dans la mémoire non volatile.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ee32d590143ed8a1ffacec6f59ad3b3094c2d2a22d0df66b0cb0d3521f83e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751111"
---
# <a name="creating-hardware-event-subscriptions"></a>Création d’abonnements aux événements matériels

Sur les ordinateurs sur lesquels est installé un contrôleur de gestion de la carte de base (BMC), les événements matériels sont générés et consignés dans le journal des événements système (SEL), qui est le magasin d’événements du contrôleur BMC stocké dans la mémoire non volatile. pour lire ces événements matériels sur Windows Server 2008 à l’aide de l’observateur d’événements, vous devez créer un abonnement aux événements. les abonnements aux événements matériels fonctionnent uniquement sur Windows Server 2008.

La procédure suivante définit comment créer l’abonnement aux événements SEL pour récupérer les événements matériels :

1.  Enregistrez le code XML suivant dans un fichier de .xml (dans cet exemple, le fichier est nommé Wsmanselrg.xml). Ce code XML définit l’abonnement.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  Créez un abonnement aux événements en exécutant la commande suivante dans une fenêtre d’invite de commandes (le programme Wecutil.exe se trouve dans le répertoire% SYSTEMROOT% \\ system32) :

     *<path> \\wsmanselrg.xml* de la ressource.

3.  Assurez-vous que l’abonnement est actif en exécutant la commande suivante dans une fenêtre d’invite de commandes :

    **Wecutil gr** *wsmanselrg*

Le BMC est un microcontrôleur attaché localement à un serveur. Les contrôleurs BMC ont des capteurs qui surveillent l’état physique du serveur et une connexion réseau distincte qui peut communiquer sur le réseau, même si le serveur est hors connexion. Vous avez accès aux données BMC via le fournisseur WMI de l’interface de gestion de plateforme intelligente (IPMI). Pour plus d’informations sur le fournisseur IPMI, consultez [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

Pour que l’abonnement à un événement fonctionne, le contrôleur BMC et le fournisseur IPMI doivent être installés sur l’ordinateur. pour les ordinateurs qui s’exécutent sur Windows Server 2008, le fournisseur IPMI est installé par défaut. Si le BMC n’est pas disponible, le pilote IPMI ne peut pas être installé et l’état d’exécution de l’abonnement affiche toujours une erreur (0x8004001-échec générique WMI).

 

 