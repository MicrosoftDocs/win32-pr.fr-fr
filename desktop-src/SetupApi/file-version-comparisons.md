---
description: Si l' \_ indicateur SP Copy \_ plus récent est spécifié au cours d’une opération de copie de fichiers, les fonctions d’installation recherchent une copie existante du fichier dans le répertoire cible.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Comparaisons de la version de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9601dcef07afca81a3ffc64148b0c4f2492f935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520682"
---
# <a name="file-version-comparisons"></a>Comparaisons de la version de fichier

Si l' \_ indicateur SP Copy \_ plus récent est spécifié au cours d’une opération de copie de fichiers, les fonctions d’installation recherchent une copie existante du fichier dans le répertoire cible. Si une copie existante est trouvée, les fonctions comparent les versions de la cible et du fichier source pour déterminer celle qui est la plus récente.

Les informations de version de fichier utilisées lors des contrôles de version sont celles spécifiées dans les membres **dwFileVersionMS** et **dwFileVersionLS** d’une structure [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) , utilisées par les fonctions de version. Si l’un des fichiers n’a pas de ressources de version spécifiées ou s’ils ont les mêmes informations de version, le fichier source est traité comme le fichier le plus récent.

 

 
