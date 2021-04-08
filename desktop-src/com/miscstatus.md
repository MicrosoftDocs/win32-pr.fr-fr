---
title: MiscStatus
description: Spécifie comment créer et afficher un objet.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- Clé de Registre MiscStatus COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029438"
---
# <a name="miscstatus"></a><span data-ttu-id="35d59-104">MiscStatus</span><span class="sxs-lookup"><span data-stu-id="35d59-104">MiscStatus</span></span>

<span data-ttu-id="35d59-105">Spécifie comment créer et afficher un objet.</span><span class="sxs-lookup"><span data-stu-id="35d59-105">Specifies how to create and display an object.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="35d59-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="35d59-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a><span data-ttu-id="35d59-107">Notes</span><span class="sxs-lookup"><span data-stu-id="35d59-107">Remarks</span></span>

<span data-ttu-id="35d59-108">Pour plus d’informations, consultez l’énumération [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) et [**IOleObject :: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span><span class="sxs-lookup"><span data-stu-id="35d59-108">For more information, see the [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) enumeration and [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span></span>

<span data-ttu-id="35d59-109">Si aucune sous-clé correspondant à un DVASPECT n’est trouvée, la valeur par défaut de **MiscStatus** est utilisée.</span><span class="sxs-lookup"><span data-stu-id="35d59-109">If no subkey that corresponds to a DVASPECT is found, the default value of **MiscStatus** is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35d59-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35d59-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35d59-111">**IOleObject :: GetMiscStatus**</span><span class="sxs-lookup"><span data-stu-id="35d59-111">**IOleObject::GetMiscStatus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




