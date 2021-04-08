---
title: Le système d’exploitation contrôle désormais les lecteurs de disque optique
description: Le système d’exploitation contrôle désormais les lecteurs de disque optique
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730733"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>Le système d’exploitation contrôle désormais les lecteurs de disque optique

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Dans les versions précédentes de Windows, la mise sous tension du lecteur optique n’était pas gérée lorsque le lecteur optique n’était pas en cours d’utilisation. Si aucun support n’est présent dans le lecteur de disque optique (impair), le système d’exploitation éteint l’alimentation du lecteur optique. Cette fonctionnalité est appelée Zero Power impaire (ZPODD). Cette fonctionnalité s’applique uniquement aux lecteurs optiques qui utilisent un connecteur SATA (Serial Advanced Technology Attachment).

## <a name="manifestation"></a>Manifestation

Nous n’avons pas trouvé d’impact négatif sur ce nouveau comportement ; Toutefois, vous devez en être conscient, car cela peut entraîner un comportement inattendu du logiciel d’écriture de médias.

## <a name="mitigation"></a>Limitation des risques

Pour revenir à l’État Always on, désactivez cette fonctionnalité dans le registre. Le chemin d’accès absolu à la valeur de Registre est :

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

Son type est DWORD (32 bits), et si sa valeur est 0, ZPODD est désactivé. s’il s’agit d’une autre valeur, ZPODD est activé.

## <a name="tests"></a>Tests

Testez votre logiciel d’écriture multimédia pour toutes les anomalies qui se produisent en raison de cette nouvelle fonctionnalité. Veuillez [informer Microsoft](mailto:OptIssue@microsoft.com) de tous les problèmes que vous rencontrez avec cette nouvelle fonctionnalité.

 

 




