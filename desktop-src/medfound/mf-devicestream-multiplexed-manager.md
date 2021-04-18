---
description: Fournit une instance de IMFMuxStreamAttributesManager qui gère les IMFAttributes qui décrivent les sous-flux d’une source de média multiplexée.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: Attribut MF_DEVICESTREAM_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522677"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a><span data-ttu-id="43476-103">\_Attribut de \_ Gestionnaire Multiplexed DEVICESTREAM MF \_</span><span class="sxs-lookup"><span data-stu-id="43476-103">MF\_DEVICESTREAM\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="43476-104">Fournit une instance de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) qui gère les [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) qui décrivent les sous-flux d’une source de média multiplexée.</span><span class="sxs-lookup"><span data-stu-id="43476-104">Provides an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) which manages the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) describing the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="43476-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="43476-105">Data type</span></span>

<span data-ttu-id="43476-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="43476-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="43476-107">Notes</span><span class="sxs-lookup"><span data-stu-id="43476-107">Remarks</span></span>

<span data-ttu-id="43476-108">Transmettez cette valeur dans [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) pour déterminer si la source du média fournit des flux multiplexés et, si c’est le cas, obtenir une instance de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span><span class="sxs-lookup"><span data-stu-id="43476-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to determine if the media source provides multiplexed streams and, if so, get an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="43476-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43476-109">Requirements</span></span>



| <span data-ttu-id="43476-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43476-110">Requirement</span></span> | <span data-ttu-id="43476-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="43476-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43476-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43476-112">Minimum supported client</span></span><br/> | <span data-ttu-id="43476-113">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43476-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="43476-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43476-114">Minimum supported server</span></span><br/> | <span data-ttu-id="43476-115">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="43476-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="43476-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="43476-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="43476-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43476-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
