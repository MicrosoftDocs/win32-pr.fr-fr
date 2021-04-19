---
description: Le registre système contient des données relatives aux ressources.
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: Description d’une ressource pour le registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540889"
---
# <a name="describing-a-resource-for-the-registry"></a><span data-ttu-id="2ef2b-103">Description d’une ressource pour le registre</span><span class="sxs-lookup"><span data-stu-id="2ef2b-103">Describing a Resource for the Registry</span></span>

<span data-ttu-id="2ef2b-104">Le registre système contient des données relatives aux ressources.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-104">The system registry contains resource-related data.</span></span> <span data-ttu-id="2ef2b-105">Ces données se trouvent sous la clé de Registre suivante et sont conservées dans un type de données de registre spécial nommé **reg \_ Resource \_ List**.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-105">This data is located under the following registry key and is kept in a special registry data type named **REG\_RESOURCE\_LIST**.</span></span> <span data-ttu-id="2ef2b-106">Les applications peuvent obtenir les données relatives aux ressources par le biais du fournisseur de Registre système.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-106">Applications can obtain the resource-related data through the System Registry provider.</span></span> <span data-ttu-id="2ef2b-107">Vous pouvez ajouter et modifier des ressources système dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-107">You can add and modify system resources in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

<span data-ttu-id="2ef2b-108">La procédure suivante décrit comment stocker des informations relatives aux ressources dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-108">The following procedure describes how to store resource-related information in the system registry.</span></span>

<span data-ttu-id="2ef2b-109">**Pour stocker les informations relatives aux ressources dans le registre système**</span><span class="sxs-lookup"><span data-stu-id="2ef2b-109">**To store resource-related information in the system registry**</span></span>

1.  <span data-ttu-id="2ef2b-110">Créez une chaîne qui contient les champs suivants.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-110">Create a string that contains the following fields.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="2ef2b-111">Champ</span><span class="sxs-lookup"><span data-stu-id="2ef2b-111">Field</span></span></th>
    <th><span data-ttu-id="2ef2b-112">Contient</span><span class="sxs-lookup"><span data-stu-id="2ef2b-112">Contains</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="2ef2b-113">Type d'interface</span><span class="sxs-lookup"><span data-stu-id="2ef2b-113">Interface type</span></span></td>
    <td><span data-ttu-id="2ef2b-114">Une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ef2b-114">One of the following values:</span></span><br/> <dl> <span data-ttu-id="2ef2b-115">Interne</span><span class="sxs-lookup"><span data-stu-id="2ef2b-115">Internal</span></span><br />
    <span data-ttu-id="2ef2b-116">ISA</span><span class="sxs-lookup"><span data-stu-id="2ef2b-116">Isa</span></span><br />
    <span data-ttu-id="2ef2b-117">EISA</span><span class="sxs-lookup"><span data-stu-id="2ef2b-117">Eisa</span></span><br />
    <span data-ttu-id="2ef2b-118">MICROCANAL</span><span class="sxs-lookup"><span data-stu-id="2ef2b-118">MicroChannel</span></span><br />
    <span data-ttu-id="2ef2b-119">TurboChannel</span><span class="sxs-lookup"><span data-stu-id="2ef2b-119">TurboChannel</span></span><br />
    <span data-ttu-id="2ef2b-120">PCIBus</span><span class="sxs-lookup"><span data-stu-id="2ef2b-120">PCIBus</span></span><br />
    <span data-ttu-id="2ef2b-121">VMEBus</span><span class="sxs-lookup"><span data-stu-id="2ef2b-121">VMEBus</span></span><br />
    <span data-ttu-id="2ef2b-122">NuBus</span><span class="sxs-lookup"><span data-stu-id="2ef2b-122">NuBus</span></span><br />
    <span data-ttu-id="2ef2b-123">PCMCIABus</span><span class="sxs-lookup"><span data-stu-id="2ef2b-123">PCMCIABus</span></span><br />
    <span data-ttu-id="2ef2b-124">CBus</span><span class="sxs-lookup"><span data-stu-id="2ef2b-124">CBus</span></span><br />
    <span data-ttu-id="2ef2b-125">MPIBus</span><span class="sxs-lookup"><span data-stu-id="2ef2b-125">MPIBus</span></span><br />
    <span data-ttu-id="2ef2b-126">MPSABus</span><span class="sxs-lookup"><span data-stu-id="2ef2b-126">MPSABus</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="2ef2b-127">Numéro de bus</span><span class="sxs-lookup"><span data-stu-id="2ef2b-127">Bus number</span></span></td>
    <td><span data-ttu-id="2ef2b-128">Entier spécifiant le numéro de bus.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-128">Integer specifying the bus number.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="2ef2b-129">Numéro de descripteur partiel</span><span class="sxs-lookup"><span data-stu-id="2ef2b-129">Partial descriptor number</span></span></td>
    <td><span data-ttu-id="2ef2b-130">Entier spécifiant le numéro du descripteur.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-130">Integer specifying the descriptor number.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="2ef2b-131">Type de décalage ou d’Union</span><span class="sxs-lookup"><span data-stu-id="2ef2b-131">Offset or union type</span></span></td>
    <td><span data-ttu-id="2ef2b-132">Une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ef2b-132">One of the following values:</span></span><br/> <dl> <span data-ttu-id="2ef2b-133">Port. Start</span><span class="sxs-lookup"><span data-stu-id="2ef2b-133">Port.Start</span></span><br />
    <span data-ttu-id="2ef2b-134">Port. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="2ef2b-134">Port.PhysicalAddress</span></span><br />
    <span data-ttu-id="2ef2b-135">Port. Length</span><span class="sxs-lookup"><span data-stu-id="2ef2b-135">Port.Length</span></span><br />
    <span data-ttu-id="2ef2b-136">Interrupt. niveau</span><span class="sxs-lookup"><span data-stu-id="2ef2b-136">Interrupt.Level</span></span><br />
    <span data-ttu-id="2ef2b-137">Interrupt. Vector</span><span class="sxs-lookup"><span data-stu-id="2ef2b-137">Interrupt.Vector</span></span><br />
    <span data-ttu-id="2ef2b-138">Interrupt. Affinity</span><span class="sxs-lookup"><span data-stu-id="2ef2b-138">Interrupt.Affinity</span></span><br />
    <span data-ttu-id="2ef2b-139">Memory. Start</span><span class="sxs-lookup"><span data-stu-id="2ef2b-139">Memory.Start</span></span><br />
    <span data-ttu-id="2ef2b-140">Memory. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="2ef2b-140">Memory.PhysicalAddress</span></span><br />
    <span data-ttu-id="2ef2b-141">Memory. Length</span><span class="sxs-lookup"><span data-stu-id="2ef2b-141">Memory.Length</span></span><br />
    <span data-ttu-id="2ef2b-142">DMA. Channel</span><span class="sxs-lookup"><span data-stu-id="2ef2b-142">Dma.Channel</span></span><br />
    <span data-ttu-id="2ef2b-143">DMA. port</span><span class="sxs-lookup"><span data-stu-id="2ef2b-143">Dma.Port</span></span><br />
    <span data-ttu-id="2ef2b-144">DMA. Reserved1</span><span class="sxs-lookup"><span data-stu-id="2ef2b-144">Dma.Reserved1</span></span><br />
    <span data-ttu-id="2ef2b-145">DeviceSpecificData. DataSize</span><span class="sxs-lookup"><span data-stu-id="2ef2b-145">DeviceSpecificData.DataSize</span></span><br />
    <span data-ttu-id="2ef2b-146">DeviceSpecificData. Reserved1</span><span class="sxs-lookup"><span data-stu-id="2ef2b-146">DeviceSpecificData.Reserved1</span></span><br />
    <span data-ttu-id="2ef2b-147">DeviceSpecificData. Reserved2</span><span class="sxs-lookup"><span data-stu-id="2ef2b-147">DeviceSpecificData.Reserved2</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="2ef2b-148">Placez la chaîne dans la clé appropriée sous la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-148">Place the string in the appropriate key under the registry key.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

<span data-ttu-id="2ef2b-149">L’exemple de code suivant décrit un descripteur de ressource valide.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-149">The following code example describes a valid resource descriptor.</span></span>

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

<span data-ttu-id="2ef2b-150">L’exemple de code suivant montre une syntaxe MOF valide pour la récupération d’un descripteur de ressource.</span><span class="sxs-lookup"><span data-stu-id="2ef2b-150">The following code example shows valid MOF syntax for retrieving a resource descriptor.</span></span>

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




