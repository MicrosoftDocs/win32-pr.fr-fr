---
title: Interface IEnumTfRenderingMarkup
description: L’interface IEnumTfRenderingMarkup est implémentée par le gestionnaire TSF et utilisée par les applications. Cette interface peut être récupérée par ITfContextRenderingMarkup GetRenderingMarkup et énumère les informations de balisage de rendu.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- IEnumTfRenderingMarkup interface Text Services Framework
- IEnumTfRenderingMarkup interface Text Services Framework, Description
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031651"
---
# <a name="ienumtfrenderingmarkup-interface"></a><span data-ttu-id="f829a-106">Interface IEnumTfRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="f829a-106">IEnumTfRenderingMarkup interface</span></span>

<span data-ttu-id="f829a-107">L’interface **IEnumTfRenderingMarkup** est implémentée par le gestionnaire TSF et utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="f829a-107">The **IEnumTfRenderingMarkup** interface is implemented by TSF Manager and used by applications.</span></span> <span data-ttu-id="f829a-108">Cette interface peut être récupérée par [ITfContextRenderingMarkup :: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) et énumère les informations de balisage de rendu.</span><span class="sxs-lookup"><span data-stu-id="f829a-108">This interface can be retrieved by [ITfContextRenderingMarkup::GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) and enumerates the rendering markup information.</span></span>



| <span data-ttu-id="f829a-109">Méthodes IEnumTfRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="f829a-109">IEnumTfRenderingMarkup methods</span></span>            | <span data-ttu-id="f829a-110">Description</span><span class="sxs-lookup"><span data-stu-id="f829a-110">Description</span></span>                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f829a-111">Répliqué</span><span class="sxs-lookup"><span data-stu-id="f829a-111">Clone</span></span>](ienumtfrenderingmarkup-clone.md) | <span data-ttu-id="f829a-112">La méthode **IEnumTfRenderingMarkup :: Clone** crée une copie de l’objet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="f829a-112">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>                                                                  |
| [<span data-ttu-id="f829a-113">Next</span><span class="sxs-lookup"><span data-stu-id="f829a-113">Next</span></span>](ienumtfrenderingmarkup-next.md)   | <span data-ttu-id="f829a-114">La méthode **IEnumTfRenderingMarkup :: Next** obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="f829a-114">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |
| [<span data-ttu-id="f829a-115">Réinitialiser</span><span class="sxs-lookup"><span data-stu-id="f829a-115">Reset</span></span>](ienumtfrenderingmarkup-reset.md) | <span data-ttu-id="f829a-116">La méthode **IEnumTfRenderingMarkup :: Reset** réinitialise l’objet énumérateur en déplaçant la position actuelle jusqu’au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="f829a-116">The **IEnumTfRenderingMarkup::Reset** method resets the enumerator object by moving the current position to the beginning of the enumeration sequence.</span></span> |
| [<span data-ttu-id="f829a-117">Skip</span><span class="sxs-lookup"><span data-stu-id="f829a-117">Skip</span></span>](ienumtfrenderingmarkup-skip.md)   | <span data-ttu-id="f829a-118">La méthode **IEnumTfRenderingMarkup :: Skip** obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="f829a-118">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |



 

## <a name="members"></a><span data-ttu-id="f829a-119">Membres</span><span class="sxs-lookup"><span data-stu-id="f829a-119">Members</span></span>

<span data-ttu-id="f829a-120">L’interface **IEnumTfRenderingMarkup** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f829a-120">The **IEnumTfRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f829a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="f829a-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f829a-122">Cette interface n’est pas actuellement dans les fichiers d’en-tête publics.</span><span class="sxs-lookup"><span data-stu-id="f829a-122">This interface is not currently in the public header files.</span></span> <span data-ttu-id="f829a-123">Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="f829a-123">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 