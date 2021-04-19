---
title: Protocol
description: Indique que cette classe OLE 2 peut être insérée dans les conteneurs OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Clé de Registre du protocole COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511441"
---
# <a name="protocol"></a><span data-ttu-id="1e594-104">Protocol</span><span class="sxs-lookup"><span data-stu-id="1e594-104">Protocol</span></span>

<span data-ttu-id="1e594-105">Indique que cette classe OLE 2 peut être insérée dans les conteneurs OLE 1.</span><span class="sxs-lookup"><span data-stu-id="1e594-105">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1e594-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="1e594-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a><span data-ttu-id="1e594-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1e594-107">Remarks</span></span>

<span data-ttu-id="1e594-108">L’entrée **StdFileEditing** spécifie les informations de compatibilité OLE 1.</span><span class="sxs-lookup"><span data-stu-id="1e594-108">The **StdFileEditing** entry specifies OLE 1 compatibility information.</span></span> <span data-ttu-id="1e594-109">Elle doit être présente uniquement si les objets de cette classe peuvent être insérés dans des conteneurs OLE 1.</span><span class="sxs-lookup"><span data-stu-id="1e594-109">It should be present only if objects of this class are insertable in OLE 1 containers.</span></span>

<span data-ttu-id="1e594-110">**Serveur** spécifie le chemin d’accès complet à l’application serveur OLE 2 et le **verbe** spécifie les verbes.</span><span class="sxs-lookup"><span data-stu-id="1e594-110">**Server** specifies the full path to the OLE 2 server application and **Verb** specifies the verbs.</span></span> <span data-ttu-id="1e594-111">Le verbe 0 est le verbe principal et les verbes supplémentaires doivent être numérotés consécutivement.</span><span class="sxs-lookup"><span data-stu-id="1e594-111">Verb 0 is the primary verb and additional verbs must be numbered consecutively.</span></span>

 

 




