---
description: Étend les fonctionnalités de SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Objet SWbemServicesEx (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114855"
---
# <a name="swbemservicesex-object"></a><span data-ttu-id="e416a-103">Objet SWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="e416a-103">SWbemServicesEx object</span></span>

<span data-ttu-id="e416a-104">L’objet **SWbemServicesEx** étend les fonctionnalités de [**SWbemServices**](swbemservices.md).</span><span class="sxs-lookup"><span data-stu-id="e416a-104">The **SWbemServicesEx** object extends the functionality of [**SWbemServices**](swbemservices.md).</span></span> <span data-ttu-id="e416a-105">Les méthodes [**put**](swbemservicesex-put.md) et [**PutAsync**](swbemservicesex-putasync.md) permettent d’enregistrer une classe ou une instance dans plusieurs espaces de noms ou dans un espace de noms différent de celui dans lequel une instance a été créée.</span><span class="sxs-lookup"><span data-stu-id="e416a-105">The [**Put**](swbemservicesex-put.md) and [**PutAsync**](swbemservicesex-putasync.md) methods allow a class or an instance to be saved to multiple namespaces or to a different namespace than the one where an instance was created.</span></span> <span data-ttu-id="e416a-106">Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e416a-106">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="e416a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e416a-107">Members</span></span>

<span data-ttu-id="e416a-108">L’objet **SWbemServicesEx** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e416a-108">The **SWbemServicesEx** object has these types of members:</span></span>

-   [<span data-ttu-id="e416a-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e416a-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e416a-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e416a-110">Methods</span></span>

<span data-ttu-id="e416a-111">L’objet **SWbemServicesEx** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e416a-111">The **SWbemServicesEx** object has these methods.</span></span>



| <span data-ttu-id="e416a-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="e416a-112">Method</span></span>                                       | <span data-ttu-id="e416a-113">Description</span><span class="sxs-lookup"><span data-stu-id="e416a-113">Description</span></span>                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e416a-114">**Posé**</span><span class="sxs-lookup"><span data-stu-id="e416a-114">**Put**</span></span>](swbemservicesex-put.md)           | <span data-ttu-id="e416a-115">Enregistre l’objet dans l’espace de noms lié à l’objet **SWbemServicesEx** et retourne un objet [**SWbemObjectPath**](swbemobjectpath.md) qui contient le chemin d’accès de l’objet dans lequel les données ont été écrites.</span><span class="sxs-lookup"><span data-stu-id="e416a-115">Saves the object to the namespace bound to the **SWbemServicesEx** object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span><br/> |
| [<span data-ttu-id="e416a-116">**PutAsync**</span><span class="sxs-lookup"><span data-stu-id="e416a-116">**PutAsync**</span></span>](swbemservicesex-putasync.md) | <span data-ttu-id="e416a-117">Enregistre un objet de façon asynchrone dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e416a-117">Saves an object asynchronously to a namespace.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="e416a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e416a-118">Remarks</span></span>

<span data-ttu-id="e416a-119">Les méthodes de cette classe peuvent être appelées en mode semi-synchrone ou en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e416a-119">The methods in this class can be called in either the semisynchronous mode or the asynchronous mode.</span></span> <span data-ttu-id="e416a-120">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="e416a-120">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e416a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e416a-121">Requirements</span></span>



| <span data-ttu-id="e416a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e416a-122">Requirement</span></span> | <span data-ttu-id="e416a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e416a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e416a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e416a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e416a-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e416a-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e416a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e416a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e416a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e416a-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e416a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e416a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e416a-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e416a-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e416a-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e416a-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="e416a-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e416a-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e416a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e416a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e416a-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e416a-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e416a-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="e416a-134">CLSID</span></span><br/>                    | <span data-ttu-id="e416a-135">CLSID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="e416a-135">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="e416a-136">IID</span><span class="sxs-lookup"><span data-stu-id="e416a-136">IID</span></span><br/>                      | <span data-ttu-id="e416a-137">IID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="e416a-137">IID\_ISWbemServicesEx</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="e416a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e416a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e416a-139">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="e416a-139">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="e416a-140">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="e416a-140">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

