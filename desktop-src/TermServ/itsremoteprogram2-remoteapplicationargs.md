---
title: ITSRemoteProgram2 propriété RemoteApplicationArgs
description: Arguments de ligne de commande pour le RemoteApp.
ms.assetid: c1c36876-df3d-4ef9-a5ac-f623bc51fe7b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RemoteApplicationArgs
- Services Bureau à distance de la propriété RemoteApplicationArgs, interface ITSRemoteProgram2
- Services Bureau à distance de l’interface ITSRemoteProgram2, propriété RemoteApplicationArgs
- Services Bureau à distance de la propriété RemoteApplicationArgs, interface ITSRemoteProgram3
- Services Bureau à distance de l’interface ITSRemoteProgram3, propriété RemoteApplicationArgs
topic_type:
- apiref
api_name:
- ITSRemoteProgram2.RemoteApplicationArgs
- ITSRemoteProgram2.put_RemoteApplicationArgs
- ITSRemoteProgram3.RemoteApplicationArgs
- ITSRemoteProgram3.put_RemoteApplicationArgs
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b77cc7259520156321140c8f85713095f02e2b78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105862"
---
# <a name="itsremoteprogram2remoteapplicationargs-property"></a><span data-ttu-id="945d6-108">ITSRemoteProgram2 :: RemoteApplicationArgs, propriété</span><span class="sxs-lookup"><span data-stu-id="945d6-108">ITSRemoteProgram2::RemoteApplicationArgs property</span></span>

<span data-ttu-id="945d6-109">Arguments de ligne de commande pour le RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="945d6-109">The command-line arguments for the RemoteApp.</span></span>

<span data-ttu-id="945d6-110">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="945d6-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="945d6-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="945d6-111">Syntax</span></span>


```C++
HRESULT put_RemoteApplicationArgs(
  [in] BSTR bstrRemoteApplicationArgs
);
```



## <a name="property-value"></a><span data-ttu-id="945d6-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="945d6-112">Property value</span></span>

<span data-ttu-id="945d6-113">Arguments de ligne de commande RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="945d6-113">The RemoteApp command-line arguments.</span></span>

## <a name="requirements"></a><span data-ttu-id="945d6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="945d6-114">Requirements</span></span>



| <span data-ttu-id="945d6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="945d6-115">Requirement</span></span> | <span data-ttu-id="945d6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="945d6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="945d6-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="945d6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="945d6-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="945d6-118">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="945d6-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="945d6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="945d6-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="945d6-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="945d6-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="945d6-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="945d6-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="945d6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="945d6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="945d6-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="945d6-124"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="945d6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="945d6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945d6-126">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="945d6-126">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="945d6-127">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="945d6-127">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> </dl>

 

 





