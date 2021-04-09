---
description: Le programme d’installation exécute la séquence de l’Assistant Installation de l’exemple uniquement si le niveau d’interface utilisateur complet est utilisé pour installer l’application.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Ajout d’un événement de contrôle à la fin de l’installation pour exécuter le lancement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951797"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a>Ajout d’un événement de contrôle à la fin de l’installation pour exécuter le lancement

Le programme d’installation exécute la séquence de l’Assistant Installation de l’exemple uniquement si le niveau d' [*interface utilisateur complet*](f-gly.md) est utilisé pour installer l’application. La dernière boîte de dialogue de la séquence de dialogue d’exemple est une [boîte de dialogue de sortie](exit-dialog.md) nommée ExitDialog. Lorsqu’un utilisateur interagit avec le bouton OK sur ExitDialog, il publie d’abord un [ControlEvent, EndDialog](enddialog-controlevent.md) qui retourne le contrôle au programme d’installation. Le contrôle publie ensuite un [ControlEvent, de script](doaction-controlevent.md) qui exécute l’action personnalisée Launch. Chaque événement de contrôle requiert un enregistrement dans la [table ControlEvent,](controlevent-table.md). Consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).

[Table ControlEvent,](controlevent-table.md)



| Boîte de dialogue     | contrôle\_ | Événement     | Argument | Condition                     | Classement |
|------------|-----------|-----------|----------|-------------------------------|----------|
| ExitDialog | Ok        | EndDialog | Renvoie   | 1                             | 1        |
| ExitDialog | Ok        | Action  | Lancer   | NON installé et $Tutorial = 3 | 2        |



 

La condition sur le contrôle de script s’assure que l’action personnalisée s’exécute uniquement lors de la première installation de l’application et qu’elle est installée localement. L’expression $Tutorial = 3 signifie que l’état de l’action du composant didacticiel est défini sur local. Consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

Cela termine l’exemple.

 

 



