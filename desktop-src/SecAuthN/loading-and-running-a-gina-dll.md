---
description: Windows charge et exécute la DLL Microsoft GINA standard (MSGina.dll). Pour charger une autre GINA, vous devez modifier une valeur de clé de registre.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Chargement et exécution d’une DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531712"
---
# <a name="loading-and-running-a-gina-dll"></a><span data-ttu-id="8e8f7-104">Chargement et exécution d’une DLL GINA</span><span class="sxs-lookup"><span data-stu-id="8e8f7-104">Loading and Running a GINA DLL</span></span>

<span data-ttu-id="8e8f7-105">Windows charge et exécute la DLL Microsoft GINA standard (MSGina.dll).</span><span class="sxs-lookup"><span data-stu-id="8e8f7-105">Windows loads and executes the standard Microsoft GINA DLL (MSGina.dll).</span></span> <span data-ttu-id="8e8f7-106">Pour charger une autre [*Gina*](../secgloss/g-gly.md), vous devez modifier la valeur de clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="8e8f7-106">To load a different [*GINA*](../secgloss/g-gly.md), you must alter the following registry key value:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

<span data-ttu-id="8e8f7-107">Si la valeur de clé GinaDLL est présente, elle doit contenir le nom d’une DLL GINA, que [*Winlogon*](../secgloss/w-gly.md) chargera et utilise.</span><span class="sxs-lookup"><span data-stu-id="8e8f7-107">If the GinaDLL key value is present, it must contain the name of a GINA DLL, which [*Winlogon*](../secgloss/w-gly.md) will load and use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e8f7-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e8f7-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e8f7-109">Génération et test d’une DLL GINA</span><span class="sxs-lookup"><span data-stu-id="8e8f7-109">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="8e8f7-110">Fonctions d’exportation GINA</span><span class="sxs-lookup"><span data-stu-id="8e8f7-110">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="8e8f7-111">Structures GINA</span><span class="sxs-lookup"><span data-stu-id="8e8f7-111">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="8e8f7-112">Fonctions GINA des services Terminal Server</span><span class="sxs-lookup"><span data-stu-id="8e8f7-112">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
