---
title: Attachement à l’ordinateur SDO
description: Avec le pointeur d’interface retourné par CoCreateInstance, appelez la méthode d’attachement ISdoMachine.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941066"
---
# <a name="attaching-to-the-sdo-computer"></a><span data-ttu-id="d7b59-103">Attachement à l’ordinateur SDO</span><span class="sxs-lookup"><span data-stu-id="d7b59-103">Attaching to the SDO Computer</span></span>

<span data-ttu-id="d7b59-104">Avec le pointeur d’interface retourné par [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), appelez la méthode [**ISdoMachine :: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) .</span><span class="sxs-lookup"><span data-stu-id="d7b59-104">With the interface pointer returned by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), call the [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) method.</span></span> <span data-ttu-id="d7b59-105">Passer **null** comme paramètre à la méthode **Attach** .</span><span class="sxs-lookup"><span data-stu-id="d7b59-105">Pass **NULL** as the parameter to the **Attach** method.</span></span> <span data-ttu-id="d7b59-106">La valeur **null** spécifie que **Attach** associe l’objet ordinateur à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d7b59-106">The value **NULL** specifies that **Attach** associate the machine object with the local computer.</span></span> <span data-ttu-id="d7b59-107">L’attachement à un ordinateur distant n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d7b59-107">Attaching to a remote computer is not supported.</span></span>

<span data-ttu-id="d7b59-108">Pour déterminer si l’ordinateur local est déjà attaché, appelez la méthode [**ISdoMachine :: GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .</span><span class="sxs-lookup"><span data-stu-id="d7b59-108">To determine if the local computer is already attached, call the [**ISdoMachine::GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) method.</span></span>

<span data-ttu-id="d7b59-109">Consultez [attachement à un ordinateur SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) pour obtenir un exemple de code qui montre comment s’attacher à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d7b59-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to attach to the local computer.</span></span>

 

 