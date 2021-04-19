---
description: Un processus peut appeler WSPCloseSocket sur un socket dupliqué et le descripteur est libéré. Toutefois, le Socket sous-jacent reste ouvert jusqu’à ce que WSPCloseSocket soit appelé sur le dernier descripteur restant.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Décompte de références
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72d9ef7b3e5e31cc7941d30c47f107fc068489ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517614"
---
# <a name="reference-counting"></a><span data-ttu-id="a9f3e-104">Décompte de références</span><span class="sxs-lookup"><span data-stu-id="a9f3e-104">Reference Counting</span></span>

<span data-ttu-id="a9f3e-105">Un processus peut appeler [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) sur un socket dupliqué et le descripteur est libéré.</span><span class="sxs-lookup"><span data-stu-id="a9f3e-105">A process may call [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) on a duplicated socket and the descriptor will become deallocated.</span></span> <span data-ttu-id="a9f3e-106">Toutefois, le Socket sous-jacent reste ouvert jusqu’à ce que **WSPCloseSocket** soit appelé sur le dernier descripteur restant.</span><span class="sxs-lookup"><span data-stu-id="a9f3e-106">The underlying socket, however, will remain open until **WSPCloseSocket** is called on the last remaining descriptor.</span></span>

 

 
