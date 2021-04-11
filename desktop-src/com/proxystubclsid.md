---
title: ProxyStubClsid
description: Mappe un IID à un CLSID dans des dll proxy 16 bits.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valeur de Registre ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029615"
---
# <a name="proxystubclsid"></a><span data-ttu-id="28a6e-104">ProxyStubClsid</span><span class="sxs-lookup"><span data-stu-id="28a6e-104">ProxyStubClsid</span></span>

<span data-ttu-id="28a6e-105">Mappe un IID à un CLSID dans des dll proxy 16 bits.</span><span class="sxs-lookup"><span data-stu-id="28a6e-105">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="28a6e-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="28a6e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="28a6e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="28a6e-107">Remarks</span></span>

<span data-ttu-id="28a6e-108">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le CLSID de l’IID.</span><span class="sxs-lookup"><span data-stu-id="28a6e-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="28a6e-109">Si vous ajoutez des interfaces, vous devez utiliser cette entrée pour les inscrire (systèmes 16 bits) afin qu’OLE puisse trouver le code de communication à distance approprié pour établir la communication entre processus.</span><span class="sxs-lookup"><span data-stu-id="28a6e-109">If you add interfaces, you must use this entry to register them (16-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28a6e-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28a6e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28a6e-111">**Interface**</span><span class="sxs-lookup"><span data-stu-id="28a6e-111">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="28a6e-112">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="28a6e-112">**ProxyStubClsid32**</span></span>](proxystubclsid32.md)
</dt> </dl>

 

 




