---
description: Vous pouvez extraire des fichiers d’un fichier CAB de deux manières. La méthode la plus simple et la plus simple consiste à tirer parti du traitement automatique des fichiers CAB intégré aux fonctions d’installation.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extraction de fichiers à partir d’armoires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfd7f41d4951e43bb58fac6efb9b1fd11895373398643e7c8c9cc00821dd72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887250"
---
# <a name="extracting-files-from-cabinets"></a>Extraction de fichiers à partir d’armoires

Vous pouvez extraire des fichiers d’un fichier CAB de deux manières. La méthode la plus simple et la plus simple consiste à tirer parti du traitement automatique des fichiers CAB intégré aux fonctions d’installation.

Les fonctions d’installation, telles que [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)et [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), vérifient la compression sur chaque fichier. Si le fichier se trouve dans un fichier CAB, les fonctions recherchent d’abord un fichier de ce nom en dehors de l’armoire. S’il est trouvé, les fonctions installent le fichier externe, en ignorant le fichier à l’intérieur du fichier CAB. Cela vous permet de mettre à jour un seul fichier à l’intérieur du cabinet sans recréer le fichier CAB.

Les fonctions d’installation suivent également les fichiers d’un fichier CAB qui ont été récupérés, de sorte qu’un fichier n’est extrait qu’une seule fois, même s’il est installé plusieurs fois.

La deuxième méthode pour extraire des fichiers d’un fichier CAB consiste à utiliser [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Cette fonction itère au sein de chaque fichier d’un fichier CAB, en envoyant une notification à une routine de rappel pour chaque fichier trouvé. La routine de rappel retourne ensuite une valeur qui indique si le fichier doit être extrait ou ignoré.

> [!Note]  
> L’API d’installation ne fournit pas de routine de rappel par défaut pour gérer les notifications de fichier CAB. Si vous appelez [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) de manière explicite, vous devez fournir une routine de rappel pour traiter les notifications d’armoire retournées par la fonction.

 

 

 



