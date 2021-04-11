---
title: IDeviceIcon, méthode de hauteur
description: Récupère la hauteur de l’icône en pixels.
ms.assetid: 06E1B3AD-FF49-4BC9-AC67-E2E00954475F
keywords:
- API de diffusion multimédia en continu de la méthode Height
- Méthode Height diffusion multimédia en continu API, interface IDeviceIcon
- API de diffusion multimédia en continu de l’interface IDeviceIcon, méthode Height
topic_type:
- apiref
api_name:
- IDeviceIcon.Height
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdba8d107cc844a29d215e5da49949595a8cd27a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031229"
---
# <a name="ideviceiconheight-method"></a><span data-ttu-id="108d2-106">IDeviceIcon :: Height, méthode</span><span class="sxs-lookup"><span data-stu-id="108d2-106">IDeviceIcon::Height method</span></span>

<span data-ttu-id="108d2-107">Récupère la hauteur de l’icône en pixels.</span><span class="sxs-lookup"><span data-stu-id="108d2-107">Retrieves the height of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="108d2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="108d2-108">Syntax</span></span>


```C++
HRESULT Height(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="108d2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="108d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="108d2-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="108d2-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="108d2-111">Reçoit un pointeur vers la hauteur de l’icône en pixels.</span><span class="sxs-lookup"><span data-stu-id="108d2-111">Receives a pointer to the height of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="108d2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="108d2-112">Return value</span></span>

<span data-ttu-id="108d2-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="108d2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="108d2-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="108d2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="108d2-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="108d2-115">Return code</span></span>                                                                          | <span data-ttu-id="108d2-116">Description</span><span class="sxs-lookup"><span data-stu-id="108d2-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="108d2-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="108d2-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="108d2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="108d2-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="108d2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="108d2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="108d2-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="108d2-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

