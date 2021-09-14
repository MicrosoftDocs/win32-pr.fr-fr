---
title: Instructions relatives au matériel périphérique
description: Si leur périphérique matériel n’est pas conçu pour fonctionner sur une session à distance, les fournisseurs doivent s’assurer que le logiciel du pilote de périphérique force la désactivation de la redirection de l’appareil à l’aide d’une stratégie système ou d’une stratégie de groupe.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919648"
---
# <a name="peripheral-hardware-guidelines"></a>Instructions relatives au matériel périphérique

Sur un client Connexion Bureau à distance (RDC), le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est l’ordinateur local. Par conséquent, les périphériques tels que les lecteurs de disque et les imprimantes attachées au serveur apparaissent en tant qu’appareils locaux sur un client. En revanche, les lecteurs et imprimantes connectés à un terminal client peuvent apparaître comme des périphériques distants, selon les options sélectionnées pour la connexion, le serveur utilisé et la version du logiciel client utilisée.

Tandis que la version initiale de Services Bureau à distance ne prenait pas en charge les applications qui envoient des sorties directement aux ports série, parallèle et audio attachés au terminal client, les versions actuelles autorisent ces appareils à apparaître en tant qu’appareils locaux pour les applications qui s’exécutent dans la session de Services Bureau à distance.

Si leur périphérique matériel n’est pas conçu pour fonctionner sur une session à distance, les fournisseurs doivent s’assurer que le logiciel du pilote de périphérique force la désactivation de la redirection de l’appareil à l’aide d’une stratégie système ou d’une stratégie de groupe.

 

 




