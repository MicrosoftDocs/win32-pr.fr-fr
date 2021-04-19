---
description: Le Windows Installer traite les actions personnalisées en tant que thread distinct de l’installation principale.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Actions personnalisées synchrones et asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517723"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>Actions personnalisées synchrones et asynchrones

Le Windows Installer traite les actions personnalisées en tant que thread distinct de l’installation principale. Pendant l’exécution synchrone d’une action personnalisée, le programme d’installation attend que le thread de l’action personnalisée se termine avant de poursuivre l’installation principale. Pendant l’exécution asynchrone, le programme d’installation exécute l’action personnalisée simultanément lorsque l’installation actuelle se poursuit. Les auteurs des actions personnalisées doivent donc connaître les threads asynchrones qui peuvent apporter des modifications à la base de données d’installation entre les appels de fonction.

En particulier, les appels à [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) et [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) doivent être évités dans les actions personnalisées asynchrones. Utilisez plutôt [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) pour obtenir un chemin d’accès cible. Les opérations de base de données en bloc, telles que les opérations d’importation, d’exportation et de transformation, doivent être évitées dans n’importe quel type d’action personnalisée.

Les indicateurs d’option peuvent être définis dans le champ type de la [table CustomAction](customaction-table.md) pour spécifier que les threads d’action principal et personnalisé s’exécutent de façon synchrone ou asynchrone. Consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).

Le programme d’installation peut uniquement exécuter des actions [personnalisées Rollback](rollback-custom-actions.md) et des actions d' [installation simultanées](concurrent-installations.md) en tant qu’actions personnalisées synchrones.

 

 



