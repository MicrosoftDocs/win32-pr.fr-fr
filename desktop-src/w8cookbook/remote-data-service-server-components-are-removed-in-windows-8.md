---
title: Service de données distant supprimé
description: Les composants du serveur de services de données distants sont supprimés dans Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Serveur RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226244"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a>Les composants du serveur de services de données distants sont supprimés dans Windows 8

## <a name="platforms"></a>Plateformes

 **Clients** -Windows 8  
**serveurs** -Windows Server 2012  



## <a name="description"></a>Description

Le serveur RDS (Remote Data Service) n’est pas disponible dans Windows 8 :

-   Le msadcf.dll de fichiers, qui héberge le « Business Object » par défaut, RDSServer. DataFactory, est supprimé et ses fichiers associés (msadcfr.dll, msadcfr.dll. mui, handler. reg et handsafe. reg) sont supprimés
-   Le fichier msdfmap.dll, qui est le gestionnaire par défaut, est supprimé et le fichier msdfmap.ini est supprimé
-   Le msadcs.dll de fichier, ISAPI, est supprimé

## <a name="manifestation"></a>Manifestation

Les clients ne peuvent pas héberger un serveur RDS sur Windows 8.

## <a name="mitigation"></a>Limitation des risques

les clients peuvent conserver leur serveur RDS sur un ordinateur avec Windows 7 ou d’autres systèmes d’exploitation de niveau supérieur.

## <a name="solution"></a>Solution

les clients peuvent conserver leur serveur RDS sur un ordinateur avec Windows 7 ou d’autres systèmes d’exploitation de niveau supérieur.

## <a name="resources"></a>Ressources

[Feuille de route des technologies d’accès aux données](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 