---
title: Méthode IDWriteFactory2 GetSystemFontFallback
description: Crée un objet de police de secours à partir de la liste des polices système de secours.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Écriture directe de la méthode GetSystemFontFallback
- Méthode GetSystemFontFallback Write directe, interface IDWriteFactory2
- Écriture directe de l’interface IDWriteFactory2, méthode GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382403"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a><span data-ttu-id="ea332-106">IDWriteFactory2 :: GetSystemFontFallback, méthode</span><span class="sxs-lookup"><span data-stu-id="ea332-106">IDWriteFactory2::GetSystemFontFallback method</span></span>

<span data-ttu-id="ea332-107">Crée un objet de police de secours à partir de la liste des polices système de secours.</span><span class="sxs-lookup"><span data-stu-id="ea332-107">Creates a font fallback object from the system font fallback list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea332-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea332-108">Syntax</span></span>


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a><span data-ttu-id="ea332-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea332-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea332-110">*fontFallback* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ea332-110">*fontFallback* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea332-111">Type : **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span><span class="sxs-lookup"><span data-stu-id="ea332-111">Type: **[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span></span>

<span data-ttu-id="ea332-112">Contient une adresse d’un pointeur vers l’objet de police de secours nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="ea332-112">Contains an address of a pointer to the newly created font fallback object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea332-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea332-113">Return value</span></span>

<span data-ttu-id="ea332-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ea332-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ea332-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ea332-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ea332-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea332-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea332-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea332-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea332-118">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="ea332-118">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

 