---
title: Considérations sur la programmation de MGM
description: Lorsque vous développez des clients du gestionnaire de groupe de multidiffusion, observez les instructions suivantes
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multidiffusion, considérations de programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840389"
---
# <a name="mgm-programming-considerations"></a><span data-ttu-id="4f133-104">Considérations sur la programmation de MGM</span><span class="sxs-lookup"><span data-stu-id="4f133-104">MGM Programming Considerations</span></span>

<span data-ttu-id="4f133-105">Lorsque vous développez des clients du gestionnaire de groupe de multidiffusion, observez les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f133-105">When you are developing multicast group manager clients, observe the following guidelines:</span></span>

-   <span data-ttu-id="4f133-106">Les appels de fonction doivent être effectués à partir du processus de routeur.</span><span class="sxs-lookup"><span data-stu-id="4f133-106">Function calls must be made from within the router process.</span></span> <span data-ttu-id="4f133-107">Si les fonctions sont appelées à partir d’un autre processus, leurs résultats ne seront pas valides ; le client n’interagit pas avec le gestionnaire de groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="4f133-107">If functions are called from another process, their results will not be valid; the client will not interact with the multicast group manager.</span></span>
-   <span data-ttu-id="4f133-108">Les clients qui utilisent l’API MGM doivent fournir leur propre vérification des erreurs, garantissant que seules les données valides sont transmises au gestionnaire de groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="4f133-108">Clients that use the MGM API must provide their own error checking, ensuring that only valid data is passed to the multicast group manager.</span></span> <span data-ttu-id="4f133-109">Les fonctions MGM ne retournent pas de messages d’erreur détaillés sur les paramètres non valides ; la \_ valeur du paramètre non valide de l’erreur \_ est retournée sans explication.</span><span class="sxs-lookup"><span data-stu-id="4f133-109">MGM functions do not return detailed error messages about invalid parameters; the ERROR\_INVALID\_PARAMETER value is returned without explanation.</span></span>
-   <span data-ttu-id="4f133-110">Les clients doivent faire preuve de prudence lors de l’utilisation de verrous lors de l’appel de fonctions MGM.</span><span class="sxs-lookup"><span data-stu-id="4f133-110">Clients should exercise caution in using locks while calling MGM functions.</span></span> <span data-ttu-id="4f133-111">Cela peut empêcher les blocages.</span><span class="sxs-lookup"><span data-stu-id="4f133-111">Doing so can prevent deadlocks.</span></span> <span data-ttu-id="4f133-112">Lors de l’appel de fonctions MGM, les clients ne doivent pas contenir de verrous qui peuvent être maintenus simultanément dans un rappel du gestionnaire de groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="4f133-112">When calling MGM functions, clients should not hold any locks that might simultaneously be held in a callback from the multicast group manager.</span></span>

 

 




