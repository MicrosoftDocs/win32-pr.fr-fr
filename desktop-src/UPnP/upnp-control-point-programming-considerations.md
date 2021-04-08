---
title: Considérations sur la programmation des points de contrôle
description: Les développeurs qui créent des applications basées sur UPnP (ou des points de contrôle) doivent utiliser ces applications à partir d’un \_ client APARTMENTTHREADED coinit. Il existe des problèmes connus lors de l’utilisation de l’API de point de contrôle à partir d’un \_ client multithread coinit s’exécutant sous stress.
ms.assetid: a5d79a29-4192-40af-b75d-a31f1f46149c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76955177f9fc0c3b164d84998547c1afdfbfb4bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840549"
---
# <a name="control-point-programming-considerations"></a><span data-ttu-id="7808e-104">Considérations sur la programmation des points de contrôle</span><span class="sxs-lookup"><span data-stu-id="7808e-104">Control Point Programming Considerations</span></span>

<span data-ttu-id="7808e-105">Les développeurs qui créent des applications basées sur UPnP (ou des points de contrôle) doivent utiliser ces applications à partir d’un \_ client APARTMENTTHREADED coinit.</span><span class="sxs-lookup"><span data-stu-id="7808e-105">Developers who create UPnP-based applications (or control points) must use these applications from a COINIT\_APARTMENTTHREADED client.</span></span> <span data-ttu-id="7808e-106">Il existe des problèmes connus lors de l’utilisation de l’API de point de contrôle à partir d’un \_ client multithread coinit s’exécutant sous stress.</span><span class="sxs-lookup"><span data-stu-id="7808e-106">There are known problems when using the Control Point API from a COINIT\_MULTITHREADED client running under stress.</span></span>

 

 




