---
description: Interface d’origine pour la communication des données relatives à un vsglog.
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2f02538f7acbd88daf166af657382e507a4e5661
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482641"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span data-ttu-id="fbb0b-103"><span id="vspixengine.ipixengine"></span>Interface IPixEngine</span><span class="sxs-lookup"><span data-stu-id="fbb0b-103"><span id="vspixengine.ipixengine"></span>IPixEngine interface</span></span>

<span data-ttu-id="fbb0b-104">Interface d’origine pour la communication des données relatives à un vsglog.</span><span class="sxs-lookup"><span data-stu-id="fbb0b-104">Original interface for communicating data about a vsglog .</span></span>

## <a name="members"></a><span data-ttu-id="fbb0b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="fbb0b-105">Members</span></span>

<span data-ttu-id="fbb0b-106">L’interface **IPixEngine** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fbb0b-106">The **IPixEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fbb0b-107">**IPixEngine** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fbb0b-107">**IPixEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="fbb0b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fbb0b-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="fbb0b-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="fbb0b-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="fbb0b-110">L’interface **IPixEngine** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fbb0b-110">The **IPixEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="fbb0b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="fbb0b-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="fbb0b-112">Description</span><span class="sxs-lookup"><span data-stu-id="fbb0b-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="fbb0b-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbb0b-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fbb0b-114">Ouvre un journal de graphisme.</span><span class="sxs-lookup"><span data-stu-id="fbb0b-114">Opens a graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="fbb0b-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbb0b-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fbb0b-116">Exécute une expérience.</span><span class="sxs-lookup"><span data-stu-id="fbb0b-116">Runs an experiment.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="fbb0b-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbb0b-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fbb0b-118">Enregistre le journal de graphisme à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="fbb0b-118">Saves the graphics log to the specified location.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="fbb0b-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbb0b-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fbb0b-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="fbb0b-120">Not used.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="fbb0b-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>Correct</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbb0b-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>ShutDown</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="fbb0b-122">Arrête le moteur.</span><span class="sxs-lookup"><span data-stu-id="fbb0b-122">Shuts down the engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="fbb0b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbb0b-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fbb0b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbb0b-124">Header</span></span></p></td><td><span data-ttu-id="fbb0b-125">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fbb0b-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
