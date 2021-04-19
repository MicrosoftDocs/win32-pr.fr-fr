---
description: La méthode SetAsClass de l’objet SWbemObjectPath force le chemin d’accès à une classe WMI.
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: SWbemObjectPath. SetAsClass, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsClass
- ISWbemObjectPath.SetAsClass
- ISWbemObjectPath.put_SetAsClass
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 371fe95c3a7152767c45849191658c4bcb661750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518392"
---
# <a name="swbemobjectpathsetasclass-property"></a><span data-ttu-id="c4f95-103">SWbemObjectPath. SetAsClass, propriété</span><span class="sxs-lookup"><span data-stu-id="c4f95-103">SWbemObjectPath.SetAsClass property</span></span>

<span data-ttu-id="c4f95-104">La méthode **SetAsClass** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) force le chemin d’accès à une classe WMI.</span><span class="sxs-lookup"><span data-stu-id="c4f95-104">The **SetAsClass** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a WMI class.</span></span>

<span data-ttu-id="c4f95-105">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="c4f95-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f95-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4f95-106">Syntax</span></span>


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a><span data-ttu-id="c4f95-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c4f95-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="c4f95-108">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c4f95-108">Error codes</span></span>

<span data-ttu-id="c4f95-109">Une fois que vous avez obtenu ou défini la propriété **SetAsClass** , l’objet **Err** peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c4f95-109">After you get or set the **SetAsClass** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="c4f95-110">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c4f95-110">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c4f95-111">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c4f95-111">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4f95-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4f95-112">Requirements</span></span>



| <span data-ttu-id="c4f95-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4f95-113">Requirement</span></span> | <span data-ttu-id="c4f95-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4f95-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f95-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4f95-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f95-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4f95-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4f95-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4f95-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f95-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4f95-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4f95-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4f95-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4f95-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4f95-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4f95-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c4f95-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4f95-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c4f95-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c4f95-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c4f95-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4f95-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4f95-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4f95-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="c4f95-125">CLSID</span></span><br/>                    | <span data-ttu-id="c4f95-126">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="c4f95-126">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="c4f95-127">IID</span><span class="sxs-lookup"><span data-stu-id="c4f95-127">IID</span></span><br/>                      | <span data-ttu-id="c4f95-128">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="c4f95-128">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




