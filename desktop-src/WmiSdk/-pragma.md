---
description: Est semblable à un commutateur de ligne de commande. Toutefois, vous n’avez pas besoin de réentrer une \# commande pragma chaque fois que vous compilez un fichier MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519525"
---
# <a name="pragma"></a>\#pragma

La commande de préprocesseur **\# pragma** est semblable à un commutateur de ligne de commande. Toutefois, vous n’avez pas besoin de réentrer une commande **\# pragma** chaque fois que vous compilez un fichier MOF. L’exemple suivant illustre la syntaxe de commande **\# pragma** :


```mof
#pragma [command]
```



En général, vous placez une commande **\# pragma** au début d’un fichier MOF. Toutefois, vous pouvez placer des commandes, telles que la commande **\# pragma** , dans le corps de votre code MOF. L’exemple suivant montre des commandes **\# pragma** qui indiquent au compilateur MOF qu’il doit placer des classes et des instances dans l' \\ espace de noms CIMV2 racine et compiler le fichier dans lequel les commandes sont incluses pendant la récupération du référentiel :


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



La liste suivante répertorie les commandes **\# pragma** disponibles.



| Commande                                         | Description                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Amendement**](pragma-amendment.md)           | Indique au compilateur MOF de séparer un fichier MOF en versions indépendantes du langage et spécifiques à la langue. |
| [**récupération automatique**](pragma-autorecover.md)       | Ajoute un fichier MOF à la liste des fichiers compilés au cours de la récupération du référentiel.                             |
| [**classflags**](pragma-classflags.md)         | Contrôle la façon dont les classes sont créées ou mises à jour en fonction des indicateurs spécifiés.                     |
| [**deleteclass**](pragma-deleteclass.md)       | Supprime une classe existante et ses instances du référentiel.                                      |
| [**DeleteInstance**](pragma-deleteinstance.md) | Supprime une instance existante d’une classe du référentiel.                                          |
| [**instanceflags**](pragma-instanceflags.md)   | Contrôle la façon dont les instances sont créées ou mises à jour en fonction des indicateurs spécifiés.                   |
| [**joint**](pragma-namespace.md)           | Demande que le compilateur charge le fichier MOF dans l’espace de noms spécifié en tant que *NamespacePath*.         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Commandes de préprocesseur](preprocessor-commands.md)
</dt> </dl>

 

 



