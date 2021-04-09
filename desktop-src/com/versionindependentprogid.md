---
title: VersionIndependentProgID
description: Associe un ProgID à un CLSID. Cette valeur est utilisée pour déterminer la version la plus récente d’une application d’objet.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- Clé de Registre VersionIndependentProgID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029857"
---
# <a name="versionindependentprogid"></a><span data-ttu-id="3d39e-105">VersionIndependentProgID</span><span class="sxs-lookup"><span data-stu-id="3d39e-105">VersionIndependentProgID</span></span>

<span data-ttu-id="3d39e-106">Associe un ProgID à un CLSID.</span><span class="sxs-lookup"><span data-stu-id="3d39e-106">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="3d39e-107">Cette valeur est utilisée pour déterminer la version la plus récente d’une application d’objet.</span><span class="sxs-lookup"><span data-stu-id="3d39e-107">This value is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3d39e-108">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="3d39e-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a><span data-ttu-id="3d39e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3d39e-109">Remarks</span></span>

<span data-ttu-id="3d39e-110">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie la version la plus récente de l’application de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3d39e-110">This is a **REG\_SZ** value that specifies the latest version of the object application.</span></span>

<span data-ttu-id="3d39e-111">Le ProgID indépendant de la version est stocké et géré uniquement par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="3d39e-111">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="3d39e-112">Lorsqu’il reçoit le ProgID indépendant de la version, la fonction [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retourne le CLSID de la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="3d39e-112">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="3d39e-113">Vous pouvez utiliser [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) et [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) pour effectuer une conversion entre ces deux représentations.</span><span class="sxs-lookup"><span data-stu-id="3d39e-113">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

 

 




