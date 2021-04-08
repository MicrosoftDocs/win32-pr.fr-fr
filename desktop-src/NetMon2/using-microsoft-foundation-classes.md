---
description: En raison de l’encombrement des DLL liées statiquement, évitez d’utiliser Microsoft Foundation Classes (MFCs) pour écrire un expert.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Utilisation de Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097c4baea2ec109933d52eed420042528e9eea76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757612"
---
# <a name="using-microsoft-foundation-classes"></a><span data-ttu-id="0a6bd-103">Utilisation de Microsoft Foundation Classes</span><span class="sxs-lookup"><span data-stu-id="0a6bd-103">Using Microsoft Foundation Classes</span></span>

<span data-ttu-id="0a6bd-104">En raison de l’encombrement des DLL liées statiquement, évitez d’utiliser Microsoft Foundation Classes (MFCs) pour écrire un expert.</span><span class="sxs-lookup"><span data-stu-id="0a6bd-104">Because of the footprint of statically linked DLLs, you should avoid using Microsoft Foundation Classes (MFCs) to write an expert.</span></span> <span data-ttu-id="0a6bd-105">Toutefois, si vous utilisez les MFC, veillez à accéder à toutes les ressources DLL MFC en incluant le code suivant immédiatement à l’entrée :</span><span class="sxs-lookup"><span data-stu-id="0a6bd-105">However, if you use the MFC, ensure access to any of the MFC DLL resources by including the following code immediately upon entry:</span></span>

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



