---
title: Constantes TS_AS_ (Textstor. h)
description: Les indicateurs suivants spécifient les événements qui appellent les méthodes AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511168"
---
# <a name="ts_as_-constants"></a><span data-ttu-id="3466a-103">TS \_ en tant que \_ \* constantes</span><span class="sxs-lookup"><span data-stu-id="3466a-103">TS\_AS\_\* Constants</span></span>

<span data-ttu-id="3466a-104">Les indicateurs suivants spécifient les événements qui appellent les méthodes **AdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="3466a-104">The following flags specify the events that call the **AdviseSink** methods.</span></span>



| <span data-ttu-id="3466a-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="3466a-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="3466a-106">Description</span><span class="sxs-lookup"><span data-stu-id="3466a-106">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <span data-ttu-id="3466a-107"><dt>**TS \_ En tant que \_ texte \_ modifié**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="3466a-107"><dt>**TS\_AS\_TEXT\_CHANGE**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="3466a-108">Le texte est modifié dans le document.</span><span class="sxs-lookup"><span data-stu-id="3466a-108">Text is changed in the document.</span></span><br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <span data-ttu-id="3466a-109"><dt>**TS \_ AS \_ sel \_ change**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="3466a-109"><dt>**TS\_AS\_SEL\_CHANGE**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="3466a-110">Le texte est sélectionné dans le document.</span><span class="sxs-lookup"><span data-stu-id="3466a-110">Text is selected in the document.</span></span><br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <span data-ttu-id="3466a-111"><dt>**TS \_ En tant que \_ \_ modification**</dt> de la disposition <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="3466a-111"><dt>**TS\_AS\_LAYOUT\_CHANGE**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="3466a-112">La mise en page du document est modifiée.</span><span class="sxs-lookup"><span data-stu-id="3466a-112">The layout of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <span data-ttu-id="3466a-113"><dt>**TS \_ En tant que \_ \_ modification d’attr**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="3466a-113"><dt>**TS\_AS\_ATTR\_CHANGE**</dt> <dt>( 0x8 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="3466a-114">Les attributs du document sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="3466a-114">The attributes of the document is changed.</span></span><br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <span data-ttu-id="3466a-115"><dt>**TS \_ En tant que \_ \_ changement d’État**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="3466a-115"><dt>**TS\_AS\_STATUS\_CHANGE**</dt> <dt>( 0x10 )</dt></span></span> </dl>                                                                                                        | <span data-ttu-id="3466a-116">L’état du document est modifié.</span><span class="sxs-lookup"><span data-stu-id="3466a-116">The status of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <span data-ttu-id="3466a-117"><dt>**TS \_ COMME \_ tous les \_ récepteurs**</dt> <dt>(TS \_ As \_ Text \_ change \| TS \_ As \_ sel change TS comme la modification de la \_ \| \_ \_ disposition \_ \| TS \_ comme \_ attr \_ change TS en \| \_ tant que \_ changement d’état \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="3466a-117"><dt>**TS\_AS\_ALL\_SINKS**</dt> <dt>( TS\_AS\_TEXT\_CHANGE \| TS\_AS\_SEL\_CHANGE \| TS\_AS\_LAYOUT\_CHANGE \| TS\_AS\_ATTR\_CHANGE \| TS\_AS\_STATUS\_CHANGE )</dt></span></span> </dl> | <span data-ttu-id="3466a-118">L’un des quatre événements précédents s’est produit dans le document.</span><span class="sxs-lookup"><span data-stu-id="3466a-118">One of the previous four events occurred in the document.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3466a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3466a-119">Requirements</span></span>



| <span data-ttu-id="3466a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3466a-120">Requirement</span></span> | <span data-ttu-id="3466a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3466a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3466a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3466a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3466a-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3466a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3466a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3466a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3466a-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3466a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3466a-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3466a-126">Redistributable</span></span><br/>          | <span data-ttu-id="3466a-127">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="3466a-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="3466a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3466a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3466a-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="3466a-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="3466a-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="3466a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3466a-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3466a-131"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





