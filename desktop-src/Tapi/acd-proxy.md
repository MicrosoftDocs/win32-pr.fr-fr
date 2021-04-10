---
description: Un serveur ACD (Automatic Call distribution) est une combinaison de matériel et de logiciels qui classifie, met en file d’attente et distribue les appels entrants aux agents ou les appels sortants vers les lignes.
ms.assetid: 29fb0bd7-0ca9-4490-82d2-39550f00a97b
title: Proxy ACD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c345fbcac3ac3471098e964336a0c3135fd1f582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952487"
---
# <a name="acd-proxy"></a>Proxy ACD

Un serveur ACD (Automatic Call distribution) est une combinaison de matériel et de logiciels qui classifie, met en file d’attente et distribue les appels entrants aux agents ou les appels sortants vers les lignes.

L’application ACD Server est une application de Proxy TAPI qui, pour une efficacité maximale, doit s’exécuter sur le même serveur que le fournisseur de services de téléphonie (TSP). Avec un commutateur ACD traditionnel, l’application proxy s’interface avec le ACD interne du commutateur et expose son fonctionnement. Une application de proxy ACD basée sur des logiciels ou « virtuelles » est entièrement responsable du suivi des appels, des files d’attente, des groupes et des agents et utilise les interfaces TAPI standard pour contrôler le matériel de commutation. Les applications clientes de l’agent s’exécutent généralement sur les stations de travail de l’agent individuel et utilisent le fournisseur de services distant TAPI pour communiquer avec le TAPISRV sur l’ordinateur serveur, et donc l’application proxy.

La classification des appels entrants est conçue pour appeler un agent qui sera en mesure de la gérer efficacement. La classification peut être basée sur le numéro composé, un système de reconnaissance vocale interactive (IVR) ou d’autres critères. L’interface TAPI utilise le concept de [groupe ACD](about-call-center-controls.md) pour représenter cette opération.

Les files d’attente sont un moyen normal et attendu pour que les centres d’appels gèrent des périodes de charge élevée. Une file d’attente est normalement associée à un groupe ACD, mais peut être créée pour gérer les lignes sortantes ou les appels entrants en attente d’une application IVR. Pour plus d’informations, consultez [files d’attente](about-call-center-controls.md) .

La distribution des appels à des agents ou à des groupes d’agents peut être uniforme, mais elle est généralement basée sur des données telles que les informations d’appel, la disponibilité de l’agent et la capacité. Le [Gestionnaire d’agents](about-call-center-controls.md) de l’interface TAPI fournit un accès aux informations telles que la disponibilité et les adresses des agents pour le transfert des appels aux agents.

En plus de la distribution des appels de base, un système ACD permet de gérer et de générer des rapports sur les performances du système. Les statistiques recueillies sur les files d’attente d’appels, les groupes et les agents sont utilisées pour affiner et améliorer les performances du système et sont généralement utilisées comme base pour la rémunération de l’agent.

 

 



