---
description: Annule l’opération de transfert en cours.
ms.assetid: 42c6b2c3-7b6a-45d2-a7ce-844e95fe277b
title: 'IWiaTransfer :: Cancel, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Cancel
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 4764e922498a3c33278555cae37d09c1822959dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526458"
---
# <a name="iwiatransfercancel-method"></a><span data-ttu-id="44688-103">IWiaTransfer :: Cancel, méthode</span><span class="sxs-lookup"><span data-stu-id="44688-103">IWiaTransfer::Cancel method</span></span>

<span data-ttu-id="44688-104">Annule l’opération de transfert en cours.</span><span class="sxs-lookup"><span data-stu-id="44688-104">Cancels the current transfer operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="44688-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44688-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="44688-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44688-106">Parameters</span></span>

<span data-ttu-id="44688-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="44688-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44688-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44688-108">Return value</span></span>

<span data-ttu-id="44688-109">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="44688-109">Type: **HRESULT**</span></span>

<span data-ttu-id="44688-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="44688-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44688-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44688-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44688-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44688-112">Requirements</span></span>



| <span data-ttu-id="44688-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44688-113">Requirement</span></span> | <span data-ttu-id="44688-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="44688-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44688-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44688-115">Minimum supported client</span></span><br/> | <span data-ttu-id="44688-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44688-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="44688-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44688-117">Minimum supported server</span></span><br/> | <span data-ttu-id="44688-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44688-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="44688-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="44688-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="44688-120"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="44688-120"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="44688-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="44688-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44688-122"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44688-122"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="44688-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="44688-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="44688-124"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44688-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




