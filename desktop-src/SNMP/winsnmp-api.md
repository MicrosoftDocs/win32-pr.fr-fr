---
title: API WinSNMP
description: l’Interface de programmation d’applications snmp de Microsoft Windows (l’API WinSNMP) versions 1.1 a et 2,0 vous permettent de développer des applications de gestion de réseau basées sur SNMP qui s’exécutent dans l’environnement Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- API WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38f6205b8d5ad2315be877f62f0f81f17b5737e557d5db2683163ff26edf62c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142982"
---
# <a name="winsnmp-api"></a>API WinSNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

l’Interface de programmation d’applications snmp de Microsoft Windows (l’API WinSNMP) versions 1.1 a et 2,0 vous permettent de développer des applications de gestion de réseau basées sur SNMP qui s’exécutent dans l’environnement Windows. Le protocole SNMP (simple Network Management Protocol) est un protocole de requête-réponse qui transfère les informations de gestion entre les entités de protocole.

WinSNMP a été développé conjointement avec la collaboration, l’entrée et la prise en charge de plusieurs sociétés, associations et individus.

La première partie de cette vue d’ensemble fournit des informations sur l’Addendum 2,0 de WinSNMP, les versions SNMP et une liste des RFC (Request for Comments) appropriées. Il décrit également le modèle WinSNMP, ainsi que les composants et fonctionnalités de l’implémentation de Microsoft WinSNMP. Il fournit également des informations sur les concepts de gestion et de communication des données que vous devez programmer dans l’environnement WinSNMP.

La deuxième section traite des fonctions WinSNMP et des tâches de programmation WinSNMP associées suivantes :

-   [Ouverture et fermeture d’une application WinSNMP](opening-and-closing-a-winsnmp-application.md)
-   [Ouverture et fermeture d’une session WinSNMP](opening-and-closing-a-winsnmp-session.md)
-   [Gestion des interruptions et des notifications](managing-traps-and-notifications.md)
-   [Utilisation des listes de liaisons de variables](working-with-variable-binding-lists.md)
-   [Utilisation d’unités de données de protocole](working-with-protocol-data-units.md)
-   [Envoi de messages SNMP](sending-snmp-messages.md)
-   [Réception des messages SNMP](receiving-snmp-messages.md)
-   [Gestion des identificateurs d’objets](managing-object-identifiers.md)
-   [Libération des descripteurs WinSNMP](freeing-winsnmp-descriptors.md)
-   [Définition du mode de traduction entité et contexte](setting-the-entity-and-context-translation-mode.md)
-   [Gestion de la stratégie de retransmission](managing-the-retransmission-policy.md)
-   [Écriture d’applications WinSNMP avec plusieurs threads](writing-winsnmp-applications-with-multiple-threads.md)
-   [Inscription d’une application d’agent SNMP](registering-an-snmp-agent-application.md)

vous devez être familiarisé avec les concepts de base de SNMP et de Windows la programmation avant de lire cette vue d’ensemble. Pour plus d’informations sur SNMP, voir [protocole de gestion de réseau simple](simple-network-management-protocol-snmp-.md) et les RFC (Request for Comments) pertinents publiés par l’IETF (Internet Engineering Task Force).

 

 