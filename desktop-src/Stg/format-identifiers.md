---
title: Identificateurs de format
description: Les valeurs de jeu de propriétés sont stockées dans une section marquée avec un FMTID unique.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificateurs de format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309813"
---
# <a name="format-identifiers"></a><span data-ttu-id="23fba-104">Identificateurs de format</span><span class="sxs-lookup"><span data-stu-id="23fba-104">Format Identifiers</span></span>

<span data-ttu-id="23fba-105">Les valeurs de jeu de propriétés sont stockées dans une section marquée avec un FMTID unique.</span><span class="sxs-lookup"><span data-stu-id="23fba-105">Property set values are stored in a section tagged with a unique FMTID.</span></span> <span data-ttu-id="23fba-106">Par exemple, le FMTID pour la propriété informations résumées COM définie est **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span><span class="sxs-lookup"><span data-stu-id="23fba-106">For example, the FMTID for the COM Summary Information property set is **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span></span>

<span data-ttu-id="23fba-107">Pour définir un FMTID pour le jeu de propriétés d’informations de synthèse, utilisez la macro **définir le \_ GUID** dans un fichier include pour le code qui manipule le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="23fba-107">To define a FMTID for the Summary Information property set, use the **DEFINE\_GUID** macro in an include file for the code that manipulates the property set.</span></span>


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



<span data-ttu-id="23fba-108">Tout code qui requiert FMTID pour le jeu de propriétés d’informations de synthèse peut y accéder via la variable *fmtid \_ SummaryInformation* .</span><span class="sxs-lookup"><span data-stu-id="23fba-108">Any code that requires the FMTID for the Summary Information property set, can access it through the *FMTID\_SummaryInformation* variable.</span></span>

<span data-ttu-id="23fba-109">Lors du stockage de jeux de propriétés dans des instances de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , convertissez le fmtid en un nom de chaîne pour l’objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="23fba-109">When storing property sets in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instances, convert the FMTID to a string name for the storage object.</span></span>

 

 




