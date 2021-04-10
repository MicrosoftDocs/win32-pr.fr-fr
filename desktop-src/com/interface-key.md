---
title: Clé d'interface
description: Inscrit les nouvelles interfaces en associant un nom d’interface à un ID d’interface (IID). Il doit y avoir une sous-clé IID pour chaque nouvelle interface.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Clé de registre de l’interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029569"
---
# <a name="interface-key"></a><span data-ttu-id="fde18-105">Clé d'interface</span><span class="sxs-lookup"><span data-stu-id="fde18-105">Interface Key</span></span>

<span data-ttu-id="fde18-106">Inscrit les nouvelles interfaces en associant un nom d’interface à un ID d’interface (IID).</span><span class="sxs-lookup"><span data-stu-id="fde18-106">Registers new interfaces by associating an interface name with an interface ID (IID).</span></span> <span data-ttu-id="fde18-107">Il doit y avoir une sous-clé IID pour chaque nouvelle interface.</span><span class="sxs-lookup"><span data-stu-id="fde18-107">There must be one IID subkey for each new interface.</span></span>

## <a name="registry-key"></a><span data-ttu-id="fde18-108">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="fde18-108">Registry Key</span></span>

<span data-ttu-id="fde18-109">**HKEY \_ \_Interface des \\ \\ classes de \\ logiciels de l’ordinateur local** \\ *{* IID *}*</span><span class="sxs-lookup"><span data-stu-id="fde18-109">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Interface**\\ *{* IID *}*</span></span>



| <span data-ttu-id="fde18-110">Valeur de Registre</span><span class="sxs-lookup"><span data-stu-id="fde18-110">Registry value</span></span>                               | <span data-ttu-id="fde18-111">Description</span><span class="sxs-lookup"><span data-stu-id="fde18-111">Description</span></span>                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fde18-112">**BaseInterface**</span><span class="sxs-lookup"><span data-stu-id="fde18-112">**BaseInterface**</span></span>](baseinterface.md)       | <span data-ttu-id="fde18-113">Identifie l’interface à partir de laquelle l’interface actuelle est dérivée.</span><span class="sxs-lookup"><span data-stu-id="fde18-113">Identifies the interface from which the current interface is derived.</span></span>                                  |
| [<span data-ttu-id="fde18-114">**NumMethods**</span><span class="sxs-lookup"><span data-stu-id="fde18-114">**NumMethods**</span></span>](nummethods.md)             | <span data-ttu-id="fde18-115">Contient le nombre de méthodes dans l’interface associée, y compris les méthodes des interfaces dérivées.</span><span class="sxs-lookup"><span data-stu-id="fde18-115">Contains the number of methods in the associated interface, including methods from derived interfaces.</span></span> |
| [<span data-ttu-id="fde18-116">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="fde18-116">**ProxyStubClsid**</span></span>](proxystubclsid.md)     | <span data-ttu-id="fde18-117">Mappe un IID à un CLSID dans des dll proxy 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fde18-117">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>                                                           |
| [<span data-ttu-id="fde18-118">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="fde18-118">**ProxyStubClsid32**</span></span>](proxystubclsid32.md) | <span data-ttu-id="fde18-119">Mappe un IID à un CLSID dans des dll de proxy 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fde18-119">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="fde18-120">Notes</span><span class="sxs-lookup"><span data-stu-id="fde18-120">Remarks</span></span>

<span data-ttu-id="fde18-121">La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.</span><span class="sxs-lookup"><span data-stu-id="fde18-121">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fde18-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fde18-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fde18-123">**Interface**</span><span class="sxs-lookup"><span data-stu-id="fde18-123">**Interface**</span></span>](interface.md)
</dt> </dl>

 

 




