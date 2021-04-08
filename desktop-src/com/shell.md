---
title: Shell (COM)
description: Fournit les informations d’impression et d’ouverture de fichier du shell Windows 3,1.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Clé de Registre Shell COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739348"
---
# <a name="shell-com"></a><span data-ttu-id="7a5c1-104">Shell (COM)</span><span class="sxs-lookup"><span data-stu-id="7a5c1-104">Shell (COM)</span></span>

<span data-ttu-id="7a5c1-105">Fournit les informations d’impression et d' **ouverture de fichier** du shell Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="7a5c1-105">Provides Windows 3.1 shell printing and **File Open** information.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7a5c1-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="7a5c1-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a><span data-ttu-id="7a5c1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7a5c1-107">Remarks</span></span>

<span data-ttu-id="7a5c1-108">Ces entrées doivent fournir le chemin d’accès et le nom de fichier de l’application.</span><span class="sxs-lookup"><span data-stu-id="7a5c1-108">These entries should provide the path and file name of the application.</span></span>

 

 




