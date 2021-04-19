---
description: Les fonctions de configuration gèrent les armoires en interne. Pour énumérer et extraire explicitement des fichiers d’un fichier CAB, vous pouvez appeler la fonction SetupIterateCabinet.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Utilisation des fichiers CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541930"
---
# <a name="using-cabinet-files"></a>Utilisation des fichiers CAB

Les fonctions de configuration gèrent les armoires en interne. Pour énumérer et extraire explicitement des fichiers d’un fichier CAB, vous pouvez appeler la fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .

La rubrique suivante décrit le traitement du fichier CAB interne aux fonctions d’installation et l’utilisation de [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Les notifications envoyées par **SetupIterateCabinet** et le format requis d’une routine de rappel d’armoire pour traiter ces notifications sont également abordés.

-   [Extraction de fichiers à partir d’armoires](extracting-files-from-cabinets.md)
-   [Création d’une routine de rappel d’armoire](creating-a-cabinet-callback-routine.md)

 

 



