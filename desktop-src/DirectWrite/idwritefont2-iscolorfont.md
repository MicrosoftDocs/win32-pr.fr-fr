---
title: Méthode IDWriteFont2 IsColorFont
description: Permet de déterminer si un chemin d’accès de rendu des couleurs est potentiellement nécessaire.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Écriture directe de la méthode IsColorFont
- Méthode IsColorFont Write directe, interface IDWriteFont2
- Écriture directe de l’interface IDWriteFont2, méthode IsColorFont
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384923"
---
# <a name="idwritefont2iscolorfont-method"></a><span data-ttu-id="a4062-106">IDWriteFont2 :: IsColorFont, méthode</span><span class="sxs-lookup"><span data-stu-id="a4062-106">IDWriteFont2::IsColorFont method</span></span>

<span data-ttu-id="a4062-107">Permet de déterminer si un chemin d’accès de rendu des couleurs est potentiellement nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a4062-107">Enables determining if a color rendering path is potentially necessary.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4062-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4062-108">Syntax</span></span>


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a><span data-ttu-id="a4062-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4062-109">Parameters</span></span>

<span data-ttu-id="a4062-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a4062-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4062-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4062-111">Return value</span></span>

<span data-ttu-id="a4062-112">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="a4062-112">Type: **BOOL**</span></span>

<span data-ttu-id="a4062-113">Retourne la **valeur true** si la police contient des informations sur la couleur (tables colr et CPAL); Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="a4062-113">Returns **TRUE** if the font has color information (COLR and CPAL tables); otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4062-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4062-114">Requirements</span></span>



| <span data-ttu-id="a4062-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4062-115">Requirement</span></span> | <span data-ttu-id="a4062-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4062-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4062-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4062-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4062-118">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a4062-118">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="a4062-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4062-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4062-120">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a4062-120">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a4062-121">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4062-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a4062-122">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="a4062-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="a4062-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a4062-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4062-124"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4062-124"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a4062-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a4062-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4062-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4062-126"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4062-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4062-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4062-128">**IDWriteFont2**</span><span class="sxs-lookup"><span data-stu-id="a4062-128">**IDWriteFont2**</span></span>](idwritefont2.md)
</dt> </dl>

 

 





