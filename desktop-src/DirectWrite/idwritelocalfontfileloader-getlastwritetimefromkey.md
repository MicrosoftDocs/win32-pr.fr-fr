---
title: Méthode IDWriteLocalFontFileLoader GetLastWriteTimeFromKey
description: Obtient l’heure de la dernière écriture du fichier à partir de la clé de référence du fichier de police.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Écriture directe de la méthode GetLastWriteTimeFromKey
- Méthode GetLastWriteTimeFromKey Write directe, interface IDWriteLocalFontFileLoader
- Écriture directe de l’interface IDWriteLocalFontFileLoader, méthode GetLastWriteTimeFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526766"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a><span data-ttu-id="19802-106">IDWriteLocalFontFileLoader :: GetLastWriteTimeFromKey, méthode</span><span class="sxs-lookup"><span data-stu-id="19802-106">IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey method</span></span>

<span data-ttu-id="19802-107">Obtient l’heure de la dernière écriture du fichier à partir de la clé de référence du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="19802-107">Obtains the last write time of the file from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="19802-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19802-108">Syntax</span></span>


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="19802-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19802-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19802-110">*fontFileReferenceKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19802-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19802-111">Type : **const void \***</span><span class="sxs-lookup"><span data-stu-id="19802-111">Type: **const void\***</span></span>

<span data-ttu-id="19802-112">Clé de référence du fichier de police qui identifie de façon unique le fichier de police local dans l’étendue du chargeur de polices utilisé.</span><span class="sxs-lookup"><span data-stu-id="19802-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="19802-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="19802-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="19802-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="19802-114">Type: **UINT32**</span></span>

<span data-ttu-id="19802-115">Taille de la clé de référence du fichier de police, en octets.</span><span class="sxs-lookup"><span data-stu-id="19802-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="19802-116">*LastWriteTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="19802-116">*lastWriteTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19802-117">Type : **fileTime \***</span><span class="sxs-lookup"><span data-stu-id="19802-117">Type: **FILETIME\***</span></span>

<span data-ttu-id="19802-118">Heure de la dernière modification du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="19802-118">The time of the last font file modification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19802-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19802-119">Return value</span></span>

<span data-ttu-id="19802-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="19802-120">Type: **HRESULT**</span></span>

<span data-ttu-id="19802-121">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="19802-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19802-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19802-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19802-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19802-123">Requirements</span></span>



| <span data-ttu-id="19802-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19802-124">Requirement</span></span> | <span data-ttu-id="19802-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="19802-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19802-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19802-126">Library</span></span><br/> | <dl> <span data-ttu-id="19802-127"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19802-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="19802-128">DLL</span><span class="sxs-lookup"><span data-stu-id="19802-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="19802-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19802-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19802-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19802-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19802-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="19802-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





