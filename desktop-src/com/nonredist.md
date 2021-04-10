---
title: Pas de REDIM
description: Ajoute des noms à la liste des fichiers qui ne doivent pas être exportés lorsque les applications COM+ sont empaquetées pour être installées sur d’autres ordinateurs. Notez qu’il s’agit d’une sous-clé, et non d’une valeur.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Valeur de Registre inversée COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029901"
---
# <a name="nonredist"></a><span data-ttu-id="3d828-105">Pas de REDIM</span><span class="sxs-lookup"><span data-stu-id="3d828-105">NONREDIST</span></span>

<span data-ttu-id="3d828-106">Ajoute des noms à la liste des fichiers qui ne doivent pas être exportés lorsque les applications COM+ sont empaquetées pour être installées sur d’autres ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="3d828-106">Adds names to the list of files that should not be exported when COM+ applications are packaged for installation on other computers.</span></span> <span data-ttu-id="3d828-107">Notez qu’il s’agit d’une sous-clé, et non d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="3d828-107">Note that this is a subkey, not a value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3d828-108">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="3d828-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a><span data-ttu-id="3d828-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3d828-109">Remarks</span></span>

<span data-ttu-id="3d828-110">Les fichiers que vous ajoutez à la liste sont représentés par des paires nom/valeur stockées sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="3d828-110">The files you add to the list are represented by name/value pairs stored under this key.</span></span> <span data-ttu-id="3d828-111">Dans chaque paire nom/valeur, le nom est le nom de fichier et la valeur est réservée.</span><span class="sxs-lookup"><span data-stu-id="3d828-111">In each name/value pair, the name is the file name and the value is reserved.</span></span>

 

 




