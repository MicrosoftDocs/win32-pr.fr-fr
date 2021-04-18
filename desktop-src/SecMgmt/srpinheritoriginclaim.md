---
description: Cette fonction prend l’attribut Origin s’il est présent à partir du jeton d’origine et les définit sur un doublon du jeton qui hérite et retourne le jeton dupliqué.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpInheritOriginClaim fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529112"
---
# <a name="srpinheritoriginclaim-function"></a><span data-ttu-id="141c5-103">srpInheritOriginClaim fonction)</span><span class="sxs-lookup"><span data-stu-id="141c5-103">srpInheritOriginClaim function</span></span>

<span data-ttu-id="141c5-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="141c5-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="141c5-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="141c5-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="141c5-106">Cette fonction prend l’attribut Origin s’il est présent à partir du jeton d’origine et les définit sur un doublon du jeton qui hérite et retourne le jeton dupliqué.</span><span class="sxs-lookup"><span data-stu-id="141c5-106">This function takes the origin attribute if present from the origin token and sets them on a duplicate of the inheriting token, and returns the duplicate token.</span></span> <span data-ttu-id="141c5-107">L’appelant peut alors emprunter l’identité du jeton retourné.</span><span class="sxs-lookup"><span data-stu-id="141c5-107">The caller can then impersonate the returned token.</span></span> <span data-ttu-id="141c5-108">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="141c5-108">This function has no associated import library.</span></span> <span data-ttu-id="141c5-109">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à srpapi.dll.</span><span class="sxs-lookup"><span data-stu-id="141c5-109">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to srpapi.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="141c5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="141c5-110">Syntax</span></span>


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a><span data-ttu-id="141c5-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="141c5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="141c5-112">*OriginToken* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="141c5-112">*OriginToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="141c5-113">Handle vers le jeton qui est dupliqué et reçoit l’attribut Origin hérité.</span><span class="sxs-lookup"><span data-stu-id="141c5-113">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="141c5-114">Ce descripteur doit être ouvert avec le \_ droit d’accès en double du jeton.</span><span class="sxs-lookup"><span data-stu-id="141c5-114">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span>

</dd> <dt>

<span data-ttu-id="141c5-115">*InheritingToken* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="141c5-115">*InheritingToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="141c5-116">Handle vers le jeton qui est dupliqué et reçoit l’attribut Origin hérité.</span><span class="sxs-lookup"><span data-stu-id="141c5-116">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="141c5-117">Ce descripteur doit être ouvert avec le \_ droit d’accès en double du jeton.</span><span class="sxs-lookup"><span data-stu-id="141c5-117">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span> 

</dd> <dt>

<span data-ttu-id="141c5-118">*ResultToken*</span><span class="sxs-lookup"><span data-stu-id="141c5-118">*ResultToken*</span></span> 
</dt> <dd>

<span data-ttu-id="141c5-119">En cas de réussite, reçoit le jeton dupliqué.</span><span class="sxs-lookup"><span data-stu-id="141c5-119">On success, receives the duplicated token.</span></span> <span data-ttu-id="141c5-120">L’appelant peut l’emprunter pour effectuer des opérations avec l’attribut Origin hérité.</span><span class="sxs-lookup"><span data-stu-id="141c5-120">The caller can impersonate it to perform operations with the inherited origin attribute.</span></span> <span data-ttu-id="141c5-121">L’appelant prend la propriété de ce handle et doit le fermer.</span><span class="sxs-lookup"><span data-stu-id="141c5-121">The caller takes ownership of this handle and must close it.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="141c5-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="141c5-122">Return value</span></span>

<span data-ttu-id="141c5-123">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="141c5-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="141c5-124">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="141c5-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="141c5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="141c5-125">Requirements</span></span>



| <span data-ttu-id="141c5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="141c5-126">Requirement</span></span> | <span data-ttu-id="141c5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="141c5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="141c5-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="141c5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="141c5-129">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="141c5-129">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="141c5-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="141c5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="141c5-131">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="141c5-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="141c5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="141c5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="141c5-133"><dt>Srpapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="141c5-133"><dt>Srpapi.dll</dt></span></span> </dl> |



 

