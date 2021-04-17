---
description: Accède aux données stockées dans le catalogue COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: COMAdminCatalog, classe (comadmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483616"
---
# <a name="comadmincatalog-class"></a><span data-ttu-id="f8ff1-103">COMAdminCatalog, classe</span><span class="sxs-lookup"><span data-stu-id="f8ff1-103">COMAdminCatalog class</span></span>

<span data-ttu-id="f8ff1-104">Accède aux données stockées dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-104">Accesses the data that is stored in the COM+ catalog.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f8ff1-105">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="f8ff1-105">When to implement</span></span>

<span data-ttu-id="f8ff1-106">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="f8ff1-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8ff1-107">Requirement</span></span> | <span data-ttu-id="f8ff1-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8ff1-108">Value</span></span> |
|------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ff1-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="f8ff1-109">CLSID</span></span>      | <span data-ttu-id="f8ff1-110">CLSID \_ COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="f8ff1-110">CLSID\_COMAdminCatalog</span></span>                                                                                            |
| <span data-ttu-id="f8ff1-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="f8ff1-111">ProgID</span></span>     | <span data-ttu-id="f8ff1-112">L « comadmin. COMAdminCatalog »</span><span class="sxs-lookup"><span data-stu-id="f8ff1-112">L"COMAdmin.COMAdminCatalog"</span></span>                                                                                       |
| <span data-ttu-id="f8ff1-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f8ff1-113">Interfaces</span></span> | [<span data-ttu-id="f8ff1-114">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="f8ff1-114">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [<span data-ttu-id="f8ff1-115">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="f8ff1-115">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="f8ff1-116">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="f8ff1-116">When to use</span></span>

<span data-ttu-id="f8ff1-117">Vous utilisez les objets créés à partir de la classe **COMAdminCatalog** pour commencer l’accès par programme aux données de configuration com+ stockées dans le catalogue com+.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-117">You use objects created from the **COMAdminCatalog** class to begin programmatic access to COM+ configuration data stored in the COM+ catalog.</span></span> <span data-ttu-id="f8ff1-118">Ces informations sous-tendent les dossiers et les éléments de l’arborescence de la console de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-118">This information underlies the folders and items in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="f8ff1-119">La classe **COMAdminCatalog** vous permet d’accéder à des regroupements dans le catalogue, d’installer des applications et des composants com+, de démarrer et d’arrêter des services et de se connecter à des serveurs distants et de les administrer.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-119">The **COMAdminCatalog** class enables you to access collections in the catalog, install COM+ applications and components, start and stop services, and connect to and administer remote servers.</span></span>

<span data-ttu-id="f8ff1-120">Les dossiers de l’outil d’administration Services de composants correspondent aux regroupements du catalogue, que vous pouvez représenter à l’aide d’objets créés à partir de la classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ff1-120">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span> <span data-ttu-id="f8ff1-121">Les éléments des dossiers correspondent aux éléments des collections, que vous pouvez représenter à l’aide d’objets créés à partir de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ff1-121">Items in the folders correspond to items in the collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="f8ff1-122">Les collections et les éléments exposés via [**COMAdminCatalogCollection**](comadmincatalogcollection.md) et [**COMAdminCatalogObject**](comadmincatalogobject.md) ne sont pas tous disponibles dans l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-122">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and [**COMAdminCatalogObject**](comadmincatalogobject.md) are available in the Component Services administration tool.</span></span>

<span data-ttu-id="f8ff1-123">Pour plus d’informations sur des regroupements spécifiques et leurs propriétés, consultez [regroupements d’administration com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="f8ff1-123">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="f8ff1-124">Pour une introduction à l’administration par programme de COM+, consultez automatisation de l' [administration com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="f8ff1-124">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ff1-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f8ff1-125">Remarks</span></span>

<span data-ttu-id="f8ff1-126">Pour créer cet objet, appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="f8ff1-126">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="f8ff1-127">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-127">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="f8ff1-128">Un objet COMAdminCatalog peut être déclaré à l’aide de « comadmin. COMAdminCatalog » comme nom de classe.</span><span class="sxs-lookup"><span data-stu-id="f8ff1-128">A COMAdminCatalog object can be declared using "COMAdmin.COMAdminCatalog" as the class name.</span></span>

<span data-ttu-id="f8ff1-129">Dans COM+ 1,5, fourni avec Windows XP, la classe **COMAdminCatalog** implémente l’interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) .</span><span class="sxs-lookup"><span data-stu-id="f8ff1-129">In COM+ 1.5, released with Windows XP, the **COMAdminCatalog** class implements the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface.</span></span> <span data-ttu-id="f8ff1-130">Toutefois, dans COM+ 1,0, fourni avec Windows 2000, la classe **COMAdminCatalog** implémente uniquement l’interface [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="f8ff1-130">However, in COM+ 1.0, released with Windows 2000, the **COMAdminCatalog** class implements only the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ff1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8ff1-131">Requirements</span></span>



| <span data-ttu-id="f8ff1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8ff1-132">Requirement</span></span> | <span data-ttu-id="f8ff1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8ff1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ff1-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8ff1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ff1-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8ff1-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f8ff1-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8ff1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ff1-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8ff1-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f8ff1-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8ff1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8ff1-139"><dt>Comadmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ff1-139"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8ff1-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="f8ff1-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f8ff1-141"><dt>Comadmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f8ff1-141"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8ff1-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8ff1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ff1-143">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="f8ff1-143">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="f8ff1-144">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="f8ff1-144">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="f8ff1-145">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="f8ff1-145">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[<span data-ttu-id="f8ff1-146">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="f8ff1-146">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

