---
description: Le programme d’installation enregistre les erreurs et les événements dans son propre journal des erreurs.
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: Journalisation normale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0846305ef53c596fbd6f117eaf76b0715a94c313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528168"
---
# <a name="normal-logging"></a>Journalisation normale

Le programme d’installation enregistre les erreurs et les événements dans son propre journal des erreurs. Le type de journalisation effectué par le programme d’installation est déterminé par le paramètre du mode de journalisation. La journalisation est activée et le mode peut être défini à l’aide des méthodes suivantes :

-   Le mode de journalisation d’une installation lancée à partir de la ligne de commande peut être spécifié à l’aide de l’option/L des [options de ligne de commande](command-line-options.md). Si le mode de journalisation n’est pas spécifié à l’aide de l’option de ligne de commande/L, le mode de journalisation par défaut est utilisé.
-   Le mode de journalisation d’un processus d’installation peut être spécifié par programme à l’aide de la fonction [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) ou de la méthode [**EnableLog**](installer-enablelog.md) . Si le mode de journalisation n’est pas spécifié à l’aide de la fonction **MsiEnableLog** ou de la méthode **EnableLog** , le mode de journalisation par défaut est utilisé.
-   Vous pouvez spécifier le mode de journalisation par défaut d’un package d’installation spécifique en définissant la propriété [**MsiLogging**](msilogging.md) dans la [table des propriétés](property-table.md) du package. Cette propriété est disponible à partir de Windows Installer 4,0.
-   Si la propriété [**MsiLogging**](msilogging.md) est présente dans la [table de propriétés](property-table.md), le mode de journalisation par défaut du package peut être modifié en modifiant la valeur à l’aide d’une [transformation de base de données](database-transforms.md). Le mode de journalisation par défaut ne peut pas être modifié à l’aide de [packages de correctifs](patch-packages.md) (un fichier. msp).
-   Si la propriété [**MsiLogging**](msilogging.md) n’a pas été définie, le mode de journalisation par défaut pour tous les utilisateurs de l’ordinateur peut être spécifié à l’aide de la stratégie de [journalisation](logging.md) .
-   Si la propriété [**MsiLogging**](msilogging.md) a été définie, le mode de journalisation par défaut pour tous les utilisateurs de l’ordinateur peut être spécifié en définissant la stratégie [DisableLoggingFromPackage](disableloggingfrompackage.md) et la stratégie de [journalisation](logging.md) .
-   Si le mode de journalisation n’a pas été spécifié par l’option/L, [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), [**EnableLog**](installer-enablelog.md), [**MsiLogging**](msilogging.md) ou la stratégie de [journalisation](logging.md) , le mode de journalisation par défaut pour le package est le même que celui obtenu en affectant à la propriété **MsiLogging** la valeur « iwearmo ».

 

 



