---
description: La méthode SetMediaName spécifie le nom du fichier source représenté par cet objet source.
ms.assetid: 60307c87-9dce-4e60-b14b-07d2c8604dd8
title: 'IAMTimelineSrc :: SetMediaName, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a770c697f72c8776e9ec7070272ab09fc0dd6af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531107"
---
# <a name="iamtimelinesrcsetmedianame-method"></a><span data-ttu-id="50cb2-103">IAMTimelineSrc :: SetMediaName, méthode</span><span class="sxs-lookup"><span data-stu-id="50cb2-103">IAMTimelineSrc::SetMediaName method</span></span>

> [!Note]  
> <span data-ttu-id="50cb2-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="50cb2-104">\[Deprecated.</span></span> <span data-ttu-id="50cb2-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="50cb2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="50cb2-106">La `SetMediaName` méthode spécifie le nom du fichier source représenté par cet objet source.</span><span class="sxs-lookup"><span data-stu-id="50cb2-106">The `SetMediaName` method specifies the name of the source file represented by this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="50cb2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50cb2-107">Syntax</span></span>


```C++
HRESULT SetMediaName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="50cb2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50cb2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50cb2-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="50cb2-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="50cb2-110">Chaîne qui spécifie le nom du fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="50cb2-110">String that specifies the name of the media file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50cb2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50cb2-111">Return value</span></span>

<span data-ttu-id="50cb2-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="50cb2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50cb2-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="50cb2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="50cb2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="50cb2-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="50cb2-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="50cb2-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="50cb2-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="50cb2-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="50cb2-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="50cb2-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="50cb2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50cb2-118">Requirements</span></span>



| <span data-ttu-id="50cb2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50cb2-119">Requirement</span></span> | <span data-ttu-id="50cb2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="50cb2-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50cb2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="50cb2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="50cb2-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="50cb2-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="50cb2-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50cb2-123">Library</span></span><br/> | <dl> <span data-ttu-id="50cb2-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50cb2-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50cb2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50cb2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50cb2-126">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="50cb2-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="50cb2-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="50cb2-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




