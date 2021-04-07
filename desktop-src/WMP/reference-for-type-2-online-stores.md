---
title: Référence pour les magasins en ligne de type 2
description: Référence pour les magasins en ligne de type 2
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Windows Media Player Online stores, référence
- magasins en ligne, référence
- type 2 magasins en ligne, référence
- référence pour les magasins en ligne de type 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103724190"
---
# <a name="reference-for-type-2-online-stores"></a>Référence pour les magasins en ligne de type 2

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

Le lecteur Windows Media 10 ou version ultérieure fournit des objets, des interfaces, des propriétés et des méthodes qui prennent en charge les magasins de type 2 en ligne. Les sections suivantes documentent ces informations en détail.



| Section                                                                                                        | Description                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interface IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | Fournit des méthodes pour augmenter la gestion des droits numériques (DRM) et initier des processus en arrière-plan.                                                                              |
| [Interface IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | Fournit des méthodes pour initier des processus en arrière-plan, fournir des informations sur l’activité du magasin en ligne et fournir un pointeur vers l’interface principale du lecteur Windows Media. |
| [Interface IWMPSubscriptionServiceCallback](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | Définit une méthode utilisée par les magasins en ligne pour notifier le lecteur Windows Media quand un processus en arrière-plan est terminé.                                                              |
| [WMPNotifySubscriptionPluginAddRemove](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | Fonction utilisée pour informer le lecteur Windows Media qu’un plug-in a été installé ou désinstallé.                                                                            |
| [Objet DownloadCollection](downloadcollection-object.md)                                                     | Fournit des méthodes et des propriétés pour gérer des collections d’éléments de téléchargement.                                                                                                    |
| [Objet DownloadItem](downloaditem-object.md)                                                                 | Fournit des méthodes et des propriétés relatives aux demandes de téléchargement.                                                                                                              |
| [Objet DownloadManager](downloadmanager-object.md)                                                           | Fournit des méthodes pour gérer les collections de téléchargement.                                                                                                                            |
| [Objet externe pour les magasins de type 2 en ligne](external-object-for-type-2-online-stores.md)                       | Fournit des propriétés, des méthodes et un événement accessibles à partir des pages Web du magasin en ligne.                                                                                           |
| [Énumérations pour les magasins de type 2 en ligne](enumerations-for-type-2-online-stores.md)                             | Décrit les énumérations utilisées par les magasins en ligne.                                                                                                                               |
| [Convention de travail de BITS du lecteur Windows Media](windows-media-player-bits-job-convention.md)                       | Décrit une convention pour l’utilisation du Service de transfert intelligent en arrière-plan (BITS).                                                                                        |
| [Clés et entrées de Registre pour un magasin de type 2 en ligne](registry-keys-and-entries-for-a-type-2-online-store.md) | Décrit les entrées de registre qu’un magasin en ligne doit créer dans le registre sur l’ordinateur de l’utilisateur.                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Tapez 2 magasins en ligne**](type-2-online-stores.md)
</dt> </dl>

 

 




