---
description: Les opérations de sauvegarde et de restauration VSS utilisent chacune un protocole pour l’interaction des systèmes qui utilisent le stockage de masse (Writers) et ceux qui les sauvegardent (demandeurs).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Utilisation de l’Service VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ad0f07cc20da83f9401ff5194776300c5aad23a950b2fbc7f14f787fe22f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866249"
---
# <a name="using-the-volume-shadow-copy-service"></a>Utilisation de l’Service VSS

Les opérations de sauvegarde et de restauration VSS utilisent chacune un protocole pour l’interaction des systèmes qui utilisent le stockage de masse (Writers) et ceux qui les sauvegardent (demandeurs).

Les opérations de sauvegarde et de restauration sont principalement pilotées par le demandeur, qui contrôle le comportement de l’enregistreur et du fournisseur en générant des événements COM à l’échelle du writer à traiter. Étant donné que les méthodes de génération d’événements sont asynchrones, les Writers ont un contrôle limité de l’état du demandeur via les gestionnaires asynchrones disponibles pour VSS (voir [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).

Cette interaction requiert des structures de données de base décrivant les fichiers et les groupes de fichiers ([*composants*](vssgloss-c.md)), ainsi qu’un modèle de métadonnées permettant de stocker les informations de sauvegarde et d’autoriser la communication de rédacteur/demandeur.

-   [Compatibilité des applications VSS](usage-conventions.md)
-   [Configuration de VSS](configuring-vss.md)
-   [Métadonnées VSS](vss-metadata.md)
-   [Utilisation de la sélectivité et des chemins logiques](working-with-selectability-and-logical-paths.md)
-   [Vue d’ensemble du traitement d’une sauvegarde sous VSS](overview-of-processing-a-backup-under-vss.md)
-   [Vue d’ensemble du traitement d’une restauration sous VSS](overview-of-processing-a-restore-under-vss.md)

 

 



