---
title: BITS et restauration du système
description: Toutes les versions de BITS n’utilisent pas le même format pour stocker les travaux.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028750"
---
# <a name="bits-and-system-restore"></a>BITS et restauration du système

Toutes les versions de BITS n’utilisent pas le même format pour stocker les travaux. Si vous renvoyez l’ordinateur à un point de restauration avant une mise à niveau de BITS, l’ancienne version de BITS ne pourra peut-être pas lire les informations de la tâche actuelle. Dans ce cas, le service BITS supprime la liste des tâches et crée une nouvelle liste de travaux vide. Par conséquent, les fichiers temporaires associés à la liste de travaux précédente ne sont pas nettoyés. pour récupérer l’espace disque, vous devez supprimer les fichiers manuellement.

Les utilisateurs familiarisés avec la ligne de commande Windows peuvent éviter ce problème en utilisant l' [outil Bitsadmin](bitsadmin-tool.md) pour effacer la liste des tâches bits avant d’exécuter la restauration du système. Pour effacer la liste des tâches BITS, exécutez la commande suivante :

**Bitsadmin/Reset/ALLUSERS**

Notez que vous devez disposer de privilèges d’administrateur pour exécuter cette commande.

 

 




