---
title: Création d’abonnements aux événements matériels
description: Sur les ordinateurs sur lesquels est installé un contrôleur de gestion de la carte de base (BMC), les événements matériels sont générés et consignés dans le journal des événements système (SEL), qui est le magasin d’événements du contrôleur BMC stocké dans la mémoire non volatile.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5f904e74d1f29b0666c9cb02b13689a0633bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315917"
---
# <a name="creating-hardware-event-subscriptions"></a><span data-ttu-id="8becb-103">Création d’abonnements aux événements matériels</span><span class="sxs-lookup"><span data-stu-id="8becb-103">Creating Hardware Event Subscriptions</span></span>

<span data-ttu-id="8becb-104">Sur les ordinateurs sur lesquels est installé un contrôleur de gestion de la carte de base (BMC), les événements matériels sont générés et consignés dans le journal des événements système (SEL), qui est le magasin d’événements du contrôleur BMC stocké dans la mémoire non volatile.</span><span class="sxs-lookup"><span data-stu-id="8becb-104">On computers that have a Baseboard Management Controller (BMC) installed, hardware events are raised and logged in the System event log (SEL), which is the BMC event store that is stored in nonvolatile memory.</span></span> <span data-ttu-id="8becb-105">Pour lire ces événements matériels sur Windows Server 2008 à l’aide de l’observateur d’événements, vous devez créer un abonnement aux événements.</span><span class="sxs-lookup"><span data-stu-id="8becb-105">To read these hardware events on Windows Server 2008 using the Event Viewer, you must create a subscription to the events.</span></span> <span data-ttu-id="8becb-106">Les abonnements aux événements matériels ne fonctionneront que sur Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8becb-106">The hardware event subscriptions will only work on Windows Server 2008.</span></span>

<span data-ttu-id="8becb-107">La procédure suivante définit comment créer l’abonnement aux événements SEL pour récupérer les événements matériels :</span><span class="sxs-lookup"><span data-stu-id="8becb-107">The following procedure defines how to create the SEL event subscription to retrieve the hardware events:</span></span>

1.  <span data-ttu-id="8becb-108">Enregistrez le code XML suivant dans un fichier. XML (dans cet exemple, le fichier est nommé Wsmanselrg.xml).</span><span class="sxs-lookup"><span data-stu-id="8becb-108">Save the following XML in an .xml file (in this example the file is named Wsmanselrg.xml).</span></span> <span data-ttu-id="8becb-109">Ce code XML définit l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8becb-109">This XML defines the subscription.</span></span>

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

    

2.  <span data-ttu-id="8becb-110">Créez un abonnement aux événements en exécutant la commande suivante dans une fenêtre d’invite de commandes (le programme Wecutil.exe se trouve dans le répertoire% SYSTEMROOT% \\ system32) :</span><span class="sxs-lookup"><span data-stu-id="8becb-110">Create an event subscription by executing the following command in a command prompt window (the Wecutil.exe program is located in the %SYSTEMROOT%\\System32 directory.):</span></span>

    <span data-ttu-id="8becb-111"> *<path> \\wsmanselrg.xml* de la ressource.</span><span class="sxs-lookup"><span data-stu-id="8becb-111">**Wecutil cs** *<path>\\wsmanselrg.xml*</span></span>

3.  <span data-ttu-id="8becb-112">Assurez-vous que l’abonnement est actif en exécutant la commande suivante dans une fenêtre d’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="8becb-112">Ensure that the subscription is active by executing the following command in a command prompt window:</span></span>

    <span data-ttu-id="8becb-113">**Wecutil gr** *wsmanselrg*</span><span class="sxs-lookup"><span data-stu-id="8becb-113">**Wecutil gr** *wsmanselrg*</span></span>

<span data-ttu-id="8becb-114">Le BMC est un microcontrôleur attaché localement à un serveur.</span><span class="sxs-lookup"><span data-stu-id="8becb-114">The BMC is a microcontroller attached locally to a server.</span></span> <span data-ttu-id="8becb-115">Les contrôleurs BMC ont des capteurs qui surveillent l’état physique du serveur et une connexion réseau distincte qui peut communiquer sur le réseau, même si le serveur est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="8becb-115">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="8becb-116">Vous avez accès aux données BMC via le fournisseur WMI de l’interface de gestion de plateforme intelligente (IPMI).</span><span class="sxs-lookup"><span data-stu-id="8becb-116">You have access to BMC data through the Intelligent Platform Management Interface (IPMI) WMI Provider.</span></span> <span data-ttu-id="8becb-117">Pour plus d’informations sur le fournisseur IPMI, consultez [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="8becb-117">For more information about the IPMI provider, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

<span data-ttu-id="8becb-118">Pour que l’abonnement à un événement fonctionne, le contrôleur BMC et le fournisseur IPMI doivent être installés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8becb-118">The computer must have the BMC and the IPMI provider installed for the event subscription to work.</span></span> <span data-ttu-id="8becb-119">Pour les ordinateurs s’exécutant sur Windows Server 2008, le fournisseur IPMI est installé par défaut.</span><span class="sxs-lookup"><span data-stu-id="8becb-119">For computers running on Windows Server 2008, the IPMI provider is installed by default.</span></span> <span data-ttu-id="8becb-120">Si le BMC n’est pas disponible, le pilote IPMI ne peut pas être installé et l’état d’exécution de l’abonnement affiche toujours une erreur (0x8004001-échec générique WMI).</span><span class="sxs-lookup"><span data-stu-id="8becb-120">If the BMC is not available, then IPMI driver cannot be installed and the subscription runtime status will always display an error (0x8004001 - WMI Generic Failure).</span></span>

 

 