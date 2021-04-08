---
title: Prise en charge de la norme USB 3,0
description: Prise en charge de la norme USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730757"
---
# <a name="support-for-usb-30"></a>Prise en charge de la norme USB 3,0

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Dans Windows 8 et Windows Server 2012, nous avons ajouté la prise en charge de la norme USB 3,0. Pour ce faire, nous avons ajouté une nouvelle pile logicielle pour alimenter le contrôleur hôte USB 3,0, appelé contrôleur hôte eXtensible (XHC). Nous avons conservé l’interface Parity, le niveau IRQL, le contexte de l’appelant, l’état d’erreur, la fréquence des tentatives, etc. Il ne devrait y avoir aucune différence lors de l’interaction avec un appareil connecté via USB 2,0 et USB 3,0.

Toutefois, si vous écrivez un pilote pour un nouvel appareil USB 3,0, optez pour les nouvelles fonctionnalités USB 3,0.

## <a name="manifestation"></a>Manifestation

Les transferts d’appareils sont plus rapides et moins puissantes à partir d’un PC par des périphériques USB. Il existe un risque que les périphériques USB existants ne fonctionnent pas correctement lorsqu’ils sont connectés à un port USB 3,0. Cela ne devrait pas se produire et n’est pas attendu, mais, étant donné que le logiciel qui alimente USB 3,0 est nouveau, il est risqué.

 

 




