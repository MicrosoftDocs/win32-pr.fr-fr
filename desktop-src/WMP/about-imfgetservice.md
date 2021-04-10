---
title: À propos de IMFGetService
description: À propos de IMFGetService
ms.assetid: c71b1362-a596-42e5-b894-f8a3c0e70140
keywords:
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
- Plug-ins du lecteur Windows Media, interface IMFGetService
- plug-ins, interface IMFGetService
- plug-ins de traitement de signal numérique, interface IMFGetService
- Plug-ins DSP, interface IMFGetService
- Interface IMFGetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235b616afe48db9ae772da1f1d74c4f7de1a74a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309374"
---
# <a name="about-imfgetservice"></a><span data-ttu-id="033e1-113">À propos de IMFGetService</span><span class="sxs-lookup"><span data-stu-id="033e1-113">About IMFGetService</span></span>

<span data-ttu-id="033e1-114">L’interface **IMFGetService** est l’une des interfaces qui doivent être implémentées par un plug-in DSP à double mode.</span><span class="sxs-lookup"><span data-stu-id="033e1-114">The **IMFGetService** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="033e1-115">Il n’a qu’une seule méthode, **GetService**.</span><span class="sxs-lookup"><span data-stu-id="033e1-115">It has only one method, **GetService**.</span></span> <span data-ttu-id="033e1-116">Un plug-in DSP implémente la méthode **GetService** afin que les clients puissent obtenir des pointeurs vers les interfaces prises en charge par le plug-in lorsque le plug-in s’exécute en mode natif dans le pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="033e1-116">A DSP plug-in implements the **GetService** method so that clients can obtain pointers to the interfaces supported by the plug-in when the plug-in is running natively in the Media Foundation pipeline.</span></span>

 

 




