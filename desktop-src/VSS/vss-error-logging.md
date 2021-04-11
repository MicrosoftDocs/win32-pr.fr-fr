---
description: 'Les informations d’erreur et d’état VSS suivantes sont écrites dans le journal des événements de l’application :'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Journalisation des erreurs VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113182"
---
# <a name="vss-error-logging"></a>Journalisation des erreurs VSS

Les informations d’erreur et d’état VSS suivantes sont écrites dans le journal des événements de l’application :

-   Erreurs de demandeur produites à l’aide de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   Erreurs d’écriture produites dans à l’aide de la classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , y compris les méthodes de substitution
-   Erreurs générées par le fournisseur par défaut
-   Erreurs de service VSS générées dans le fournisseur de coordination, l’enregistreur et l’activité du demandeur (par exemple, la génération d’événements)

Ces erreurs peuvent avoir plusieurs causes, y compris une erreur de programmation dans du code tiers ou des erreurs de configuration liées à VSS.

Les pilotes VSS et les fonctionnalités d’implémentation de niveau inférieur écrivent des erreurs dans le journal système. Les logiciels tiers (demandeur, fournisseur, rédacteur) peuvent choisir le journal des applications, le journal système, ou les deux, pour écrire les entrées du journal des erreurs.

Il est recommandé que les applications de haut niveau (telles que le code en mode utilisateur) utilisent le journal des applications. Les applications de niveau inférieur, telles que les interfaces et les pilotes matériels, doivent utiliser le journal système.

 

 



