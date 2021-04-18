---
description: La méthode SetAlias configure un alias H. 323 par défaut pour l’adresse. Cet alias sera utilisé dans le programme d’installation d’un appel H. 323 afin que l’autre partie sache le nom de ce tiers.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'IH323LineEx :: SetAlias, méthode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532979"
---
# <a name="ih323lineexsetalias-method"></a><span data-ttu-id="2b801-104">IH323LineEx :: SetAlias, méthode</span><span class="sxs-lookup"><span data-stu-id="2b801-104">IH323LineEx::SetAlias method</span></span>

<span data-ttu-id="2b801-105">\[**SetAlias** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2b801-105">\[**SetAlias** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2b801-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="2b801-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2b801-107">La méthode **SetAlias** configure un alias H. 323 par défaut pour l’adresse.</span><span class="sxs-lookup"><span data-stu-id="2b801-107">The **SetAlias** method configures a default H.323 alias for the address.</span></span> <span data-ttu-id="2b801-108">Cet alias sera utilisé dans le programme d’installation d’un appel H. 323 afin que l’autre partie sache le nom de ce tiers.</span><span class="sxs-lookup"><span data-stu-id="2b801-108">This alias will be used in the H.323 call setup exchange so that the other party knows the name of this party.</span></span>

<span data-ttu-id="2b801-109">L’appel de cette méthode une deuxième fois remplace l’alias précédent.</span><span class="sxs-lookup"><span data-stu-id="2b801-109">Calling this method a second time will overwrite the previous alias.</span></span>

<span data-ttu-id="2b801-110">L’alias défini sur cette interface est utilisé uniquement lorsqu’il n’existe aucun autre moyen pour le TSP de trouver un alias approprié.</span><span class="sxs-lookup"><span data-stu-id="2b801-110">The alias set on this interface will be used only when there is no other way for the TSP to find a proper alias.</span></span> <span data-ttu-id="2b801-111">À l’avenir, lorsque la prise en charge de Gatekeeper sera ajoutée au TSP, l’alias inscrit auprès de l’opérateur de l’opérateur ou attribué par l’opérateur de l’opérateur remplacera ce qui est défini par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2b801-111">In the future, when gatekeeper support is added into the TSP, the alias registered to the gatekeeper or assigned by the gatekeeper will override whatever is set through this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b801-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b801-112">Syntax</span></span>


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="2b801-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b801-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b801-114">*strAlias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b801-114">*strAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b801-115">Alias à utiliser, en Unicode.</span><span class="sxs-lookup"><span data-stu-id="2b801-115">The alias to be used, in Unicode.</span></span> <span data-ttu-id="2b801-116">La terminaison **null** n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2b801-116">**Null** termination is not required.</span></span>

</dd> <dt>

<span data-ttu-id="2b801-117">*dwLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b801-117">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b801-118">Longueur du nom d’alias en nombre de caractères, y compris la marque de fin **null** .</span><span class="sxs-lookup"><span data-stu-id="2b801-118">The length of the alias name in number of characters, including the **null** terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b801-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b801-119">Return value</span></span>

<span data-ttu-id="2b801-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2b801-120">This method can return one of these values.</span></span>



| <span data-ttu-id="2b801-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2b801-121">Return code</span></span>                                                                               | <span data-ttu-id="2b801-122">Description</span><span class="sxs-lookup"><span data-stu-id="2b801-122">Description</span></span>                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b801-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2b801-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="2b801-124">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="2b801-124">Method succeeded.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="2b801-125"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="2b801-125"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="2b801-126">Le nombre de caractères indiqué dans *dwLength* dépasse le nombre réel de caractères dans le paramètre *strAlias* .</span><span class="sxs-lookup"><span data-stu-id="2b801-126">The number of characters indicated in *dwLength* exceeds the actual number of characters in the *strAlias* parameter.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b801-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b801-127">Requirements</span></span>



| <span data-ttu-id="2b801-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b801-128">Requirement</span></span> | <span data-ttu-id="2b801-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b801-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b801-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2b801-130">TAPI version</span></span><br/> | <span data-ttu-id="2b801-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2b801-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2b801-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b801-132">Header</span></span><br/>       | <dl> <span data-ttu-id="2b801-133"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b801-133"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="2b801-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2b801-134">Library</span></span><br/>      | <dl> <span data-ttu-id="2b801-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b801-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2b801-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2b801-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="2b801-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b801-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




