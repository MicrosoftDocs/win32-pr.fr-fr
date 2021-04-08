---
title: SRPActivateAsActivatorChecks
description: Détermine si les niveaux de confiance de la stratégie de restriction logicielle (SRP) sont utilisés lors des activations de ActivateAsActivator.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- Valeur de Registre SRPActivateAsActivatorChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672489"
---
# <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="28f58-104">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="28f58-104">SRPActivateAsActivatorChecks</span></span>

<span data-ttu-id="28f58-105">Détermine si les niveaux de confiance de la stratégie de restriction logicielle (SRP) sont utilisés lors des activations de ActivateAsActivator.</span><span class="sxs-lookup"><span data-stu-id="28f58-105">Determines whether software restriction policy (SRP) trust levels are used during ActivateAsActivator activations.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="28f58-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="28f58-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a><span data-ttu-id="28f58-107">Notes</span><span class="sxs-lookup"><span data-stu-id="28f58-107">Remarks</span></span>

<span data-ttu-id="28f58-108">Il s’agit d’une valeur de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="28f58-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="28f58-109">Les valeurs de chaîne {N, n, NO, no} indiquent que l’objet serveur s’exécute avec le niveau de confiance SRP de l’objet client, quel que soit le niveau de confiance du SRP avec lequel il a été configuré.</span><span class="sxs-lookup"><span data-stu-id="28f58-109">String values of {N, n, NO, No, no} indicate that the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which it was configured.</span></span> <span data-ttu-id="28f58-110">Si cette valeur de Registre est définie sur une autre valeur ou n’existe pas, le niveau de confiance SRP configuré pour l’objet serveur est comparé au niveau de confiance SRP de l’objet client et le niveau de confiance le plus strict est utilisé pour exécuter l’objet serveur.</span><span class="sxs-lookup"><span data-stu-id="28f58-110">If this registry value is set to any other value or does not exist, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and that the more stringent trust level is used to run the server object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28f58-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28f58-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f58-112">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="28f58-112">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




