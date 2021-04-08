---
title: Interface IWMDRMProvider
description: L’interface IWMDRMProvider fournit une méthode qui crée les autres objets des API étendues du client Microsoft Windows Media DRM. vous pouvez obtenir un pointeur vers une instance de cette interface en appelant la fonction WMDRMCreateProvider.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Format Windows Media de l’interface IWMDRMProvider
- Interface IWMDRMProvider format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729213"
---
# <a name="iwmdrmprovider-interface"></a><span data-ttu-id="81099-105">Interface IWMDRMProvider</span><span class="sxs-lookup"><span data-stu-id="81099-105">IWMDRMProvider interface</span></span>

<span data-ttu-id="81099-106">L’interface **IWMDRMProvider** fournit une méthode qui crée les autres objets des API étendues du client Microsoft Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="81099-106">The **IWMDRMProvider** interface provides a method that creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="81099-107">Vous pouvez obtenir un pointeur vers une instance de cette interface en appelant la fonction [**WMDRMCreateProvider**](wmdrmcreateprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="81099-107">You can obtain a pointer to an instance of this interface by calling the [**WMDRMCreateProvider**](wmdrmcreateprovider.md) function.</span></span> <span data-ttu-id="81099-108">Pour obtenir un pointeur vers une instance de cette interface qui peut créer des objets sécurisés, vous devez appeler la fonction [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="81099-108">To obtain a pointer to an instance of this interface that can create secure objects, you must call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="81099-109">Membres</span><span class="sxs-lookup"><span data-stu-id="81099-109">Members</span></span>

<span data-ttu-id="81099-110">L’interface **IWMDRMProvider** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="81099-110">The **IWMDRMProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="81099-111">**IWMDRMProvider** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="81099-111">**IWMDRMProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="81099-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="81099-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="81099-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="81099-113">Methods</span></span>

<span data-ttu-id="81099-114">L’interface **IWMDRMProvider** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="81099-114">The **IWMDRMProvider** interface has these methods.</span></span>



| <span data-ttu-id="81099-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="81099-115">Method</span></span>                                              | <span data-ttu-id="81099-116">Description</span><span class="sxs-lookup"><span data-stu-id="81099-116">Description</span></span>                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81099-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="81099-117">**CreateObject**</span></span>](iwmdrmprovider-createobject.md) | <span data-ttu-id="81099-118">Récupère un pointeur vers une interface spécifiée, en créant l’objet d’implémentation, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="81099-118">Retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="81099-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81099-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81099-120">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="81099-120">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

