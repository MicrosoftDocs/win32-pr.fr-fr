---
title: SRPRunningObjectChecks
description: Détermine si les tentatives de connexion aux objets en cours d’exécution sont filtrées pour les niveaux de confiance de stratégie de restriction logicielle (SRP) compatibles.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valeur de Registre SRPRunningObjectChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672486"
---
# <a name="srprunningobjectchecks"></a><span data-ttu-id="9469a-104">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="9469a-104">SRPRunningObjectChecks</span></span>

<span data-ttu-id="9469a-105">Détermine si les tentatives de connexion aux objets en cours d’exécution sont filtrées pour les niveaux de confiance de stratégie de restriction logicielle (SRP) compatibles.</span><span class="sxs-lookup"><span data-stu-id="9469a-105">Determines whether attempts to connect to running objects are screened for compatible software restriction policy (SRP) trust levels.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="9469a-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="9469a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a><span data-ttu-id="9469a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9469a-107">Remarks</span></span>

<span data-ttu-id="9469a-108">Il s’agit d’une valeur de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="9469a-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="9469a-109">Les valeurs de chaîne {N, n, NO, no} indiquent que les tentatives de connexion aux objets en cours d’exécution ne sont pas filtrées pour les niveaux de confiance SRP compatibles.</span><span class="sxs-lookup"><span data-stu-id="9469a-109">String values of {N, n, NO, No, no} indicate that attempts to connect to running objects are not screened for compatible SRP trust levels.</span></span> <span data-ttu-id="9469a-110">Si cette valeur de Registre est définie sur une autre valeur ou n’existe pas, l’objet en cours d’exécution ne peut pas avoir un niveau de confiance SRP moins strict que l’objet client.</span><span class="sxs-lookup"><span data-stu-id="9469a-110">If this registry value is set to any other value or does not exist, the running object cannot have a less stringent SRP trust level than the client object.</span></span> <span data-ttu-id="9469a-111">Par exemple, l’objet en cours d’exécution ne peut pas avoir un niveau de confiance non autorisé si l’objet client a un niveau de confiance illimité.</span><span class="sxs-lookup"><span data-stu-id="9469a-111">For example, the running object cannot have a Disallowed trust level if the client object has an Unrestricted trust level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9469a-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9469a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9469a-113">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="9469a-113">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




