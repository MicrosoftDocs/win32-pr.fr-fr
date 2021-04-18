---
title: Méthode IDWriteLocalFontFileLoader GetFilePathLengthFromKey
description: Obtient la longueur du chemin d’accès absolu du fichier à partir de la clé de référence du fichier de police.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Écriture directe de la méthode GetFilePathLengthFromKey
- Méthode GetFilePathLengthFromKey Write directe, interface IDWriteLocalFontFileLoader
- Écriture directe de l’interface IDWriteLocalFontFileLoader, méthode GetFilePathLengthFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526767"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a><span data-ttu-id="68a57-106">IDWriteLocalFontFileLoader :: GetFilePathLengthFromKey, méthode</span><span class="sxs-lookup"><span data-stu-id="68a57-106">IDWriteLocalFontFileLoader::GetFilePathLengthFromKey method</span></span>

<span data-ttu-id="68a57-107">Obtient la longueur du chemin d’accès absolu du fichier à partir de la clé de référence du fichier de police.</span><span class="sxs-lookup"><span data-stu-id="68a57-107">Obtains the length of the absolute file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a57-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68a57-108">Syntax</span></span>


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a><span data-ttu-id="68a57-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68a57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68a57-110">*fontFileReferenceKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68a57-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68a57-111">Type : **const void \***</span><span class="sxs-lookup"><span data-stu-id="68a57-111">Type: **const void\***</span></span>

<span data-ttu-id="68a57-112">Clé de référence du fichier de police qui identifie de façon unique le fichier de police local dans l’étendue du chargeur de polices utilisé.</span><span class="sxs-lookup"><span data-stu-id="68a57-112">Font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="68a57-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="68a57-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="68a57-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68a57-114">Type: **UINT32**</span></span>

<span data-ttu-id="68a57-115">Taille de la clé de référence du fichier de police en octets.</span><span class="sxs-lookup"><span data-stu-id="68a57-115">Size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="68a57-116">*filePathLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="68a57-116">*filePathLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68a57-117">Type : **UInt32 \***</span><span class="sxs-lookup"><span data-stu-id="68a57-117">Type: **UINT32\***</span></span>

<span data-ttu-id="68a57-118">Longueur de la chaîne du chemin d’accès du fichier, sans inclure le caractère **null** terminé.</span><span class="sxs-lookup"><span data-stu-id="68a57-118">Length of the file path string, not including the terminated **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68a57-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68a57-119">Return value</span></span>

<span data-ttu-id="68a57-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="68a57-120">Type: **HRESULT**</span></span>

<span data-ttu-id="68a57-121">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="68a57-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68a57-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68a57-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68a57-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68a57-123">Requirements</span></span>



| <span data-ttu-id="68a57-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68a57-124">Requirement</span></span> | <span data-ttu-id="68a57-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="68a57-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68a57-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="68a57-126">Library</span></span><br/> | <dl> <span data-ttu-id="68a57-127"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68a57-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="68a57-128">DLL</span><span class="sxs-lookup"><span data-stu-id="68a57-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="68a57-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68a57-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a57-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68a57-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a57-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="68a57-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





