---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Détermine si RPCSS ajoute automatiquement un SID tous \_ les \_ packages d’application aux restrictions com par défaut.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379668"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a><span data-ttu-id="8245a-103">DoNotAddAllApplicationPackagesToRestrictions</span><span class="sxs-lookup"><span data-stu-id="8245a-103">DoNotAddAllApplicationPackagesToRestrictions</span></span>

<span data-ttu-id="8245a-104">Détermine si RPCSS ajoute automatiquement un SID tous \_ les \_ packages d’application aux restrictions com par défaut.</span><span class="sxs-lookup"><span data-stu-id="8245a-104">Determines whether RPCSS automatically appends an ALL\_APPLICATION\_PACKAGES SID to COM restrictions by default.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8245a-105">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="8245a-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a><span data-ttu-id="8245a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="8245a-106">Remarks</span></span>

<span data-ttu-id="8245a-107">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8245a-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="8245a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8245a-108">Value</span></span> | <span data-ttu-id="8245a-109">Description</span><span class="sxs-lookup"><span data-stu-id="8245a-109">Description</span></span>                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8245a-110">0</span><span class="sxs-lookup"><span data-stu-id="8245a-110">0</span></span>     | <span data-ttu-id="8245a-111">Désactive les applications du Windows Store lors de la migration de Windows 7 vers Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8245a-111">Disables Windows Store apps upon migration from Windows 7 to Windows 8.</span></span>                   |
| <span data-ttu-id="8245a-112">1</span><span class="sxs-lookup"><span data-stu-id="8245a-112">1</span></span>     | <span data-ttu-id="8245a-113">N’ajoute pas le SID tous les \_ \_ packages d’application aux restrictions com.</span><span class="sxs-lookup"><span data-stu-id="8245a-113">Does not add the ALL\_APPLICATION\_PACKAGES SID to COM restrictions.</span></span> <span data-ttu-id="8245a-114">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8245a-114">This is the default.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8245a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8245a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8245a-116">Définition de la sécurité pour les applications COM</span><span class="sxs-lookup"><span data-stu-id="8245a-116">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




