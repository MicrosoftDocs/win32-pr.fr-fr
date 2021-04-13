---
title: Configuration des compresseurs et des décompresseurs
description: Configuration des compresseurs et des décompresseurs
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- Gestionnaire de compression vidéo (VCM), configuration des compresseurs
- VCM (gestionnaire de compression vidéo), configuration des compresseurs
- ICQueryConfigure macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d388a52047a1aea7936cc494dafc0d1a2d6dec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379865"
---
# <a name="configuring-compressors-and-decompressors"></a><span data-ttu-id="a6325-106">Configuration des compresseurs et des décompresseurs</span><span class="sxs-lookup"><span data-stu-id="a6325-106">Configuring Compressors and Decompressors</span></span>

<span data-ttu-id="a6325-107">L’exemple suivant utilise la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) pour montrer comment tester si un compresseur prend en charge la boîte de dialogue de configuration et pour l’afficher si c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="a6325-107">The following example uses the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro to demonstrate how to test whether a compressor supports the configuration dialog box and to display it if it does.</span></span>


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



<span data-ttu-id="a6325-108">L’exemple suivant montre comment obtenir les données d’État à l’aide de la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .</span><span class="sxs-lookup"><span data-stu-id="a6325-108">The following example shows how to obtain the state data using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



<span data-ttu-id="a6325-109">L’exemple suivant montre comment restaurer des données d’État à l’aide de la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .</span><span class="sxs-lookup"><span data-stu-id="a6325-109">The following example shows how to restore state data using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span> <span data-ttu-id="a6325-110">Les données d’État restaurées par les applications ne doivent pas contenir de modifications des données d’État obtenues à partir d’un pilote.</span><span class="sxs-lookup"><span data-stu-id="a6325-110">State data restored by applications should not contain any changes to the state data obtained from a driver.</span></span>


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




