---
description: Fournit une instance de IMFMuxStreamMediaTypeManager qui peut être utilisée pour obtenir les types de média des sous-flux d’une source de média multiplexée et contrôler la combinaison de sous-flux multiplexés par la source.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: Attribut MF_MEDIATYPE_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96c74bbff8f4858c8467fcd13253cfedf2f5dc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211232"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a><span data-ttu-id="24121-103">\_Attribut de \_ Gestionnaire de multiplexage de MediaType MF \_</span><span class="sxs-lookup"><span data-stu-id="24121-103">MF\_MEDIATYPE\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="24121-104">Fournit une instance de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) qui peut être utilisée pour obtenir les types de média des sous-flux d’une source de média multiplexée et contrôler la combinaison de sous-flux multiplexés par la source.</span><span class="sxs-lookup"><span data-stu-id="24121-104">Provides an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) which can be used to get the media types of the substreams of a multiplexed media source as well as control the combination of substreams that are multiplexed by the source.</span></span>

## <a name="data-type"></a><span data-ttu-id="24121-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="24121-105">Data type</span></span>

<span data-ttu-id="24121-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="24121-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="24121-107">Notes</span><span class="sxs-lookup"><span data-stu-id="24121-107">Remarks</span></span>

<span data-ttu-id="24121-108">Transmettez cette valeur dans [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) pour recevoir une instance de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).</span><span class="sxs-lookup"><span data-stu-id="24121-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to get an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="24121-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24121-109">Requirements</span></span>



| <span data-ttu-id="24121-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24121-110">Requirement</span></span> | <span data-ttu-id="24121-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="24121-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24121-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24121-112">Minimum supported client</span></span><br/> | <span data-ttu-id="24121-113">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24121-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="24121-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24121-114">Minimum supported server</span></span><br/> | <span data-ttu-id="24121-115">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="24121-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="24121-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="24121-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="24121-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24121-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
