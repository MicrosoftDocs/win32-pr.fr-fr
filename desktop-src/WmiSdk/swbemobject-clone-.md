---
description: La méthode Clone \_ de l’objet SWbemObject retourne un nouvel objet qui est un clone de l’objet actuel.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: Méthode SWbemObject.Clone_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035076"
---
# <a name="swbemobjectclone_-method"></a><span data-ttu-id="830fc-103">SWbemObject. Clone, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="830fc-103">SWbemObject.Clone\_ method</span></span>

<span data-ttu-id="830fc-104">La **méthode \_ clone** de l’objet [**SWbemObject**](swbemobject.md) retourne un nouvel objet qui est un clone de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="830fc-104">The **Clone\_** method of the [**SWbemObject**](swbemobject.md) object returns a new object that is a clone of the current object.</span></span>

<span data-ttu-id="830fc-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="830fc-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="830fc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="830fc-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="830fc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="830fc-107">Parameters</span></span>

<span data-ttu-id="830fc-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="830fc-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="830fc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="830fc-109">Return value</span></span>

<span data-ttu-id="830fc-110">En cas de réussite, cette méthode retourne un nouvel objet [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="830fc-110">If successful, this method returns a new [**SWbemObject**](swbemobject.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="830fc-111">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="830fc-111">Error codes</span></span>

<span data-ttu-id="830fc-112">Une fois la méthode **clone \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="830fc-112">After completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="830fc-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="830fc-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="830fc-114">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="830fc-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="830fc-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="830fc-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="830fc-116">**Rien** n’a été spécifié en tant que paramètre et n’est pas acceptable dans cette utilisation.</span><span class="sxs-lookup"><span data-stu-id="830fc-116">**Nothing** was specified as a parameter, and it is not acceptable in this usage.</span></span>

</dd> <dt>

<span data-ttu-id="830fc-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="830fc-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="830fc-118">Mémoire insuffisante pour cloner l’objet.</span><span class="sxs-lookup"><span data-stu-id="830fc-118">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="830fc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="830fc-119">Remarks</span></span>

<span data-ttu-id="830fc-120">Utilisez la **méthode \_ clone** pour dupliquer une définition de classe ou une instance.</span><span class="sxs-lookup"><span data-stu-id="830fc-120">Use the **Clone\_** method to duplicate a class definition or an instance.</span></span> <span data-ttu-id="830fc-121">Cela est utile lorsque vous avez besoin de la copie d’origine de l’objet à des fins de sauvegarde lors de la modification d’une nouvelle copie.</span><span class="sxs-lookup"><span data-stu-id="830fc-121">This is useful when you need the original copy of the object for backup purposes while you are modifying a new copy.</span></span> <span data-ttu-id="830fc-122">De même, utilisez cette méthode pour créer un grand nombre de nouvelles instances à partir d’une seule instance source.</span><span class="sxs-lookup"><span data-stu-id="830fc-122">Likewise, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="830fc-123">Par exemple, utilisez [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) pour créer une instance de démarrage unique et utilisez **SWbemObject. Clone \_** pour produire rapidement 100 copies de l’instance.</span><span class="sxs-lookup"><span data-stu-id="830fc-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance, and use **SWbemObject.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="830fc-124">Par la suite, vous pouvez modifier les objets, en attribuant à chacune d’elles des valeurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="830fc-124">Subsequently, you can modify the objects, giving each one specific values.</span></span>

<span data-ttu-id="830fc-125">Il n’est pas possible d’utiliser cette méthode pour convertir une définition de classe en instance, ni pour convertir une instance en une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="830fc-125">It is not possible to use this method to convert a class definition to an instance, or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="830fc-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="830fc-126">Requirements</span></span>



| <span data-ttu-id="830fc-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="830fc-127">Requirement</span></span> | <span data-ttu-id="830fc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="830fc-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="830fc-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="830fc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="830fc-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="830fc-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="830fc-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="830fc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="830fc-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="830fc-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="830fc-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="830fc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="830fc-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="830fc-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="830fc-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="830fc-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="830fc-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="830fc-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="830fc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="830fc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="830fc-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="830fc-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="830fc-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="830fc-139">CLSID</span></span><br/>                    | <span data-ttu-id="830fc-140">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="830fc-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="830fc-141">IID</span><span class="sxs-lookup"><span data-stu-id="830fc-141">IID</span></span><br/>                      | <span data-ttu-id="830fc-142">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="830fc-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




