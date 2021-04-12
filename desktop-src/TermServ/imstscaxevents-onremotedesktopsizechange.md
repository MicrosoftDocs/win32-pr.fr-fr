---
title: Méthode IMsTscAxEvents OnRemoteDesktopSizeChange
description: Appelé pour indiquer que la taille du contrôle client sur le Bureau à distance a changé en réponse à une opération de contrôle client.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRemoteDesktopSizeChange
- Méthode OnRemoteDesktopSizeChange Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRemoteDesktopSizeChange
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508758"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a><span data-ttu-id="8432b-106">IMsTscAxEvents :: OnRemoteDesktopSizeChange, méthode</span><span class="sxs-lookup"><span data-stu-id="8432b-106">IMsTscAxEvents::OnRemoteDesktopSizeChange method</span></span>

<span data-ttu-id="8432b-107">Appelé pour indiquer que la taille du contrôle client sur le Bureau à distance a changé en réponse à une opération de contrôle client.</span><span class="sxs-lookup"><span data-stu-id="8432b-107">Called to indicate that the size of the client control on the remote desktop has changed in response to a client control operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8432b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8432b-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="8432b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8432b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8432b-110">*largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8432b-110">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8432b-111">Largeur, en pixels, du Bureau à distance redimensionné.</span><span class="sxs-lookup"><span data-stu-id="8432b-111">Width, in pixels, of the resized remote desktop.</span></span>

</dd> <dt>

<span data-ttu-id="8432b-112">*hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8432b-112">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8432b-113">Hauteur, en pixels, du Bureau à distance redimensionné.</span><span class="sxs-lookup"><span data-stu-id="8432b-113">Height, in pixels, of the resized remote desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8432b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8432b-114">Return value</span></span>

<span data-ttu-id="8432b-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8432b-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8432b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8432b-116">Remarks</span></span>

<span data-ttu-id="8432b-117">Cet événement permet au conteneur de déterminer s’il doit se redimensionner en réponse à une opération de contrôle client, ce qui peut entraîner une plus grande taille de bureau affichable.</span><span class="sxs-lookup"><span data-stu-id="8432b-117">This event allows the container to determine if it must resize itself in response to a client control operation, which could result in a larger viewable desktop size.</span></span> <span data-ttu-id="8432b-118">Notez que le contrôle ajuste automatiquement les barres de défilement pour la nouvelle taille de session.</span><span class="sxs-lookup"><span data-stu-id="8432b-118">Note that the control will automatically adjust scroll bars for the new session size.</span></span>

<span data-ttu-id="8432b-119">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8432b-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8432b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8432b-120">Requirements</span></span>



| <span data-ttu-id="8432b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8432b-121">Requirement</span></span> | <span data-ttu-id="8432b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8432b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8432b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8432b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8432b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8432b-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8432b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8432b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8432b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8432b-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8432b-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8432b-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="8432b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8432b-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8432b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8432b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8432b-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8432b-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8432b-131">IID</span><span class="sxs-lookup"><span data-stu-id="8432b-131">IID</span></span><br/>                      | <span data-ttu-id="8432b-132">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="8432b-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8432b-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8432b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8432b-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="8432b-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





