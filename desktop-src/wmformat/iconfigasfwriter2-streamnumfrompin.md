---
title: Méthode IConfigAsfWriter2 StreamNumFromPin
description: La méthode StreamNumFromPin récupère le numéro de flux associé à la broche d’entrée spécifiée.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Méthode StreamNumFromPin format Windows Media
- Méthode StreamNumFromPin format Windows Media, interface IConfigAsfWriter2
- Interface IConfigAsfWriter2 Windows Media format, méthode StreamNumFromPin
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382092"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a><span data-ttu-id="29afa-106">IConfigAsfWriter2 :: StreamNumFromPin, méthode</span><span class="sxs-lookup"><span data-stu-id="29afa-106">IConfigAsfWriter2::StreamNumFromPin method</span></span>

<span data-ttu-id="29afa-107">La méthode **StreamNumFromPin** récupère le numéro de flux associé à la broche d’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29afa-107">The **StreamNumFromPin** method retrieves the stream number associated with the specified input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="29afa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29afa-108">Syntax</span></span>


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a><span data-ttu-id="29afa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29afa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29afa-110">*pPin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29afa-110">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29afa-111">Pointeur vers l’interface **IPIN** sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="29afa-111">Pointer to the **IPin** interface on the input pin.</span></span>

</dd> <dt>

<span data-ttu-id="29afa-112">*pwStreamNum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="29afa-112">*pwStreamNum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29afa-113">Pointeur qui reçoit le numéro de flux.</span><span class="sxs-lookup"><span data-stu-id="29afa-113">Pointer that receives the stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29afa-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29afa-114">Return value</span></span>

<span data-ttu-id="29afa-115">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29afa-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="29afa-116">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29afa-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29afa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="29afa-117">Remarks</span></span>

<span data-ttu-id="29afa-118">Parfois, vous devrez peut-être utiliser directement les interfaces du kit de développement logiciel (SDK) du format Windows Media pour manipuler un flux avant d’exécuter un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="29afa-118">Sometimes you may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running a filter graph.</span></span> <span data-ttu-id="29afa-119">Étant donné que vous ne pouvez pas supposer qu’un numéro de flux ASF est le même que le numéro de code confidentiel DirectShow, cette méthode est fournie.</span><span class="sxs-lookup"><span data-stu-id="29afa-119">Because you cannot assume that an ASF stream number is the same as the DirectShow pin number, this method is provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="29afa-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29afa-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="29afa-121">[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="29afa-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

 