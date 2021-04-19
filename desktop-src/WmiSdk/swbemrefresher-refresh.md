---
description: La méthode SWbemRefresher. Refresh met à jour tous les éléments contenus dans l’objet SWbemRefresher. Objet SWbemRefresher.
ms.assetid: 85a4777a-4be7-44f2-b7a6-e18b5e57f7af
ms.tgt_platform: multiple
title: SWbemRefresher. Refresh, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Refresh
- ISWbemRefresher.Refresh
- ISWbemRefresher.Refresh
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8b2522227041858770c7256d7d2520cc661948e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535104"
---
# <a name="swbemrefresherrefresh-method"></a><span data-ttu-id="63142-103">SWbemRefresher. Refresh, méthode</span><span class="sxs-lookup"><span data-stu-id="63142-103">SWbemRefresher.Refresh method</span></span>

<span data-ttu-id="63142-104">La méthode **SWbemRefresher. Refresh** met à jour tous les éléments contenus dans l’objet [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="63142-104">The **SWbemRefresher.Refresh** method updates all the items that are contained in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="63142-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="63142-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="63142-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63142-106">Syntax</span></span>


```VB
SWbemRefresher.Refresh( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="63142-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63142-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63142-108">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="63142-108">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63142-109">Les indicateurs doivent avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="63142-109">Flags must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63142-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63142-110">Return value</span></span>

<span data-ttu-id="63142-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="63142-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="63142-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63142-112">Requirements</span></span>



| <span data-ttu-id="63142-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63142-113">Requirement</span></span> | <span data-ttu-id="63142-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="63142-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63142-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63142-115">Minimum supported client</span></span><br/> | <span data-ttu-id="63142-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63142-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63142-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63142-117">Minimum supported server</span></span><br/> | <span data-ttu-id="63142-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63142-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63142-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="63142-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="63142-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="63142-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="63142-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="63142-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="63142-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="63142-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="63142-123">DLL</span><span class="sxs-lookup"><span data-stu-id="63142-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63142-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63142-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="63142-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="63142-125">CLSID</span></span><br/>                    | <span data-ttu-id="63142-126">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="63142-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="63142-127">IID</span><span class="sxs-lookup"><span data-stu-id="63142-127">IID</span></span><br/>                      | <span data-ttu-id="63142-128">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="63142-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="63142-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63142-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63142-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="63142-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




