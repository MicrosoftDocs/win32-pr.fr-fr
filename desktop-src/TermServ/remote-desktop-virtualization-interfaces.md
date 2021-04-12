---
title: Bureau à distance les interfaces de virtualisation
description: L’API de virtualisation Bureau à distance prend en charge les interfaces suivantes.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315738"
---
# <a name="remote-desktop-virtualization-interfaces"></a>Bureau à distance les interfaces de virtualisation

L’API de virtualisation Bureau à distance prend en charge les interfaces suivantes.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**ITsSbBaseNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

Expose des méthodes qui signalent des messages d’État et d’erreur à Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).

</dd> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

Expose des méthodes et des propriétés qui stockent des informations d’État sur une demande de connexion entrante à partir d’un client Connexion Bureau à distance (RDC).

</dd> <dt>

[**ITsSbClientConnectionPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

Peut être utilisé pour définir les propriétés personnalisées d’une connexion cliente, le cas échéant.

</dd> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

Expose des méthodes et des propriétés qui contiennent des informations sur l’environnement qui héberge l’ordinateur cible. Cette interface peut être utilisée pour stocker des informations sur un serveur physique qui héberge des ordinateurs virtuels.

</dd> <dt>

[**ITsSbEnvironmentPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

Peut être utilisé pour définir les propriétés personnalisées d’un environnement qui héberge les ordinateurs cibles, le cas échéant.

</dd> <dt>

[**ITsSbFilterPluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

Filtrer le magasin de plug-ins

</dd> <dt>

[**ITsSbGenericNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

Expose les méthodes qui signalent l’achèvement à et obtient le temps d’attente du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

[**ITsSbGlobalStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

Expose les méthodes qui interrogent les ordinateurs cibles, les sessions, les environnements et les batteries de serveurs qui ont été ajoutés au magasin du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

[**ITsSbLoadBalanceResult**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

Expose des méthodes et des propriétés qui stockent le nom cible retourné par un algorithme d’équilibrage de charge.

</dd> <dt>

[**ITsSbLoadBalancing**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

Expose des méthodes que vous pouvez utiliser pour fournir un algorithme d’équilibrage de charge personnalisé.

</dd> <dt>

[**ITsSbLoadBalancingNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

Expose les méthodes qui retournent le résultat d’un algorithme d’équilibrage de charge au service Broker pour les connexions Bureau à distance.

</dd> <dt>

[**ITsSbOrchestration**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

Expose les méthodes utilisées par le Service Broker pour les connexions Bureau à distance pour s’assurer que la cible est prête avant qu’un client lui soit redirigé.

</dd> <dt>

[**ITsSbOrchestrationNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

Expose des méthodes qui retournent un objet [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) à Service Broker pour les connexions Bureau à distance après la préparation de la cible pour une connexion.

</dd> <dt>

[**ITsSbPlacement**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

Expose des méthodes qui préparent l’environnement (l’ordinateur qui héberge l’ordinateur virtuel).

</dd> <dt>

[**ITsSbPlacementNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

Expose des méthodes qui retournent des informations sur les environnements au service Broker pour les connexions Bureau à distance.

</dd> <dt>

[**ITsSbPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

Expose les méthodes qui initialisent et terminent les plug-ins.

</dd> <dt>

[**ITsSbPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

Expose des méthodes qui notifient l’initialisation ou l’arrêt d’un plug-in par le Service Broker pour les connexions Bureau à distance.

</dd> <dt>

[**ITsSbPluginPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

Peut être utilisé pour définir les propriétés de plug-in personnalisées, le cas échéant.

</dd> <dt>

[**ITsSbPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

Peut être utilisé pour définir les propriétés personnalisées appropriées.

</dd> <dt>

[**ITsSbProvider**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

Expose des méthodes qui créent des implémentations par défaut des objets utilisés dans Bureau à distance virtualisation.

</dd> <dt>

[**ITsSbProvisioning**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

Expose des méthodes qui créent et gèrent des ordinateurs virtuels.

</dd> <dt>

[**ITsSbProvisioningPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

Expose des méthodes qui notifient le Service Broker pour les connexions Bureau à distance de la configuration des ordinateurs virtuels.

</dd> <dt>

[**ITsSbResourceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

Expose les méthodes que le Service Broker pour les connexions Bureau à distance utilise pour notifier les plug-ins des modifications d’État qui se produisent dans la session, la cible et les objets de connexion client.

</dd> <dt>

[**ITsSbResourceNotificationEx**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

Expose les méthodes que le Service Broker pour les connexions Bureau à distance utilise pour notifier les plug-ins des modifications d’État qui se produisent dans la session, la cible et les objets de connexion client.

</dd> <dt>

[**ITsSbResourcePlugin**](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

Expose des méthodes qui étendent les fonctionnalités du Service Broker pour les connexions Bureau à distance.

</dd> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

Expose des méthodes qui permettent aux plug-ins de ressources de stocker des objets tels que des sessions et des cibles.

</dd> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> <dd>

Expose des méthodes qui permettent aux plug-ins de ressources de stocker des objets tels que des sessions et des cibles.

</dd> <dt>

[**ITsSbServiceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

Expose les méthodes que le Service Broker pour les connexions Bureau à distance utilise pour notifier les plug-ins des modifications d’État qui se produisent dans le Service Broker pour les connexions Bureau à distance.

</dd> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

Expose les propriétés qui stockent des informations sur une session utilisateur.

</dd> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

Expose les propriétés qui stockent les informations de configuration et d’état d’une cible.

</dd> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dd>

Expose les propriétés qui stockent les informations de configuration et d’état d’une cible.

</dd> <dt>

[**ITsSbTargetPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

Dérivez de cette interface pour définir un jeu de propriétés cible personnalisé.

</dd> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

Expose les propriétés que le Service Broker de Connexion Bureau à distance utilise pour définir la file d’attente d’un plug-in.

</dd> <dt>

[**ITsSbTaskPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

Expose des méthodes qui mettent à jour la file d’attente des tâches pour les plug-ins Connexion Bureau à distance Broker.

</dd> <dt>

[**ITsSbTaskPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

Expose des méthodes qui signalent des messages d’État et d’erreur sur les tâches au service Broker pour les connexions Bureau à distance.

</dd> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

Permet d’étendre les fonctionnalités de session Broker TS (session Broker TS). Implémentez cette interface lorsque vous souhaitez fournir un plug-in qui remplace la logique de redirection de session Broker TS.

</dd> </dl>

 

 