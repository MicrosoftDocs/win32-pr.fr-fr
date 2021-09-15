---
title: Nouveautés dans SNMP
description: SNMP prend en charge l’utilisation d’ipv6 à partir de Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413486"
---
# <a name="new-in-snmp"></a>Nouveautés dans SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

SNMP prend en charge l’utilisation d’ipv6 à partir de Windows Vista. toutefois, SNMP prend en charge IPv6 uniquement pour les réseaux qui exécutent Windows Server 2008 et Windows Vista. Cela est dû au fait que SNMP requiert la mise à jour de la pile de protocole disponible dans ces systèmes d’exploitation pour sa prise en charge IPv6.

à moins que votre réseau ne soit qu’un réseau Windows Server 2008, les communications ipv6 échouent, même si une pile de protocole ipv6 est installée séparément sur les ordinateurs qui exécutent des versions antérieures de Windows. par exemple, les agents SNMP qui s’exécutent sur Windows Server 2003 ou Windows XP, ou Windows 2000, répondent uniquement aux requêtes qui sont effectuées sur leurs adresses IPv4.

 

 