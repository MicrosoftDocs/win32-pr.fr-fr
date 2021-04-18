---
description: Obtient un objet de type IMFCollection contenant des objets IMFSample qui contiennent des unités de couche d’abstraction de réseau (NALUs) et des unités SEI (Supplémental addition information) transmises par un décodeur.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Attribut MFSampleExtension_ForwardedDecodeUnits (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519834"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a><span data-ttu-id="ccc38-103">\_Attribut MFSampleExtension ForwardedDecodeUnits</span><span class="sxs-lookup"><span data-stu-id="ccc38-103">MFSampleExtension\_ForwardedDecodeUnits attribute</span></span>

<span data-ttu-id="ccc38-104">Obtient un objet de type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) contenant des objets [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) qui contiennent des unités de couche d’abstraction de réseau (NALUs) et des unités SEI (Supplémental addition information) transmises par un décodeur.</span><span class="sxs-lookup"><span data-stu-id="ccc38-104">Gets an object of type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) containing [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) objects which contain network abstraction layer units (NALUs) and Supplemental Enhancement Information (SEI) units forwarded by a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="ccc38-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ccc38-105">Data type</span></span>

<span data-ttu-id="ccc38-106">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="ccc38-106">**IUnknown**</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc38-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ccc38-107">Remarks</span></span>

<span data-ttu-id="ccc38-108">La collection contient toutes les unités NALU/SEI personnalisées depuis la suppression du frame précédent avec les octets de prévention de l’émulation.</span><span class="sxs-lookup"><span data-stu-id="ccc38-108">The collection contains all custom NALU/SEI units since previous frame with emulation prevention bytes removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc38-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccc38-109">Requirements</span></span>



| <span data-ttu-id="ccc38-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccc38-110">Requirement</span></span> | <span data-ttu-id="ccc38-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccc38-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc38-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccc38-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc38-113">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccc38-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ccc38-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccc38-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc38-115">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccc38-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ccc38-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccc38-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc38-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc38-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




