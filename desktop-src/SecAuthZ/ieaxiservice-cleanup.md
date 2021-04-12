---
description: Libère les ressources utilisées par l’interface IeAxiService.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'IeAxiService :: Cleanup, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204002"
---
# <a name="ieaxiservicecleanup-method"></a><span data-ttu-id="aba52-103">IeAxiService :: Cleanup, méthode</span><span class="sxs-lookup"><span data-stu-id="aba52-103">IeAxiService::Cleanup method</span></span>

<span data-ttu-id="aba52-104">La méthode **Cleanup** libère les ressources utilisées par l’interface [**IeAxiService**](ieaxiservice.md) .</span><span class="sxs-lookup"><span data-stu-id="aba52-104">The **Cleanup** method frees resources used by the [**IeAxiService**](ieaxiservice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba52-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aba52-105">Syntax</span></span>


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a><span data-ttu-id="aba52-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aba52-106">Parameters</span></span>

<span data-ttu-id="aba52-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="aba52-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aba52-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aba52-108">Return value</span></span>

<span data-ttu-id="aba52-109">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aba52-109">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="aba52-110">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="aba52-110">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="aba52-111">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="aba52-111">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="aba52-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aba52-112">Requirements</span></span>



| <span data-ttu-id="aba52-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aba52-113">Requirement</span></span> | <span data-ttu-id="aba52-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="aba52-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba52-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aba52-115">Minimum supported client</span></span><br/> | <span data-ttu-id="aba52-116">Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aba52-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="aba52-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aba52-117">Minimum supported server</span></span><br/> | <span data-ttu-id="aba52-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="aba52-118">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="aba52-119">IID</span><span class="sxs-lookup"><span data-stu-id="aba52-119">IID</span></span><br/>                      | <span data-ttu-id="aba52-120">IID \_ IeAxiService est défini en tant que E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="aba52-120">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="aba52-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aba52-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba52-122">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="aba52-122">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

