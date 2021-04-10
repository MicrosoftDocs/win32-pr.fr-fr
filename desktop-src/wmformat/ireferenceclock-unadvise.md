---
title: IReferenceClock méthode Unadvise
description: La méthode Unadvise annule une demande de notification.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Méthode Unadvise Windows Media format
- Méthode Unadvise Windows Media format, interface IReferenceClock
- Interface IReferenceClock Windows Media format, Unadvise, méthode
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104101008"
---
# <a name="ireferenceclockunadvise-method"></a><span data-ttu-id="ca442-106">IReferenceClock :: Unadvise, méthode</span><span class="sxs-lookup"><span data-stu-id="ca442-106">IReferenceClock::Unadvise method</span></span>

<span data-ttu-id="ca442-107">La méthode **Unadvise** annule une demande de notification.</span><span class="sxs-lookup"><span data-stu-id="ca442-107">The **Unadvise** method cancels a notification request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca442-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca442-108">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="ca442-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca442-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca442-110">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="ca442-110">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="ca442-111">Identificateur de la demande à supprimer.</span><span class="sxs-lookup"><span data-stu-id="ca442-111">Identifier of the request to remove.</span></span> <span data-ttu-id="ca442-112">Utilisez la valeur retournée par AdviseTime dans le paramètre pdwAdviseCookie.</span><span class="sxs-lookup"><span data-stu-id="ca442-112">Use the value returned by AdviseTime in the pdwAdviseCookie parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca442-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca442-113">Return value</span></span>

<span data-ttu-id="ca442-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ca442-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ca442-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ca442-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ca442-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ca442-116">Return code</span></span>                                                                             | <span data-ttu-id="ca442-117">Description</span><span class="sxs-lookup"><span data-stu-id="ca442-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="ca442-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca442-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ca442-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca442-119">The method succeeded.</span></span><br/>                    |
| <dl> <span data-ttu-id="ca442-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ca442-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ca442-121">L’identificateur passé n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="ca442-121">The identifier passed in does not exist.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ca442-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca442-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca442-123">**Interface IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="ca442-123">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





