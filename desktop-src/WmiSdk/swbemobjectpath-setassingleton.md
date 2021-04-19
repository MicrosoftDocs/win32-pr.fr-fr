---
description: La méthode SetAsSingleton de l’objet SWbemObjectPath force le chemin d’accès à l’adresse d’une instance WMI Singleton d’une classe. Une classe singleton est une classe qui ne peut jamais avoir plus d’une instance.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Méthode SWbemObjectPath. SetAsSingleton (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5335f595eccc996ece9f941092ffffae487352fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529449"
---
# <a name="swbemobjectpathsetassingleton-method"></a><span data-ttu-id="13a72-104">Méthode SWbemObjectPath. SetAsSingleton</span><span class="sxs-lookup"><span data-stu-id="13a72-104">SWbemObjectPath.SetAsSingleton method</span></span>

<span data-ttu-id="13a72-105">La méthode **SetAsSingleton** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) force le chemin d’accès à l’adresse d’une instance WMI Singleton d’une classe.</span><span class="sxs-lookup"><span data-stu-id="13a72-105">The **SetAsSingleton** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a singleton WMI instance of a class.</span></span> <span data-ttu-id="13a72-106">Une classe singleton est une classe qui ne peut jamais avoir plus d’une instance.</span><span class="sxs-lookup"><span data-stu-id="13a72-106">A singleton class is a class that can never have more than one instance.</span></span>

<span data-ttu-id="13a72-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="13a72-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span> <span data-ttu-id="13a72-108">SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="13a72-108">SWbemObjectPath</span></span>

## <a name="syntax"></a><span data-ttu-id="13a72-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13a72-109">Syntax</span></span>


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a><span data-ttu-id="13a72-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13a72-110">Parameters</span></span>

<span data-ttu-id="13a72-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="13a72-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13a72-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13a72-112">Return value</span></span>

<span data-ttu-id="13a72-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="13a72-113">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13a72-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="13a72-114">Error codes</span></span>

<span data-ttu-id="13a72-115">À la fin de la méthode **SetAsSingleton** , l’objet **Err** peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="13a72-115">Upon completion of the **SetAsSingleton** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="13a72-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="13a72-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="13a72-117">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="13a72-117">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13a72-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13a72-118">Requirements</span></span>



| <span data-ttu-id="13a72-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13a72-119">Requirement</span></span> | <span data-ttu-id="13a72-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="13a72-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13a72-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13a72-121">Minimum supported client</span></span><br/> | <span data-ttu-id="13a72-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13a72-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13a72-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13a72-123">Minimum supported server</span></span><br/> | <span data-ttu-id="13a72-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13a72-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13a72-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="13a72-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a72-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="13a72-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="13a72-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="13a72-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="13a72-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="13a72-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="13a72-129">DLL</span><span class="sxs-lookup"><span data-stu-id="13a72-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13a72-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13a72-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="13a72-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="13a72-131">CLSID</span></span><br/>                    | <span data-ttu-id="13a72-132">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="13a72-132">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="13a72-133">IID</span><span class="sxs-lookup"><span data-stu-id="13a72-133">IID</span></span><br/>                      | <span data-ttu-id="13a72-134">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="13a72-134">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




