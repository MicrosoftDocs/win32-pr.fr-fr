---
description: Un processus en deux étapes étend le modèle de transaction de Windows Installer aux produits contenant common language runtime assemblys. Cela permet au programme d’installation de restaurer les installations et les suppressions ayant échoué d’assemblys.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Restauration d’assemblys dans le global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751117"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Restauration d’assemblys dans le global assembly cache

Un processus en deux étapes étend le modèle de transaction de Windows Installer aux produits contenant common language runtime assemblys. Cela permet au programme d’installation de restaurer les installations et les suppressions ayant échoué d’assemblys.

Au cours de la première étape, l’Windows Installer utilise l’infrastructure Microsoft .NET pour créer une interface pour chaque assembly. Le Windows Installer utilise autant d’interfaces qu’il y a d’assemblys en cours d’installation. La validation d’un assembly à l’aide de l’une de ces interfaces signifie uniquement que l’assembly est prêt à remplacer un assembly existant portant le même nom, il ne le remplace pas encore. Si l’utilisateur annule l’installation, ou s’il y a une erreur d’installation irrécupérable, le Windows Installer peut toujours restaurer l’assembly à son état précédent en libérant ces interfaces.

Une fois l’Windows Installer terminée l’installation de tous les assemblys et Windows Installer composants, le programme d’installation peut lancer la deuxième étape de l’installation. La deuxième étape utilise une fonction distincte pour effectuer la validation finale de tous les nouveaux assemblys de common language runtime. Cela remplace tous les assemblys existants portant le même nom.

 

 



