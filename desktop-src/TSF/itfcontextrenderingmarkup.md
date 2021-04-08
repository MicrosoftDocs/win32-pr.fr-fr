---
title: Interface ITfContextRenderingMarkup
description: L’interface ITfContextRenderingMarkup est implémentée par le gestionnaire TSF et utilisée par les applications. Cette interface peut être récupérée à l’aide de IQueryInterface à partir de l’objet ITfContext. Cette interface permet à l’application d’énumérer les informations de rendu.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- ITfContextRenderingMarkup interface Text Services Framework
- ITfContextRenderingMarkup interface Text Services Framework, Description
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842466"
---
# <a name="itfcontextrenderingmarkup-interface"></a><span data-ttu-id="de08c-107">Interface ITfContextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="de08c-107">ITfContextRenderingMarkup interface</span></span>

<span data-ttu-id="de08c-108">L’interface **ITfContextRenderingMarkup** est implémentée par le gestionnaire TSF et utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="de08c-108">The **ITfContextRenderingMarkup** interface is implemented by TSF manager and used by applications.</span></span> <span data-ttu-id="de08c-109">Cette interface peut être récupérée à l’aide de IQueryInterface à partir de l’objet [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) .</span><span class="sxs-lookup"><span data-stu-id="de08c-109">This interface can be retrieved using IQueryInterface from [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) object.</span></span> <span data-ttu-id="de08c-110">Cette interface permet à l’application d’énumérer les informations de rendu.</span><span class="sxs-lookup"><span data-stu-id="de08c-110">This interface helps the application enumerate rendering information.</span></span>



| <span data-ttu-id="de08c-111">Méthodes ITfContextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="de08c-111">ITfContextRenderingMarkup methods</span></span>                                                | <span data-ttu-id="de08c-112">Description</span><span class="sxs-lookup"><span data-stu-id="de08c-112">Description</span></span>                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="de08c-113">GetRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="de08c-113">GetRenderingMarkup</span></span>](itfcontextrenderingmarkup-getrenderingmarkup.md)           | <span data-ttu-id="de08c-114">Récupère un énumérateur des balises de rendu pour la plage donnée.</span><span class="sxs-lookup"><span data-stu-id="de08c-114">Retrieves an enumerator of the rendering markups for the given range.</span></span> |
| [<span data-ttu-id="de08c-115">FindNextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="de08c-115">FindNextRenderingMarkup</span></span>](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | <span data-ttu-id="de08c-116">Cette fonction n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="de08c-116">This function is not implemented.</span></span> <span data-ttu-id="de08c-117">Elle retourne toujours E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="de08c-117">It always returns E\_NOTIMPL.</span></span>       |



 

## <a name="members"></a><span data-ttu-id="de08c-118">Membres</span><span class="sxs-lookup"><span data-stu-id="de08c-118">Members</span></span>

<span data-ttu-id="de08c-119">L’interface **ITfContextRenderingMarkup** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="de08c-119">The **ITfContextRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="de08c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="de08c-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="de08c-121">Cette interface n’est pas actuellement dans les fichiers d’en-tête publics.</span><span class="sxs-lookup"><span data-stu-id="de08c-121">This interface is not currently in the public header files.</span></span> <span data-ttu-id="de08c-122">Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="de08c-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 