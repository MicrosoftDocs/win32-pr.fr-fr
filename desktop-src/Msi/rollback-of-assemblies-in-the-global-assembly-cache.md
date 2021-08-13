---
description: un processus en deux étapes étend le modèle de transaction de Windows Installer aux produits contenant common language runtime assemblys. Cela permet au programme d’installation de restaurer les installations et les suppressions ayant échoué d’assemblys.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Restauration d’assemblys dans le global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1379d8132e4a0789108bae4b26fc02c492f5ccb9a0ec7699bba3d9d4de04d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625824"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Restauration d’assemblys dans le global assembly cache

un processus en deux étapes étend le modèle de transaction de Windows Installer aux produits contenant common language runtime assemblys. Cela permet au programme d’installation de restaurer les installations et les suppressions ayant échoué d’assemblys.

au cours de la première étape, l’Windows Installer utilise le .NET Framework Microsoft pour créer une interface pour chaque assembly. le Windows Installer utilise autant d’interfaces qu’il y a d’assemblys en cours d’installation. La validation d’un assembly à l’aide de l’une de ces interfaces signifie uniquement que l’assembly est prêt à remplacer un assembly existant portant le même nom, il ne le remplace pas encore. si l’utilisateur annule l’installation, ou s’il y a une erreur d’installation irrécupérable, le Windows Installer peut toujours restaurer l’assembly à son état précédent en libérant ces interfaces.

une fois l’Windows Installer terminée l’installation de tous les assemblys et Windows Installer composants, le programme d’installation peut lancer la deuxième étape de l’installation. La deuxième étape utilise une fonction distincte pour effectuer la validation finale de tous les nouveaux assemblys de common language runtime. Cela remplace tous les assemblys existants portant le même nom.

 

 



