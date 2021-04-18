---
description: La mise en file d’attente des opérations de fichier est utile, car elle vous permet de traiter l’installation dans son ensemble, plutôt que par la section INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Création d’une file d’attente et mise en file d’attente des opérations de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533656"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a>Création d’une file d’attente et mise en file d’attente des opérations de fichiers

La mise en file d’attente des opérations de fichier est utile, car elle vous permet de traiter l’installation dans son ensemble, plutôt que par la section INF.

Pour créer une file d’attente de fichiers, déclarez une variable pour stocker le descripteur de file d’attente, puis appelez la fonction [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) . Une fois la file d’attente créée, vous pouvez effectuer des opérations de copie, de renommage et de suppression, ainsi que d’analyser la file d’attente de fichiers pour vérifier les opérations mises en file d’attente.

Pour ajouter des opérations de fichier unique à la file d’attente, utilisez les fonctions [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)et [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .

Toutes les opérations de fichiers listées dans une section **copier** des fichiers, **supprimer des fichiers** ou **Renommer des fichiers** peuvent être ajoutées à la file d’attente à l’aide de [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)ou [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectivement.

Une autre façon de faire la file d’attente de tous les fichiers dans les sections **copier les fichiers** figurant dans une section d' **installation** d’un fichier INF consiste à utiliser la fonction [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).

L’exemple suivant utilise la fonction [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) pour empiler les opérations de copie de tous les fichiers listés dans une section **copier des fichiers** d’un fichier INF.

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

Dans l’exemple, MyQueue est la file d’attente dans laquelle ajouter des opérations de copie, « A : \\ » spécifie le chemin d’accès à la source, et MyInf est le descripteur du fichier INF ouvert. Le paramètre *ListInfHandle* a la valeur **null**, ce qui indique que la section pour la copie se trouve dans MyInf. MySection est la section de MyInf contenant les fichiers à la file d’attente pour la copie.

Les indicateurs SP de \_ copie \_ NOSKIP et SP # \_ \_ Browse ont été combinés à l’aide d’un opérateur or pour indiquer que l’utilisateur ne doit pas être proposé d’options pour ignorer ou Rechercher des fichiers si des erreurs se produisent.

 

 



