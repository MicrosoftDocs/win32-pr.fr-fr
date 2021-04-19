---
description: La méthode obtenir la \_ similarité récupère la plage de données de couleur qui devient transparente. À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB ou DXTKEY \_ NONRED.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'IDxtKey :: get_Similarity, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530478"
---
# <a name="idxtkeyget_similarity-method"></a><span data-ttu-id="a3f46-105">IDxtKey :: obtient \_ la méthode de similarité</span><span class="sxs-lookup"><span data-stu-id="a3f46-105">IDxtKey::get\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="a3f46-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a3f46-106">\[Deprecated.</span></span> <span data-ttu-id="a3f46-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a3f46-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a3f46-108">La `get_Similarity` méthode récupère la plage de données de couleur qui devient transparente.</span><span class="sxs-lookup"><span data-stu-id="a3f46-108">The `get_Similarity` method retrieves the range of color data that becomes transparent.</span></span> <span data-ttu-id="a3f46-109">À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente.</span><span class="sxs-lookup"><span data-stu-id="a3f46-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="a3f46-110">Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB ou DXTKEY \_ NONRED.</span><span class="sxs-lookup"><span data-stu-id="a3f46-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f46-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3f46-111">Syntax</span></span>


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a3f46-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3f46-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f46-113">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a3f46-113">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f46-114">Reçoit la valeur de similarité.</span><span class="sxs-lookup"><span data-stu-id="a3f46-114">Receives the similarity value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f46-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3f46-115">Return value</span></span>

<span data-ttu-id="a3f46-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a3f46-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3f46-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3f46-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f46-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a3f46-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a3f46-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="a3f46-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a3f46-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a3f46-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a3f46-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a3f46-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a3f46-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3f46-122">Requirements</span></span>



| <span data-ttu-id="a3f46-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3f46-123">Requirement</span></span> | <span data-ttu-id="a3f46-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3f46-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f46-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3f46-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a3f46-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f46-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a3f46-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a3f46-127">Library</span></span><br/> | <dl> <span data-ttu-id="a3f46-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3f46-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f46-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3f46-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f46-130">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="a3f46-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="a3f46-131">**IDxtKey :: obtient \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="a3f46-131">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




