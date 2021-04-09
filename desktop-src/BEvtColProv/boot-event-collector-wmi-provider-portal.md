---
description: Le fournisseur WMI du collecteur d’événements de démarrage fournit l’accès aux informations de connexion et de configuration pour la fonctionnalité de collecte d’événements d’installation et de démarrage sur Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Fournisseur WMI du collecteur d’événements de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846977"
---
# <a name="boot-event-collector-wmi-provider"></a>Fournisseur WMI du collecteur d’événements de démarrage

## <a name="purpose"></a>Objectif

Le fournisseur WMI du collecteur d’événements de démarrage fournit l’accès aux informations de connexion et de configuration pour la fonctionnalité de collecte d’événements d’installation et de démarrage sur Windows Server. Cela vous permet d’afficher la liste des connexions en cours et l’historique des connexions entre un serveur du collecteur et ses ordinateurs cibles. En outre, ce fournisseur vous permet de gérer la configuration d’un serveur collecteur.

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

 

 



