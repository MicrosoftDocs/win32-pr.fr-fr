---
description: le fournisseur WMI du collecteur d’événements de démarrage fournit l’accès aux informations de connexion et de configuration pour la fonctionnalité de collecte d’événements d’installation et de démarrage sur Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Fournisseur WMI du collecteur d’événements de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccebb4c4408aaa0ce58ad6ab412e4ca85fbb291c8da14ba764dfe3b19e2cbfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579859"
---
# <a name="boot-event-collector-wmi-provider"></a>Fournisseur WMI du collecteur d’événements de démarrage

## <a name="purpose"></a>Objectif

le fournisseur WMI du collecteur d’événements de démarrage fournit l’accès aux informations de connexion et de configuration pour la fonctionnalité de collecte d’événements d’installation et de démarrage sur Windows Server. Cela vous permet d’afficher la liste des connexions en cours et l’historique des connexions entre un serveur du collecteur et ses ordinateurs cibles. En outre, ce fournisseur vous permet de gérer la configuration d’un serveur collecteur.

> [!Note]  
> Le fournisseur WMI du collecteur d’événements de démarrage est implémenté dans BEvtCol.exe.

 

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**TargetForwarding**](targetforwarding.md)
</dt> <dd>

Récupère les données de transfert d’un ordinateur cible.

</dd> <dt>

[**TargetForwardingDestination**](targetforwardingdestination.md)
</dt> <dd>

Destinations connues contenant les données collectées. Disponible uniquement si le collecteur est en cours d’exécution avec le journal d’état activé.

</dd> <dt>

[**TargetForwardingHistory**](targetforwardinghistory.md)
</dt> <dd>

Historique récent des modifications apportées aux données de transfert pour un ordinateur cible.

</dd> <dt>

[**Contrôler**](control.md)
</dt> <dd>

Contrôle de l’instance du collecteur. Requiert les privilèges d’administrateur (BA).

</dd> </dl>

 

 



