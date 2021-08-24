---
title: BITS et restauration du système
description: Toutes les versions de BITS n’utilisent pas le même format pour stocker les travaux.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0fbf96cf4d1e3372a9e65cad27c1e1f34ebdb07b6edd976e8b1f36add8a50eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702099"
---
# <a name="bits-and-system-restore"></a>BITS et restauration du système

Toutes les versions de BITS n’utilisent pas le même format pour stocker les travaux. Si vous renvoyez l’ordinateur à un point de restauration avant une mise à niveau de BITS, l’ancienne version de BITS ne pourra peut-être pas lire les informations de la tâche actuelle. Dans ce cas, le service BITS supprime la liste des tâches et crée une nouvelle liste de travaux vide. Par conséquent, les fichiers temporaires associés à la liste de travaux précédente ne sont pas nettoyés. pour récupérer l’espace disque, vous devez supprimer les fichiers manuellement.

les utilisateurs familiarisés avec la ligne de commande Windows peuvent éviter ce problème en utilisant l' [outil BITSAdmin](bitsadmin-tool.md) pour effacer la liste des tâches BITS avant d’exécuter la restauration du système. Pour effacer la liste des tâches BITS, exécutez la commande suivante :

**Bitsadmin/Reset/ALLUSERS**

Notez que vous devez disposer de privilèges d’administrateur pour exécuter cette commande.

 

 




