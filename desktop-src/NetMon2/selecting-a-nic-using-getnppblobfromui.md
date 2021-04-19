---
description: Avec Moniteur réseau, la sélection d’une carte réseau par programmation est un processus en deux étapes. Tout d’abord, créez l’objet BLOB de filtre en appelant la méthode CreateBlob. Ensuite, sélectionnez la carte réseau en appelant la méthode GetNPPBlobFromUI.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Sélection d’une carte réseau à l’aide de GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb429a87d284a5a6a03a20357728c8bbcb5acac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517305"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a><span data-ttu-id="5d1aa-105">Sélection d’une carte réseau à l’aide de GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="5d1aa-105">Selecting a NIC Using GetNPPBlobFromUI</span></span>

<span data-ttu-id="5d1aa-106">Avec Moniteur réseau, la sélection d’une carte réseau par programmation est un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="5d1aa-106">With Network Monitor, selecting a NIC programmatically is a two-step process.</span></span> <span data-ttu-id="5d1aa-107">Tout d’abord, créez l’objet BLOB de filtre en appelant la méthode [**CreateBlob**](createblob.md) .</span><span class="sxs-lookup"><span data-stu-id="5d1aa-107">First, create the filter BLOB by calling the [**CreateBlob**](createblob.md) method.</span></span> <span data-ttu-id="5d1aa-108">Ensuite, sélectionnez la carte réseau en appelant la méthode [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="5d1aa-108">Then, select the NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) method.</span></span>

<span data-ttu-id="5d1aa-109">Dans cet exemple, un objet BLOB de filtre est utilisé pour sélectionner la carte réseau requise :</span><span class="sxs-lookup"><span data-stu-id="5d1aa-109">In this example a filter BLOB is used to select the required NIC:</span></span>


```C++
DWORD rc;

// Call CreateBlob to create a filter blob.
///////////////////////////////////////////
HBLOB hFilterBlob;
rc = CreateBlob(&hFilterBlob);
if (FAILED (rc));
{
  // Failed creating filter BLOB. Add appropriate error handling.
}


// Call GetNPPBlobFromUI to retrieve the NPP Blob.
//////////////////////////////////////////////////
rc = GetNPPBlobFromUI(hwnd,
                      hFilterBlob,
                      &hBlob);
if (FAILED (rc));
{
  // Failed retrieving NPP BLOB. Add appropriate error handling.
}
```



 

 



