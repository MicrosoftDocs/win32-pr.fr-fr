---
description: Une fois que la file d’attente a été validée avec succès, vous devez mettre à jour les informations du Registre pour le produit que vous installez.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Mise à jour des informations du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952689"
---
# <a name="updating-registry-information"></a>Mise à jour des informations du Registre

Une fois que la file d’attente a été validée avec succès, vous devez mettre à jour les informations du Registre pour le produit que vous installez. Il est recommandé d’attendre que toutes les opérations de copie de fichiers nécessaires aient été effectuées avec succès avant de modifier les informations du Registre.

L’une des façons de mettre à jour le registre consiste à appeler [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) avec le INIFILES de rotation le plus efficace, le registre de rotation le plus efficace \_ ou les \_ indicateurs INI2REG de spinst \_ spécifiés. Ces indicateurs peuvent être combinés en un seul appel à **SetupInstallFromInfSection**.

L’exemple suivant utilise \_ tous les ^ fichiers de rotation tous les ^ \_ pour indiquer que la fonction doit traiter toutes les opérations de la liste, à l’exception des opérations de fichier. Étant donné que seules les opérations INI, de Registre et de fichier sont répertoriées dans la section **install** , il s’agit d’une méthode abrégée qui consiste à spécifier que la fonction doit traiter toutes les opérations ini et du Registre.

L’exemple suivant montre comment installer les informations du Registre à l’aide de la fonction **SetupInstallFromINFSection** .

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

Dans l’exemple, *OwnerWindow* a la **valeur null** , car seules les opérations de fichier génèrent des boîtes de dialogue et, par conséquent, une fenêtre parente n’est pas nécessaire. « MyInf » est le fichier INF contenant la section à traiter. Le paramètre « MySection » spécifie la section à installer. Les indicateurs combinés, \_ les ^ fichiers les ^ les plus \_ perverses, spécifient les opérations d’installation à traiter, dans ce cas, toutes les opérations à l’exception des opérations de fichier. Le chemin racine source est spécifié sous la forme « A : \\ ».

Dans la mesure où aucune opération de copie n’est en cours de traitement, les paramètres *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet* et *DeviceInfoData* ne sont pas spécifiés.

 

 



