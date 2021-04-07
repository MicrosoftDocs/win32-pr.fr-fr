---
title: AuxUserType
description: Spécifie le nom complet et les noms d’application de l’application.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- Clé de Registre AuxUserType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670889"
---
# <a name="auxusertype"></a><span data-ttu-id="c0178-104">AuxUserType</span><span class="sxs-lookup"><span data-stu-id="c0178-104">AuxUserType</span></span>

<span data-ttu-id="c0178-105">Spécifie le nom complet et les noms d’application de l’application.</span><span class="sxs-lookup"><span data-stu-id="c0178-105">Specifies an application's short display name and application names.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c0178-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="c0178-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a><span data-ttu-id="c0178-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c0178-107">Remarks</span></span>

<span data-ttu-id="c0178-108">La longueur maximale recommandée pour *ShortDisplayName* est de 15 caractères.</span><span class="sxs-lookup"><span data-stu-id="c0178-108">The recommended maximum length for *ShortDisplayName* is 15 characters.</span></span> <span data-ttu-id="c0178-109">Ce nom est utilisé dans les menus, y compris les menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="c0178-109">This name is used in menus, including pop-up menus.</span></span>

<span data-ttu-id="c0178-110">*ApplicationName* doit contenir le nom réel de l’application (par exemple, « Acme Draw 2,0 »).</span><span class="sxs-lookup"><span data-stu-id="c0178-110">*ApplicationName* should contain the actual name of the application (such as "Acme Draw 2.0").</span></span> <span data-ttu-id="c0178-111">Ce nom est utilisé dans le champ **résultats** de la boîte de dialogue **Collage spécial** .</span><span class="sxs-lookup"><span data-stu-id="c0178-111">This name is used in the **Results** field of the **Paste Special** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0178-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0178-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0178-113">**IOleObject :: GetUserType**</span><span class="sxs-lookup"><span data-stu-id="c0178-113">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




