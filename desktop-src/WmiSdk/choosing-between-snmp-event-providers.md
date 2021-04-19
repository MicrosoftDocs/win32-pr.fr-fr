---
description: Les fournisseurs d’événements SNMP reçoivent les paquets d’événements SNMP de la pile WINSNMP et traduisent les informations incluses dans les paquets en événements WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Choix entre des fournisseurs d’événements SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534661"
---
# <a name="choosing-between-snmp-event-providers"></a>Choix entre des fournisseurs d’événements SNMP

Les fournisseurs d’événements SNMP reçoivent les paquets d’événements SNMP de la pile WINSNMP et traduisent les informations incluses dans les paquets en événements WMI.

WMI comprend les deux fournisseurs d’événements SNMP suivants :

-   Fournisseur d’événements encapsulés SNMP (SEEP)

    L’approvisionnement encapsulé signifie que l’instance d’événement a des propriétés simples qui décrivent les informations mappées directement à partir de l’interruption SNMP.

-   Fournisseur d’événements référent SNMP (SREP)

    Le service référent extrait les informations présentes dans l’interruption SNMP afin que les propriétés qui partagent la même classe et l’instance soient présentées sous forme d’objets incorporés. Cela permet à l’instance unique, à laquelle l’interruption est associée, d’être récupérée après la réception de l’événement, à l’aide du \_ \_ RelPath SNMP.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Indépendamment du fait que l’événement SNMP soit une notification SNMPv1 ou SNMPv2C, la pile le signale comme une notification SNMPv2. Par conséquent, les fournisseurs d’événements traitent tous les événements SNMP en tant que notifications SNMPv2.

Pour décrire les événements SNMP aux consommateurs WMI, chaque fournisseur d’événements prend en charge une hiérarchie de classes qui dérive de la classe système [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) . La classe [SNMPNotification](snmpnotification.md) est la classe parente de la hiérarchie SEEP ; la classe [SNMPExtendedNotification](snmpextendednotification.md) est la classe parente de la hiérarchie SREP.

 

 



