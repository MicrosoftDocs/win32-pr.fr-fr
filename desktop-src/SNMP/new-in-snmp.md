---
title: Nouveautés dans SNMP
description: SNMP prend en charge l’utilisation D’ipv6 à partir de Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729781"
---
# <a name="new-in-snmp"></a>Nouveautés dans SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

SNMP prend en charge l’utilisation D’ipv6 à partir de Windows Vista. Toutefois, SNMP prend en charge IPv6 uniquement pour les réseaux qui exécutent Windows Server 2008 et Windows Vista. Cela est dû au fait que SNMP requiert la mise à jour de la pile de protocole disponible dans ces systèmes d’exploitation pour sa prise en charge IPv6.

À moins que votre réseau ne soit qu’un réseau Windows Server 2008, les communications IPv6 échouent, même si une pile de protocole IPv6 est installée séparément sur les ordinateurs qui exécutent des versions antérieures de Windows. Par exemple, les agents SNMP qui s’exécutent sur Windows Server 2003, Windows XP ou Windows 2000, répondent uniquement aux requêtes effectuées sur leurs adresses IPv4.

 

 