---
description: La \_ méthode obtenir la luminance récupère la valeur de luminance sur laquelle la clé doit être ajoutée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ luminance.
ms.assetid: 92113331-a7b7-4618-81b2-ea02e7bcc923
title: 'IDxtKey :: get_Luminance, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85dcba3720e007d0f3de890c085b0b223e3df350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542311"
---
# <a name="idxtkeyget_luminance-method"></a><span data-ttu-id="0afdb-104">IDxtKey :: obtient la \_ méthode de luminance</span><span class="sxs-lookup"><span data-stu-id="0afdb-104">IDxtKey::get\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="0afdb-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0afdb-105">\[Deprecated.</span></span> <span data-ttu-id="0afdb-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0afdb-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0afdb-107">La `get_Luminance` méthode récupère la valeur de luminance sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="0afdb-107">The `get_Luminance` method retrieves the luminance value on which to key.</span></span> <span data-ttu-id="0afdb-108">Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ luminance.</span><span class="sxs-lookup"><span data-stu-id="0afdb-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="0afdb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0afdb-109">Syntax</span></span>


```C++
HRESULT get_Luminance(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0afdb-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0afdb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0afdb-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0afdb-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0afdb-112">Reçoit la valeur de luminance sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="0afdb-112">Receives the luminance value on which to key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0afdb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0afdb-113">Return value</span></span>

<span data-ttu-id="0afdb-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0afdb-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0afdb-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0afdb-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0afdb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0afdb-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0afdb-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0afdb-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0afdb-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0afdb-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0afdb-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0afdb-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0afdb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0afdb-120">Requirements</span></span>



| <span data-ttu-id="0afdb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0afdb-121">Requirement</span></span> | <span data-ttu-id="0afdb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0afdb-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0afdb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0afdb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0afdb-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0afdb-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0afdb-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0afdb-125">Library</span></span><br/> | <dl> <span data-ttu-id="0afdb-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0afdb-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0afdb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0afdb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0afdb-128">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="0afdb-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="0afdb-129">**IDxtKey :: obtient \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="0afdb-129">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




