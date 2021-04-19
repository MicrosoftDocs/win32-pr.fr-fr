---
title: Interface (COM)
description: Entrée facultative qui spécifie tous les ID d’interface (IID) pris en charge par la classe associée.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Clé de registre de l’interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511117"
---
# <a name="interface-com"></a><span data-ttu-id="da0ad-104">Interface (COM)</span><span class="sxs-lookup"><span data-stu-id="da0ad-104">Interface (COM)</span></span>

<span data-ttu-id="da0ad-105">Entrée facultative qui spécifie tous les ID d’interface (IID) pris en charge par la classe associée.</span><span class="sxs-lookup"><span data-stu-id="da0ad-105">An optional entry that specifies all interface IDs (IIDs) supported by the associated class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="da0ad-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="da0ad-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a><span data-ttu-id="da0ad-107">Notes</span><span class="sxs-lookup"><span data-stu-id="da0ad-107">Remarks</span></span>

<span data-ttu-id="da0ad-108">Si un nom d’interface n’est pas présent dans cette liste, l’interface ne peut jamais être prise en charge par une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="da0ad-108">If an interface name is not present in this list, the interface can never be supported by an instance of this class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da0ad-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da0ad-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da0ad-110">Clé d'interface</span><span class="sxs-lookup"><span data-stu-id="da0ad-110">Interface Key</span></span>](interface-key.md)
</dt> </dl>

 

 




