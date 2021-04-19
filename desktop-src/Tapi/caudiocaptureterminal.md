---
description: Le terminal CAudioCaptureTerminal est dérivé de CSingleFilterTerminal et implémente un terminal de capture audio statique pour les appareils Wave à l’aide du filtre Wave DirectShow. La plupart des MSP n’ont pas besoin de remplacer l’implémentation de ce terminal.
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: CAudioCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519401"
---
# <a name="caudiocaptureterminal"></a><span data-ttu-id="c59dd-104">CAudioCaptureTerminal</span><span class="sxs-lookup"><span data-stu-id="c59dd-104">CAudioCaptureTerminal</span></span>

<span data-ttu-id="c59dd-105">Le terminal **CAudioCaptureTerminal** est dérivé de [CSingleFilterTerminal](csinglefilterterminal.md) et implémente un terminal de capture audio statique pour les appareils Wave à l’aide du filtre Wave DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c59dd-105">The **CAudioCaptureTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio capture terminal for wave devices using the DirectShow wavein filter.</span></span> <span data-ttu-id="c59dd-106">La plupart des MSP n’ont pas besoin de remplacer l’implémentation de ce terminal.</span><span class="sxs-lookup"><span data-stu-id="c59dd-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="c59dd-107">Défini dans MSPtmac. h.</span><span class="sxs-lookup"><span data-stu-id="c59dd-107">Defined in MSPtmac.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="c59dd-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c59dd-108">Remarks</span></span>

<span data-ttu-id="c59dd-109">Les méthodes [**put \_ Solde**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) et [**obtenir l' \_ équilibre**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioCaptureTerminal** ne sont pas implémentées et retournent E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c59dd-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioCaptureTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



