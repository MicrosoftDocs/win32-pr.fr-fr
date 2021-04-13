---
title: ProxyStubClsid32
description: Mappe un IID à un CLSID dans des dll de proxy 32 bits.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- Valeur de Registre ProxyStubClsid32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316554"
---
# <a name="proxystubclsid32"></a><span data-ttu-id="51a19-104">ProxyStubClsid32</span><span class="sxs-lookup"><span data-stu-id="51a19-104">ProxyStubClsid32</span></span>

<span data-ttu-id="51a19-105">Mappe un IID à un CLSID dans des dll de proxy 32 bits.</span><span class="sxs-lookup"><span data-stu-id="51a19-105">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="51a19-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="51a19-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a><span data-ttu-id="51a19-107">Notes</span><span class="sxs-lookup"><span data-stu-id="51a19-107">Remarks</span></span>

<span data-ttu-id="51a19-108">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le CLSID de l’IID.</span><span class="sxs-lookup"><span data-stu-id="51a19-108">This is a **REG\_SZ** value that specifies the CLSID for the IID.</span></span>

<span data-ttu-id="51a19-109">Il s’agit d’une entrée obligatoire, car le mappage IID-à-CLSID peut être différent pour les interfaces 16 bits et 32 bits.</span><span class="sxs-lookup"><span data-stu-id="51a19-109">This is a required entry since the IID-to-CLSID mapping may be different for 16-bit and 32-bit interfaces.</span></span> <span data-ttu-id="51a19-110">Le mappage IID-to-CLSID dépend de la façon dont les proxies d’interface sont empaquetés dans un ensemble de dll proxy.</span><span class="sxs-lookup"><span data-stu-id="51a19-110">The IID-to-CLSID mapping depends on the way the interface proxies are packaged into a set of proxy DLLs.</span></span>

<span data-ttu-id="51a19-111">Si vous ajoutez des interfaces, vous devez utiliser cette entrée pour les inscrire (systèmes 32 bits) afin qu’OLE puisse trouver le code de communication à distance approprié pour établir la communication entre processus.</span><span class="sxs-lookup"><span data-stu-id="51a19-111">If you add interfaces, you must use this entry to register them (32-bit systems) so that OLE can find the appropriate remoting code to establish interprocess communication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51a19-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51a19-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51a19-113">**IMarshal**</span><span class="sxs-lookup"><span data-stu-id="51a19-113">**IMarshal**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[<span data-ttu-id="51a19-114">**Interface**</span><span class="sxs-lookup"><span data-stu-id="51a19-114">**Interface**</span></span>](interface-key.md)
</dt> <dt>

[<span data-ttu-id="51a19-115">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="51a19-115">**ProxyStubClsid**</span></span>](proxystubclsid.md)
</dt> </dl>

 

 