---
title: Contrôler
description: Identifie un objet en tant que contrôle ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Clé de registre de contrôle COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380383"
---
# <a name="control"></a><span data-ttu-id="68489-104">Contrôler</span><span class="sxs-lookup"><span data-stu-id="68489-104">Control</span></span>

<span data-ttu-id="68489-105">Identifie un objet en tant que contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="68489-105">Identifies an object as an ActiveX Control.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="68489-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="68489-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a><span data-ttu-id="68489-107">Notes</span><span class="sxs-lookup"><span data-stu-id="68489-107">Remarks</span></span>

<span data-ttu-id="68489-108">Cette entrée facultative est utilisée par les conteneurs pour renseigner les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="68489-108">This optional entry is used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="68489-109">Le conteneur utilise cette sous-clé pour déterminer s’il faut inclure un objet dans une boîte de dialogue qui affiche des contrôles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="68489-109">The container uses this subkey to determine whether to include an object in a dialog box that displays ActiveX Controls.</span></span> <span data-ttu-id="68489-110">Un contrôle peut omettre cette entrée s’il est conçu pour fonctionner uniquement avec un conteneur spécifique et n’est donc pas destiné à être inséré dans d’autres conteneurs.</span><span class="sxs-lookup"><span data-stu-id="68489-110">A control can omit this entry if it is designed to work only with a specific container and therefore does is not intended to be inserted in other containers.</span></span>

 

 




