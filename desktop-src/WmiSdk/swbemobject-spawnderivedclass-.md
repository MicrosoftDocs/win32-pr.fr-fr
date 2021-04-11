---
description: Utilisez la \_ méthode SpawnDerivedClass de l’objet SWbemObject pour créer un objet de classe dérivée à partir de l’objet actuel. L’objet doit être une définition de classe qui devient la classe parente de l’objet généré.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: Méthode SWbemObject.SpawnDerivedClass_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202158"
---
# <a name="swbemobjectspawnderivedclass_-method"></a><span data-ttu-id="9103c-104">SWbemObject. SpawnDerivedClass, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="9103c-104">SWbemObject.SpawnDerivedClass\_ method</span></span>

<span data-ttu-id="9103c-105">Utilisez la **méthode \_ SpawnDerivedClass** de l’objet [**SWbemObject**](swbemobject.md) pour créer un objet de classe dérivée à partir de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="9103c-105">Use the **SpawnDerivedClass\_** method of the [**SWbemObject**](swbemobject.md) object to create a derived class object from the current object.</span></span> <span data-ttu-id="9103c-106">L’objet doit être une définition de classe qui devient la classe parente de l’objet généré.</span><span class="sxs-lookup"><span data-stu-id="9103c-106">The object must be a class definition that becomes the parent class of the spawned object.</span></span>

<span data-ttu-id="9103c-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9103c-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9103c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9103c-108">Syntax</span></span>


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9103c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9103c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9103c-110">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9103c-110">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9103c-111">Réservé et doit avoir la valeur 0 (zéro) si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9103c-111">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9103c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9103c-112">Return value</span></span>

<span data-ttu-id="9103c-113">Si l’appel réussit, l’objet [**SWbemObject**](swbemobject.md) contient le nouvel objet de définition de classe.</span><span class="sxs-lookup"><span data-stu-id="9103c-113">If the call is successful, the [**SWbemObject**](swbemobject.md) object contains the new class definition object.</span></span> <span data-ttu-id="9103c-114">Aucun objet n’est retourné en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9103c-114">No object returns when there is an error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9103c-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9103c-115">Error codes</span></span>

<span data-ttu-id="9103c-116">À la fin de la **méthode \_ SpawnDerivedClass** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="9103c-116">After the completion of the **SpawnDerivedClass\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9103c-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9103c-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9103c-118">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9103c-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9103c-119">**wbemErrIllegalOperation** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="9103c-119">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="9103c-120">L’utilisateur a demandé une opération non conforme, telle que la génération d’une classe à partir d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9103c-120">User requested an illegal operation, such as spawning a class from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="9103c-121">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="9103c-121">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="9103c-122">La classe source n’a pas été entièrement définie ou inscrite avec WMI, de sorte qu’une nouvelle classe dérivée n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="9103c-122">Source class was not completely defined or registered with WMI, so a new derived class is not permitted.</span></span>

</dd> <dt>

<span data-ttu-id="9103c-123">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9103c-123">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9103c-124">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="9103c-124">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9103c-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9103c-125">Remarks</span></span>

<span data-ttu-id="9103c-126">L’objet qui est retourné automatiquement devient une sous-classe de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="9103c-126">The object that is returned automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="9103c-127">Ce comportement ne peut pas être substitué.</span><span class="sxs-lookup"><span data-stu-id="9103c-127">This behavior cannot be overridden.</span></span> <span data-ttu-id="9103c-128">Il n’existe aucune autre méthode permettant de créer des classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="9103c-128">There is no other method by which you can create derived classes.</span></span>

<span data-ttu-id="9103c-129">Vous ne pouvez pas créer une classe dérivée à partir d’une classe qui est locale à votre propre processus client.</span><span class="sxs-lookup"><span data-stu-id="9103c-129">You cannot create a derived class from a class that is local to your own client process.</span></span> <span data-ttu-id="9103c-130">Avant d’utiliser cette méthode pour créer une classe dérivée, vous devez créer la classe de base.</span><span class="sxs-lookup"><span data-stu-id="9103c-130">Before use this method to create a derived class, you must create the base class.</span></span> <span data-ttu-id="9103c-131">Pour créer la classe de base, appelez [**SWbemObject. \_ put**](swbemobject-put-.md)et récupérez la classe de base à l’aide de [**SWbemServices. obtenir**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="9103c-131">To create the base class, call [**SWbemObject.Put\_**](swbemobject-put-.md), and retrieve the base class using [**SWbemServices.Get**](swbemservices-get.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9103c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9103c-132">Requirements</span></span>



| <span data-ttu-id="9103c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9103c-133">Requirement</span></span> | <span data-ttu-id="9103c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9103c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9103c-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9103c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9103c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9103c-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9103c-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9103c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9103c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9103c-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9103c-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="9103c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9103c-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9103c-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9103c-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9103c-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="9103c-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9103c-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9103c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9103c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9103c-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9103c-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9103c-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="9103c-145">CLSID</span></span><br/>                    | <span data-ttu-id="9103c-146">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="9103c-146">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="9103c-147">IID</span><span class="sxs-lookup"><span data-stu-id="9103c-147">IID</span></span><br/>                      | <span data-ttu-id="9103c-148">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="9103c-148">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




