---
description: Crée un objet de transformation de couleur qui implémente IWICColorTransform. Cet objet COM prend en charge le modèle objet à thread libre.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540204"
---
# <a name="wiccreatecolortransform_proxy-function"></a><span data-ttu-id="860d5-104">\_Fonction proxy WICCreateColorTransform</span><span class="sxs-lookup"><span data-stu-id="860d5-104">WICCreateColorTransform\_Proxy function</span></span>

<span data-ttu-id="860d5-105">Crée un objet de transformation de couleur qui implémente [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span><span class="sxs-lookup"><span data-stu-id="860d5-105">Creates an color transform object that implements [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span></span> <span data-ttu-id="860d5-106">Cet objet COM prend en charge le modèle objet à thread libre.</span><span class="sxs-lookup"><span data-stu-id="860d5-106">This COM object supports the free-threaded object model.</span></span>

## <a name="syntax"></a><span data-ttu-id="860d5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="860d5-107">Syntax</span></span>


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a><span data-ttu-id="860d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="860d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="860d5-109">*ppIColorTransform* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="860d5-109">*ppIColorTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="860d5-110">Transformation de couleur créée.</span><span class="sxs-lookup"><span data-stu-id="860d5-110">The color transform created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="860d5-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="860d5-111">Return value</span></span>

<span data-ttu-id="860d5-112">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="860d5-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="860d5-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="860d5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="860d5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="860d5-114">Requirements</span></span>



| <span data-ttu-id="860d5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="860d5-115">Requirement</span></span> | <span data-ttu-id="860d5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="860d5-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="860d5-117">DLL</span><span class="sxs-lookup"><span data-stu-id="860d5-117">DLL</span></span><br/> | <dl> <span data-ttu-id="860d5-118"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="860d5-118"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 
