---
description: Fournit une instance de IMFMuxStreamSampleManager qui est utilisée pour accéder à la collection d’exemples à partir des sous-flux d’une source de média multiplexée.
ms.assetid: 4FD8169D-FDDF-4C69-AD46-05B02B35028C
title: Attribut MFSampleExtension_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b46c277265538ccb2b990ea9d912b9337bcd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106537000"
---
# <a name="mfsampleextension_multiplexed_manager-attribute"></a><span data-ttu-id="1969b-103">\_Attribut MFSampleExtension Multiplexed \_ Manager</span><span class="sxs-lookup"><span data-stu-id="1969b-103">MFSampleExtension\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="1969b-104">Fournit une instance de [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) qui est utilisée pour accéder à la collection d’exemples à partir des sous-flux d’une source de média multiplexée.</span><span class="sxs-lookup"><span data-stu-id="1969b-104">Provides an instance of [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) which is used to access the collection of samples from the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="1969b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1969b-105">Data type</span></span>

<span data-ttu-id="1969b-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="1969b-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="1969b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1969b-107">Remarks</span></span>

<span data-ttu-id="1969b-108">Transmettez cette valeur dans [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) pour recevoir une instance de [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager).</span><span class="sxs-lookup"><span data-stu-id="1969b-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to get an instance of [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="1969b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1969b-109">Requirements</span></span>



| <span data-ttu-id="1969b-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1969b-110">Requirement</span></span> | <span data-ttu-id="1969b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1969b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1969b-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1969b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1969b-113">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1969b-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1969b-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1969b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1969b-115">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1969b-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="1969b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="1969b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1969b-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1969b-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
