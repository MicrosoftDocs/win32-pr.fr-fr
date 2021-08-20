---
description: le routeur multifournisseur (MPR) gère la communication entre le système d’exploitation Windows et les fournisseurs réseau installés. il permet à Windows de présenter un réseau intégré à l’utilisateur.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Routeur à plusieurs fournisseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788a6b5dc7ec2db1f75d4bdf7d04df4127e90670b7f798682423dac4567a6fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786577"
---
# <a name="multiple-provider-router"></a>Routeur à plusieurs fournisseurs

le [*routeur multifournisseur*](../secgloss/m-gly.md) (MPR) gère la communication entre le système d’exploitation Windows et les fournisseurs réseau installés. il permet à Windows de présenter un réseau intégré à l’utilisateur.

Au démarrage de MPR, il vérifie le registre pour déterminer quels fournisseurs de réseau sont installés sur le système et l’ordre dans lequel ils doivent être recycles. Il charge toutes les dll de fournisseur réseau inscrites et les utilise pour traiter les appels WNet suivants effectués par l’interface utilisateur ou d’autres applications.

pour plus d’informations sur les fonctions WNet, consultez [mise en réseau Windows](../wnet/windows-networking-wnet-.md).

 

 
