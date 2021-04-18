---
title: IDeviceIcon, méthode de largeur
description: Récupère la largeur de l’icône en pixels.
ms.assetid: 28ADA921-6808-43B8-966E-BA42B1B52931
keywords:
- Méthode Width API de diffusion multimédia en continu
- Méthode Width API de diffusion multimédia en continu, interface IDeviceIcon
- API de diffusion multimédia en continu de l’interface IDeviceIcon, méthode Width
topic_type:
- apiref
api_name:
- IDeviceIcon.Width
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b04f8c40cc209ccf1261af0fc2f6cdfd329db88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315083"
---
# <a name="ideviceiconwidth-method"></a><span data-ttu-id="ff9dd-106">IDeviceIcon :: Width, méthode</span><span class="sxs-lookup"><span data-stu-id="ff9dd-106">IDeviceIcon::Width method</span></span>

<span data-ttu-id="ff9dd-107">Récupère la largeur de l’icône en pixels.</span><span class="sxs-lookup"><span data-stu-id="ff9dd-107">Retrieves the width of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff9dd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff9dd-108">Syntax</span></span>


```C++
HRESULT Width(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="ff9dd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff9dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff9dd-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ff9dd-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff9dd-111">Reçoit un pointeur vers la largeur de l’icône en pixels.</span><span class="sxs-lookup"><span data-stu-id="ff9dd-111">Receives a pointer to the width of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff9dd-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff9dd-112">Return value</span></span>

<span data-ttu-id="ff9dd-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ff9dd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ff9dd-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ff9dd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ff9dd-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ff9dd-115">Return code</span></span>                                                                          | <span data-ttu-id="ff9dd-116">Description</span><span class="sxs-lookup"><span data-stu-id="ff9dd-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ff9dd-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ff9dd-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ff9dd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff9dd-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ff9dd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff9dd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff9dd-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="ff9dd-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

