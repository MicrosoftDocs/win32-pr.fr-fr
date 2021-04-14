---
description: Obtient le résultat d’une action asynchrone.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'IAsyncAction :: GetResults, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201445"
---
# <a name="iasyncactiongetresults-method"></a><span data-ttu-id="09172-103">IAsyncAction :: GetResults, méthode</span><span class="sxs-lookup"><span data-stu-id="09172-103">IAsyncAction::GetResults method</span></span>

<span data-ttu-id="09172-104">Obtient le résultat d’une action asynchrone.</span><span class="sxs-lookup"><span data-stu-id="09172-104">Gets the outcome of an asynchronous action.</span></span>

## <a name="syntax"></a><span data-ttu-id="09172-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09172-105">Syntax</span></span>


```C++
HRESULT GetResults();
```



## <a name="parameters"></a><span data-ttu-id="09172-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09172-106">Parameters</span></span>

<span data-ttu-id="09172-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="09172-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09172-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09172-108">Return value</span></span>

<span data-ttu-id="09172-109">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="09172-109">Type: **HRESULT**</span></span>

<span data-ttu-id="09172-110">Cette méthode retourne toujours **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="09172-110">This method always returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="09172-111">Notes</span><span class="sxs-lookup"><span data-stu-id="09172-111">Remarks</span></span>

<span data-ttu-id="09172-112">L’appel de la méthode **GetResults** n’a aucun effet si l’implémentation actuelle a un type dynamique [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span><span class="sxs-lookup"><span data-stu-id="09172-112">Calling the **GetResults** method has no effect if the current implementation has a dynamic type of [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span></span>

## <a name="requirements"></a><span data-ttu-id="09172-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09172-113">Requirements</span></span>



| <span data-ttu-id="09172-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09172-114">Requirement</span></span> | <span data-ttu-id="09172-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="09172-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09172-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09172-116">Minimum supported client</span></span><br/> | <span data-ttu-id="09172-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="09172-117">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="09172-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09172-118">Minimum supported server</span></span><br/> | <span data-ttu-id="09172-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09172-119">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="09172-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="09172-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="09172-121"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="09172-121"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09172-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09172-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09172-123">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="09172-123">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
