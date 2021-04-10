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
# <a name="updating-registry-information"></a><span data-ttu-id="3dd7b-103">Mise à jour des informations du Registre</span><span class="sxs-lookup"><span data-stu-id="3dd7b-103">Updating Registry Information</span></span>

<span data-ttu-id="3dd7b-104">Une fois que la file d’attente a été validée avec succès, vous devez mettre à jour les informations du Registre pour le produit que vous installez.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-104">After the queue has successfully committed, you will need to update registry information for the product you are installing.</span></span> <span data-ttu-id="3dd7b-105">Il est recommandé d’attendre que toutes les opérations de copie de fichiers nécessaires aient été effectuées avec succès avant de modifier les informations du Registre.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-105">It is recommended that you wait until all necessary file copy operations have been successfully completed before altering registry information.</span></span>

<span data-ttu-id="3dd7b-106">L’une des façons de mettre à jour le registre consiste à appeler [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) avec le INIFILES de rotation le plus efficace, le registre de rotation le plus efficace \_ ou les \_ indicateurs INI2REG de spinst \_ spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-106">One way to update the registry is to call [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) with the SPINST\_INIFILES, SPINST\_REGISTRY, or SPINST\_INI2REG flags specified.</span></span> <span data-ttu-id="3dd7b-107">Ces indicateurs peuvent être combinés en un seul appel à **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-107">These flags can be combined in one call to **SetupInstallFromInfSection**.</span></span>

<span data-ttu-id="3dd7b-108">L’exemple suivant utilise \_ tous les ^ fichiers de rotation tous les ^ \_ pour indiquer que la fonction doit traiter toutes les opérations de la liste, à l’exception des opérations de fichier.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-108">The following example uses SPINST\_ALL^SPINST\_FILES to indicate that the function should process all of the listed operations except file operations.</span></span> <span data-ttu-id="3dd7b-109">Étant donné que seules les opérations INI, de Registre et de fichier sont répertoriées dans la section **install** , il s’agit d’une méthode abrégée qui consiste à spécifier que la fonction doit traiter toutes les opérations ini et du Registre.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-109">Since only INI, registry, and file operations are listed in the **Install** section, this is a shorthand method of specifying the function should process all INI and registry operations.</span></span>

<span data-ttu-id="3dd7b-110">L’exemple suivant montre comment installer les informations du Registre à l’aide de la fonction **SetupInstallFromINFSection** .</span><span class="sxs-lookup"><span data-stu-id="3dd7b-110">The following example shows how to install registry information using the **SetupInstallFromINFSection** function.</span></span>

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

<span data-ttu-id="3dd7b-111">Dans l’exemple, *OwnerWindow* a la **valeur null** , car seules les opérations de fichier génèrent des boîtes de dialogue et, par conséquent, une fenêtre parente n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-111">In the example, *OwnerWindow* is **NULL** because only file operations generate dialog boxes, and thus a parent window is not needed.</span></span> <span data-ttu-id="3dd7b-112">« MyInf » est le fichier INF contenant la section à traiter.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-112">"MyInf" is the INF file containing the section to process.</span></span> <span data-ttu-id="3dd7b-113">Le paramètre « MySection » spécifie la section à installer.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-113">The parameter, "MySection", specifies the section to be installed.</span></span> <span data-ttu-id="3dd7b-114">Les indicateurs combinés, \_ les ^ fichiers les ^ les plus \_ perverses, spécifient les opérations d’installation à traiter, dans ce cas, toutes les opérations à l’exception des opérations de fichier.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-114">The combined flags, SPINST\_ALL ^ SPINST\_FILES, specify which installation operations to process, in this case, all operations except file operations.</span></span> <span data-ttu-id="3dd7b-115">Le chemin racine source est spécifié sous la forme « A : \\ ».</span><span class="sxs-lookup"><span data-stu-id="3dd7b-115">The source root path is specified as "A:\\".</span></span>

<span data-ttu-id="3dd7b-116">Dans la mesure où aucune opération de copie n’est en cours de traitement, les paramètres *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet* et *DeviceInfoData* ne sont pas spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3dd7b-116">Since no copy operations are being processed, the *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet*, and *DeviceInfoData* parameters are not specified.</span></span>

 

 



