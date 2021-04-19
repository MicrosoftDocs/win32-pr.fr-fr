---
description: Le terminal CAudioRenderTerminal est dérivé de CSingleFilterTerminal et implémente un terminal de rendu audio statique pour les appareils Wave à l’aide du filtre DirectShow WaveOut. La plupart des MSP n’ont pas besoin de remplacer l’implémentation de ce terminal.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544970"
---
# <a name="caudiorenderterminal"></a><span data-ttu-id="98bfc-104">CAudioRenderTerminal</span><span class="sxs-lookup"><span data-stu-id="98bfc-104">CAudioRenderTerminal</span></span>

<span data-ttu-id="98bfc-105">Le terminal **CAudioRenderTerminal** est dérivé de [CSingleFilterTerminal](csinglefilterterminal.md) et implémente un terminal de rendu audio statique pour les appareils Wave à l’aide du filtre DirectShow WaveOut.</span><span class="sxs-lookup"><span data-stu-id="98bfc-105">The **CAudioRenderTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio render terminal for wave devices using the DirectShow waveout filter.</span></span> <span data-ttu-id="98bfc-106">La plupart des MSP n’ont pas besoin de remplacer l’implémentation de ce terminal.</span><span class="sxs-lookup"><span data-stu-id="98bfc-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="98bfc-107">Défini dans MSPtrmar. h.</span><span class="sxs-lookup"><span data-stu-id="98bfc-107">Defined in MSPtrmar.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="98bfc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="98bfc-108">Remarks</span></span>

<span data-ttu-id="98bfc-109">Les méthodes [**put \_ Solde**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) et [**obtenir l' \_ équilibre**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioRenderTerminal** ne sont pas implémentées et retournent E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="98bfc-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioRenderTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



