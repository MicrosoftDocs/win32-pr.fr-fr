---
description: La \_ méthode put similarité spécifie la plage de données de couleur qui devient transparente. À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB ou DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: IDxtKey ::p ut_Similarity, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533123"
---
# <a name="idxtkeyput_similarity-method"></a><span data-ttu-id="a40ca-105">IDxtKey ::p \_ méthode de similarité de la ut</span><span class="sxs-lookup"><span data-stu-id="a40ca-105">IDxtKey::put\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="a40ca-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a40ca-106">\[Deprecated.</span></span> <span data-ttu-id="a40ca-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a40ca-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a40ca-108">La `put_Similarity` méthode spécifie la plage de données de couleur qui devient transparente.</span><span class="sxs-lookup"><span data-stu-id="a40ca-108">The `put_Similarity` method specifies the range of color data that becomes transparent.</span></span> <span data-ttu-id="a40ca-109">À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente.</span><span class="sxs-lookup"><span data-stu-id="a40ca-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="a40ca-110">Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB ou DXTKEY \_ NONRED.</span><span class="sxs-lookup"><span data-stu-id="a40ca-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="a40ca-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a40ca-111">Syntax</span></span>


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="a40ca-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a40ca-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a40ca-113">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a40ca-113">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a40ca-114">Spécifie la valeur de similarité.</span><span class="sxs-lookup"><span data-stu-id="a40ca-114">Specifies the similarity value.</span></span> <span data-ttu-id="a40ca-115">La plage valide est comprise entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="a40ca-115">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a40ca-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a40ca-116">Return value</span></span>

<span data-ttu-id="a40ca-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a40ca-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a40ca-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a40ca-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a40ca-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a40ca-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a40ca-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="a40ca-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a40ca-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a40ca-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a40ca-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a40ca-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a40ca-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a40ca-123">Requirements</span></span>



| <span data-ttu-id="a40ca-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a40ca-124">Requirement</span></span> | <span data-ttu-id="a40ca-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a40ca-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a40ca-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a40ca-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a40ca-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a40ca-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a40ca-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a40ca-128">Library</span></span><br/> | <dl> <span data-ttu-id="a40ca-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a40ca-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a40ca-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a40ca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a40ca-131">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="a40ca-131">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="a40ca-132">**IDxtKey ::p \_ type ut**</span><span class="sxs-lookup"><span data-stu-id="a40ca-132">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




