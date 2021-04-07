---
title: Exemple de diagnostics NDF
description: L’exemple suivant montre comment lancer l’interface utilisateur NDF et diagnostiquer la connectivité au site Web http//www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fca4d54519988c3182b50a7c304f9c76a86392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029070"
---
# <a name="ndf-diagnostics-example"></a><span data-ttu-id="62dff-103">Exemple de diagnostics NDF</span><span class="sxs-lookup"><span data-stu-id="62dff-103">NDF Diagnostics Example</span></span>

<span data-ttu-id="62dff-104">L’exemple suivant montre comment lancer l’interface utilisateur NDF et diagnostiquer la connectivité au site Web https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="62dff-104">The following example shows how to launch the NDF user interface and diagnose connectivity to the website https://www.microsoft.com.</span></span>


```C++
#include "ndfapi.h"

NDFHANDLE hNDF;
HRESULT hr = NdfCreateWebIncident (
                    L"https://www.microsoft.com",
                    &hNDF);

if(SUCCEEDED(hr))
{
    NdfExecuteDiagnosis(hNDF, NULL); // launches the NDF UI
                                     // the UI is not modal to the original window
    NdfCloseIncident(hNDF);
}
```



<span data-ttu-id="62dff-105">L’interface utilisateur NDF peut être lancée sous la forme d’une fenêtre modale.</span><span class="sxs-lookup"><span data-stu-id="62dff-105">The NDF UI can be launched as a modal window.</span></span> <span data-ttu-id="62dff-106">Pour ce faire, remplacez le deuxième paramètre de [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) par **null** par le handle (HWND) de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="62dff-106">To do so, change the second parameter of [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) from **NULL** to the handle (HWND) of the parent window.</span></span>

<span data-ttu-id="62dff-107">Cet exemple peut être modifié pour diagnostiquer d’autres zones de la mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="62dff-107">This example can be modified to diagnose other areas of networking.</span></span> <span data-ttu-id="62dff-108">Pour ce faire, remplacez l’appel [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) par l’une des autres fonctions de création d’incident, telles que [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) ou [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span><span class="sxs-lookup"><span data-stu-id="62dff-108">To do so, replace the [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) call with one of the other incident creation functions, such as [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) or [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62dff-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62dff-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62dff-110">**NdfCloseIncident**</span><span class="sxs-lookup"><span data-stu-id="62dff-110">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[<span data-ttu-id="62dff-111">**NdfCreateWebIncident**</span><span class="sxs-lookup"><span data-stu-id="62dff-111">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[<span data-ttu-id="62dff-112">**NdfExecuteDiagnosis**</span><span class="sxs-lookup"><span data-stu-id="62dff-112">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




