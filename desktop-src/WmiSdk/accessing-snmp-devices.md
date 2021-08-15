---
description: Permet aux applications clientes d’accéder aux informations SNMP via WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Accès aux appareils SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3acf8fd67ee9153167cd328b7a50f6aafc5853327a64baf80c3b2e20b663d3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320301"
---
# <a name="accessing-snmp-devices"></a>Accès aux appareils SNMP

Le fournisseur SNMP (simple Network Management Protocol) permet aux applications clientes d’accéder aux informations SNMP via WMI. Le [fournisseur SNMP](snmp-provider.md) joue le rôle de passerelle pour les systèmes et les périphériques qui utilisent SNMP pour la gestion. Seul l’ordinateur de gestion ou de surveillance doit exécuter WMI, car il peut lire à partir de n’importe quel périphérique compatible SNMP.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Les variables d’objet MIB (Management Information base) SNMP peuvent être lues et écrites, et les interruptions SNMP peuvent être mappées automatiquement aux événements WMI, qui peuvent être définies pour des opérations de création, de suppression ou de mise à jour arbitraires sur des données au-delà des interruptions définies par la MIB. Cette fonctionnalité de WMI fonctionne comme une extension des fonctionnalités SNMP standard. Pour plus d’informations, consultez [surveillance des événements](monitoring-events.md).

les outils décrits dans les rubriques suivantes sont conçus pour être utilisés par Windows scripting et les programmeurs C/C++. Il est recommandé de vous familiariser avec WMI, SNMPv1 et SNMPv2C, ainsi que des connaissances pratiques sur les concepts de gestion réseau et de réseau.

Pour plus d’informations sur l’utilisation de WMI avec SNMP, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

 



