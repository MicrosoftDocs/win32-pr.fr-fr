---
title: ToolBoxBitmap32
description: Identifie le nom de module et l’ID de ressource pour une image bitmap de 16 x 16 à utiliser pour la face d’un bouton de barre d’outils ou de boîte à outils.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- Clé de Registre ToolBoxBitmap32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029032"
---
# <a name="toolboxbitmap32"></a><span data-ttu-id="3b976-104">ToolBoxBitmap32</span><span class="sxs-lookup"><span data-stu-id="3b976-104">ToolBoxBitmap32</span></span>

<span data-ttu-id="3b976-105">Identifie le nom de module et l’ID de ressource pour une image bitmap de 16 x 16 à utiliser pour la face d’un bouton de barre d’outils ou de boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="3b976-105">Identifies the module name and resource ID for a 16 x 16 bitmap to use for the face of a toolbar or toolbox button.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3b976-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="3b976-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a><span data-ttu-id="3b976-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3b976-107">Remarks</span></span>

<span data-ttu-id="3b976-108">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le nom du module et l’identificateur de ressource pour l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="3b976-108">This is a **REG\_SZ** value that specifies the module name and resource identifier for the bitmap.</span></span>

<span data-ttu-id="3b976-109">La taille de l’icône Windows standard est trop grande pour être utilisée à cet effet.</span><span class="sxs-lookup"><span data-stu-id="3b976-109">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="3b976-110">Cela requiert des conteneurs de contrôle qui ont un mode création dans lequel l’un sélectionne des contrôles et les place sur un formulaire en cours de conception.</span><span class="sxs-lookup"><span data-stu-id="3b976-110">This requires control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span>

 

 




