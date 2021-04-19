---
title: Méthode IDWriteLocalFontFileLoader GetFilePathFromKey
description: Obtient le chemin d’accès absolu au fichier de polices à partir de la clé de référence du fichier de police.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Écriture directe de la méthode GetFilePathFromKey
- Méthode GetFilePathFromKey Write directe, interface IDWriteLocalFontFileLoader
- Écriture directe de l’interface IDWriteLocalFontFileLoader, méthode GetFilePathFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536033"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a><span data-ttu-id="ca91c-106">IDWriteLocalFontFileLoader :: GetFilePathFromKey, méthode</span><span class="sxs-lookup"><span data-stu-id="ca91c-106">IDWriteLocalFontFileLoader::GetFilePathFromKey method</span></span>

<span data-ttu-id="ca91c-107">Obtient le chemin d’accès absolu au fichier de polices à partir de la clé de référence du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="ca91c-107">Obtains the absolute font file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca91c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca91c-108">Syntax</span></span>


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="ca91c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca91c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca91c-110">*fontFileReferenceKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca91c-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca91c-111">Type : **const void \***</span><span class="sxs-lookup"><span data-stu-id="ca91c-111">Type: **const void\***</span></span>

<span data-ttu-id="ca91c-112">Clé de référence du fichier de police qui identifie de façon unique le fichier de police local dans l’étendue du chargeur de polices utilisé.</span><span class="sxs-lookup"><span data-stu-id="ca91c-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="ca91c-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="ca91c-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="ca91c-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca91c-114">Type: **UINT32**</span></span>

<span data-ttu-id="ca91c-115">Taille de la clé de référence du fichier de police, en octets.</span><span class="sxs-lookup"><span data-stu-id="ca91c-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ca91c-116">*filePath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ca91c-116">*filePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca91c-117">Type : **WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="ca91c-117">Type: **WCHAR\***</span></span>

<span data-ttu-id="ca91c-118">Tableau de caractères qui reçoit le chemin d’accès au fichier local.</span><span class="sxs-lookup"><span data-stu-id="ca91c-118">The character array that receives the local file path.</span></span>

</dd> <dt>

<span data-ttu-id="ca91c-119">*filePathSize*</span><span class="sxs-lookup"><span data-stu-id="ca91c-119">*filePathSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ca91c-120">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca91c-120">Type: **UINT32**</span></span>

<span data-ttu-id="ca91c-121">Longueur du tableau de caractères de chemin d’accès de fichier.</span><span class="sxs-lookup"><span data-stu-id="ca91c-121">The length of the file path character array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca91c-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca91c-122">Return value</span></span>

<span data-ttu-id="ca91c-123">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ca91c-123">Type: **HRESULT**</span></span>

<span data-ttu-id="ca91c-124">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ca91c-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ca91c-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca91c-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca91c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca91c-126">Requirements</span></span>



| <span data-ttu-id="ca91c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca91c-127">Requirement</span></span> | <span data-ttu-id="ca91c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca91c-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca91c-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ca91c-129">Library</span></span><br/> | <dl> <span data-ttu-id="ca91c-130"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca91c-130"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="ca91c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ca91c-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="ca91c-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca91c-132"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca91c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca91c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca91c-134">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="ca91c-134">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





