---
description: 'L’interface ISampleGrabberCB fournit des méthodes de rappel pour la méthode ISampleGrabber :: SetCallback. Si votre application appelle cette méthode, elle doit implémenter cette interface. Pour plus d’informations, consultez ISampleGrabber.'
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Interface ISampleGrabberCB (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526020"
---
# <a name="isamplegrabbercb-interface"></a><span data-ttu-id="4788c-105">Interface ISampleGrabberCB</span><span class="sxs-lookup"><span data-stu-id="4788c-105">ISampleGrabberCB interface</span></span>

> [!Note]  
> <span data-ttu-id="4788c-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="4788c-106">\[Deprecated.</span></span> <span data-ttu-id="4788c-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4788c-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4788c-108">L' `ISampleGrabberCB` interface fournit des méthodes de rappel pour la méthode [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="4788c-108">The `ISampleGrabberCB` interface provides callback methods for the [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) method.</span></span> <span data-ttu-id="4788c-109">Si votre application appelle cette méthode, elle doit implémenter cette interface.</span><span class="sxs-lookup"><span data-stu-id="4788c-109">If your application calls that method, it must implement this interface.</span></span> <span data-ttu-id="4788c-110">Pour plus d’informations, consultez [**ISampleGrabber**](isamplegrabber.md).</span><span class="sxs-lookup"><span data-stu-id="4788c-110">For more information, see [**ISampleGrabber**](isamplegrabber.md).</span></span>

## <a name="members"></a><span data-ttu-id="4788c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="4788c-111">Members</span></span>

<span data-ttu-id="4788c-112">L’interface **ISampleGrabberCB** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4788c-112">The **ISampleGrabberCB** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4788c-113">**ISampleGrabberCB** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4788c-113">**ISampleGrabberCB** also has these types of members:</span></span>

-   [<span data-ttu-id="4788c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4788c-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4788c-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4788c-115">Methods</span></span>

<span data-ttu-id="4788c-116">L’interface **ISampleGrabberCB** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4788c-116">The **ISampleGrabberCB** interface has these methods.</span></span>



| <span data-ttu-id="4788c-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="4788c-117">Method</span></span>                                        | <span data-ttu-id="4788c-118">Description</span><span class="sxs-lookup"><span data-stu-id="4788c-118">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="4788c-119">**BufferCB**</span><span class="sxs-lookup"><span data-stu-id="4788c-119">**BufferCB**</span></span>](isamplegrabbercb-buffercb.md) | <span data-ttu-id="4788c-120">Méthode de rappel qui reçoit un pointeur vers l’exemple de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4788c-120">Callback method that receives a pointer to the sample buffer.</span></span><br/> |
| [<span data-ttu-id="4788c-121">**SampleCB**</span><span class="sxs-lookup"><span data-stu-id="4788c-121">**SampleCB**</span></span>](isamplegrabbercb-samplecb.md) | <span data-ttu-id="4788c-122">Méthode de rappel qui reçoit un pointeur vers l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="4788c-122">Callback method that receives a pointer to the media sample.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="4788c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4788c-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4788c-124">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="4788c-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4788c-125">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4788c-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4788c-126">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4788c-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4788c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4788c-127">Requirements</span></span>



| <span data-ttu-id="4788c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4788c-128">Requirement</span></span> | <span data-ttu-id="4788c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4788c-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4788c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="4788c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4788c-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4788c-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4788c-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4788c-132">Library</span></span><br/> | <dl> <span data-ttu-id="4788c-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4788c-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
