---
description: La configuration correcte des symboles pour le débogage peut être une tâche difficile, en particulier pour le débogage du noyau.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Serveur de symboles et magasins de symboles"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a54753885fc1771c43223770421eb8c2bfe7feffc5bf39b60d875852ddce22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956948"
---
# <a name="symbol-server-and-symbol-stores"></a>  Serveur de symboles et magasins de symboles

La configuration correcte des symboles pour le débogage peut être une tâche difficile, en particulier pour le débogage du noyau. Il est souvent nécessaire de connaître les noms et les versions de tous les produits sur votre ordinateur. Le débogueur doit être en mesure de localiser les fichiers de symboles qui correspondent à chaque version de produit et Service Pack. Cela peut aboutir à un chemin d’accès de symboles extrêmement long composé d’une longue liste de répertoires.

Pour simplifier ces difficultés dans la coordination des fichiers de symboles, utilisez le *serveur de symboles*. Le serveur de symboles permet aux débogueurs de récupérer automatiquement les fichiers de symboles appropriés sans les noms de produits, les mises en production ou les numéros de Build. outils de débogage pour Windows contient le serveur de symboles SymSrv.

Le serveur de symboles est activé en incluant une certaine chaîne de texte dans le chemin d’accès aux symboles. Chaque fois que le débogueur doit charger des symboles pour un module qui vient d’être chargé, il appelle le serveur de symboles pour localiser les fichiers de symboles appropriés. Le serveur de symboles localise les fichiers dans un *magasin de symboles*. Il s’agit d’une collection de fichiers de symboles, d’un index et d’un outil qui peut être utilisé par un administrateur pour ajouter et supprimer des fichiers. Les fichiers sont indexés selon des paramètres uniques, tels que l’horodatage et la taille de l’image. les outils de débogage pour Windows contiennent un outil de magasin de symboles appelé SymStore.

Pour plus d'informations, consultez les pages suivantes :

-   [Utilisation de SymSrv](using-symsrv.md)
-   [Utilisation de SymStore](using-symstore.md)
-   [Utilisation d’autres magasins de symboles](using-other-symbol-stores.md)
-   [Options de Command-Line SymStore](symstore-command-line-options.md)
-   [Serveur de symboles et pare-feu Internet](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fichiers de symboles](symbol-files.md)
</dt> </dl>

 

 



