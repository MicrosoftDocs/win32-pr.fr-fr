---
description: Demande de données d’analyse hors connexion.
MS-HAID: vspixengine.IOfflineAnalysisRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IOfflineAnalysisRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1E438545-D4C4-45A7-918E-D3D9DC06BA08
api_name:
- IOfflineAnalysisRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 980c4d9f3b745d197789e5e450e0bf782127ca0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846586"
---
# <a name="span-idvspixengineiofflineanalysisrequestspaniofflineanalysisrequest-interface"></a><span data-ttu-id="780c7-103"><span id="vspixengine.iofflineanalysisrequest"></span>Interface IOfflineAnalysisRequest</span><span class="sxs-lookup"><span data-stu-id="780c7-103"><span id="vspixengine.iofflineanalysisrequest"></span>IOfflineAnalysisRequest interface</span></span>

<span data-ttu-id="780c7-104">Demande de données d’analyse hors connexion.</span><span class="sxs-lookup"><span data-stu-id="780c7-104">Request for offline analysis data.</span></span>

## <a name="members"></a><span data-ttu-id="780c7-105">Membres</span><span class="sxs-lookup"><span data-stu-id="780c7-105">Members</span></span>

<span data-ttu-id="780c7-106">L’interface **IOfflineAnalysisRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="780c7-106">The **IOfflineAnalysisRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="780c7-107">**IOfflineAnalysisRequest** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="780c7-107">**IOfflineAnalysisRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="780c7-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="780c7-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="780c7-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="780c7-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="780c7-110">L’interface **IOfflineAnalysisRequest** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="780c7-110">The **IOfflineAnalysisRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="780c7-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="780c7-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="780c7-112">Description</span><span class="sxs-lookup"><span data-stu-id="780c7-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="780c7-113"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="780c7-113"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-cancelofflineanalysisasync-dword"><strong>CancelOfflineAnalysisAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="780c7-114">Demandes d’annulation de l’analyse hors connexion dans une demande d’analyse hors connexion.</span><span class="sxs-lookup"><span data-stu-id="780c7-114">Requests to cancel offline analysis in an offline analysis request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="780c7-115"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="780c7-115"><a href="/windows/desktop/direct3dtools/iofflineanalysisrequest-requestofflineanalysisasync-enumofflineanalysissource-bstr-bstr-dword-bstr-dword-bstr-iofflineanalysiscallback-ptr"><strong>RequestOfflineAnalysisAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="780c7-116">Demandes d’exécution de l’analyse hors connexion avec la source, le manifeste, les paramètres et le frame spécifiés.</span><span class="sxs-lookup"><span data-stu-id="780c7-116">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="780c7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="780c7-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="780c7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="780c7-118">Header</span></span></p></td><td><span data-ttu-id="780c7-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="780c7-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
