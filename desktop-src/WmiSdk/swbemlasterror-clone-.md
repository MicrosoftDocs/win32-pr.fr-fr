---
description: La méthode Clone \_ de l’objet SWbemLastError retourne un nouvel objet qui est un clone de l’objet SWbemLastError actuel.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: Méthode SWbemLastError.Clone_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7d4d43f73ab42021235db39adba0a77bc783b97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535451"
---
# <a name="swbemlasterrorclone_-method"></a><span data-ttu-id="4f0a9-103">SWbemLastError. Clone, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="4f0a9-103">SWbemLastError.Clone\_ method</span></span>

<span data-ttu-id="4f0a9-104">La **méthode \_ clone** de l’objet [**SWbemLastError**](swbemlasterror.md) retourne un nouvel objet qui est un clone de l’objet **SWbemLastError** actuel.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-104">The **Clone\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a new object that is a clone of the current **SWbemLastError** object.</span></span>

<span data-ttu-id="4f0a9-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4f0a9-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0a9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f0a9-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="4f0a9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f0a9-107">Parameters</span></span>

<span data-ttu-id="4f0a9-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f0a9-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f0a9-109">Return value</span></span>

<span data-ttu-id="4f0a9-110">Si la **méthode \_ clone** réussit, elle retourne un nouvel objet [**SWbemLastError**](swbemlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4f0a9-110">If the **Clone\_** method is successful, it returns a new [**SWbemLastError**](swbemlasterror.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f0a9-111">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4f0a9-111">Error codes</span></span>

<span data-ttu-id="4f0a9-112">À la fin de la **méthode \_ clone** , l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-112">Upon the completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="4f0a9-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4f0a9-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4f0a9-114">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4f0a9-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="4f0a9-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4f0a9-116">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-116">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4f0a9-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="4f0a9-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="4f0a9-118">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-118">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f0a9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4f0a9-119">Remarks</span></span>

<span data-ttu-id="4f0a9-120">Utilisez la **méthode \_ clone** pour dupliquer une définition ou une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-120">Use the **Clone\_** method to duplicate a class definition or instance.</span></span> <span data-ttu-id="4f0a9-121">Cette méthode est utile lorsque vous devez sauvegarder la copie d’origine de l’objet lors de la modification d’une nouvelle copie.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-121">This method is useful when you need to back up the original copy of the object while you modify a new copy.</span></span> <span data-ttu-id="4f0a9-122">Utilisez également cette méthode pour créer de nombreuses nouvelles instances à partir d’une seule instance source.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-122">Also, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="4f0a9-123">Par exemple, utilisez [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) pour créer une instance de démarrage unique et utilisez **SWbemLastError. \_ clone** pour produire rapidement 100 copies de l’instance.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance and use **SWbemLastError.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="4f0a9-124">Par la suite, vous pouvez modifier les objets, en attribuant des valeurs spécifiques à chaque objet.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-124">Subsequently, you can modify the objects, giving specific values to each object.</span></span>

<span data-ttu-id="4f0a9-125">Il n’est pas possible d’utiliser cette méthode pour convertir une définition de classe en instance ou pour convertir une instance en une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-125">It is not possible to use this method to convert a class definition to an instance or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f0a9-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f0a9-126">Requirements</span></span>



| <span data-ttu-id="4f0a9-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f0a9-127">Requirement</span></span> | <span data-ttu-id="4f0a9-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0a9-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0a9-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f0a9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4f0a9-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f0a9-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f0a9-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f0a9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4f0a9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f0a9-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f0a9-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f0a9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f0a9-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f0a9-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f0a9-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4f0a9-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f0a9-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4f0a9-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4f0a9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4f0a9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f0a9-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f0a9-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f0a9-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="4f0a9-139">CLSID</span></span><br/>                    | <span data-ttu-id="4f0a9-140">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="4f0a9-140">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="4f0a9-141">IID</span><span class="sxs-lookup"><span data-stu-id="4f0a9-141">IID</span></span><br/>                      | <span data-ttu-id="4f0a9-142">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="4f0a9-142">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




