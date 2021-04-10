---
description: Utilisez la \_ méthode SpawnInstance de l’objet SWbemObject pour créer une nouvelle instance d’une classe.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Méthode SWbemObject.SpawnInstance_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210548"
---
# <a name="swbemobjectspawninstance_-method"></a><span data-ttu-id="2f625-103">SWbemObject. SpawnInstance, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="2f625-103">SWbemObject.SpawnInstance\_ method</span></span>

<span data-ttu-id="2f625-104">Utilisez la **méthode \_ SpawnInstance** de l’objet [**SWbemObject**](swbemobject.md) pour créer une nouvelle instance d’une classe.</span><span class="sxs-lookup"><span data-stu-id="2f625-104">Use the **SpawnInstance\_** method of the [**SWbemObject**](swbemobject.md) object to create a new instance of a class.</span></span> <span data-ttu-id="2f625-105">L’objet actuel doit être une définition de classe obtenue à partir de WMI via une méthode telle que [**SWbemServices. obtenir**](swbemservices-get.md) ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="2f625-105">The current object must be a class definition obtained from WMI via a method such as [**SWbemServices.Get**](swbemservices-get.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="2f625-106">Utilisez ensuite cette définition de classe pour créer des instances.</span><span class="sxs-lookup"><span data-stu-id="2f625-106">Then, use this class definition to create new instances.</span></span> <span data-ttu-id="2f625-107">Créez chaque nouvelle instance localement au sein du processus, puis appelez [**SWbemObject. put \_**](swbemobject-put-.md) pour réellement créer l’instance dans WMI.</span><span class="sxs-lookup"><span data-stu-id="2f625-107">Create each new instance locally within the process, and then call [**SWbemObject.Put\_**](swbemobject-put-.md) to actually create the instance within WMI.</span></span>

> [!Note]  
> <span data-ttu-id="2f625-108">La génération d’une instance à partir d’une instance est prise en charge, mais l’instance retournée est vide.</span><span class="sxs-lookup"><span data-stu-id="2f625-108">Spawning an instance from an instance is supported, but the returned instance is empty.</span></span>

 

<span data-ttu-id="2f625-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2f625-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f625-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f625-110">Syntax</span></span>


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2f625-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f625-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f625-112">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2f625-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f625-113">Réservé et doit être égal à zéro s’il est spécifié.</span><span class="sxs-lookup"><span data-stu-id="2f625-113">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f625-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f625-114">Return value</span></span>

<span data-ttu-id="2f625-115">En cas de réussite, cet appel retourne un objet [**SWbemObject**](swbemobject.md) qui contient une nouvelle instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="2f625-115">If successful, this call returns an [**SWbemObject**](swbemobject.md) object that contains a new instance of the class.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f625-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2f625-116">Error codes</span></span>

<span data-ttu-id="2f625-117">À la fin de la **méthode \_ SpawnInstance** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="2f625-117">After the completion of the **SpawnInstance\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2f625-118">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="2f625-118">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="2f625-119">L’objet actuel n’est pas une définition de classe valide et ne peut pas générer de nouvelles instances.</span><span class="sxs-lookup"><span data-stu-id="2f625-119">Current object is not a valid class definition, and it cannot spawn new instances.</span></span> <span data-ttu-id="2f625-120">Soit il est incomplet, soit il n’a pas été inscrit auprès de WMI à l’aide de [**SWbemObject. put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="2f625-120">Either it is incomplete, or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f625-121">**wbemErrIllegalOperation** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="2f625-121">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="2f625-122">Retourné si cette méthode est utilisée sur une instance au lieu d’une classe.</span><span class="sxs-lookup"><span data-stu-id="2f625-122">Returned if this method is used on an instance instead of a class.</span></span>

</dd> <dt>

<span data-ttu-id="2f625-123">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="2f625-123">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2f625-124">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="2f625-124">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="2f625-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="2f625-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2f625-126">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="2f625-126">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f625-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f625-127">Requirements</span></span>



| <span data-ttu-id="2f625-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f625-128">Requirement</span></span> | <span data-ttu-id="2f625-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f625-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f625-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f625-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2f625-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f625-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f625-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f625-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2f625-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f625-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f625-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f625-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f625-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f625-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f625-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2f625-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f625-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f625-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f625-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2f625-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f625-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f625-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2f625-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="2f625-140">CLSID</span></span><br/>                    | <span data-ttu-id="2f625-141">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="2f625-141">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="2f625-142">IID</span><span class="sxs-lookup"><span data-stu-id="2f625-142">IID</span></span><br/>                      | <span data-ttu-id="2f625-143">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="2f625-143">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="2f625-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f625-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f625-145">**M**</span><span class="sxs-lookup"><span data-stu-id="2f625-145">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="2f625-146">**SWbemObject. put\_**</span><span class="sxs-lookup"><span data-stu-id="2f625-146">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)
</dt> <dt>

[<span data-ttu-id="2f625-147">**SWbemServices.**</span><span class="sxs-lookup"><span data-stu-id="2f625-147">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

 




