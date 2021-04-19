---
description: La \_ méthode obtenir MaskName récupère le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'IDxtJpeg :: get_MaskName, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535900"
---
# <a name="idxtjpegget_maskname-method"></a><span data-ttu-id="e00ef-103">IDxtJpeg :: \_ MaskName, méthode</span><span class="sxs-lookup"><span data-stu-id="e00ef-103">IDxtJpeg::get\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="e00ef-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e00ef-104">\[Deprecated.</span></span> <span data-ttu-id="e00ef-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e00ef-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e00ef-106">La `get_MaskName` méthode récupère le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="e00ef-106">The `get_MaskName` method retrieves the name of a JPEG file to be used as the wipe mask.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00ef-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e00ef-107">Syntax</span></span>


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e00ef-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e00ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00ef-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e00ef-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e00ef-110">Reçoit le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="e00ef-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00ef-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e00ef-111">Return value</span></span>

<span data-ttu-id="e00ef-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e00ef-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e00ef-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e00ef-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e00ef-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e00ef-114">Remarks</span></span>

<span data-ttu-id="e00ef-115">Si la transition de réinitialisation utilise l’une des réinitialisations SMPTE intégrées qu’elle prend en charge, la valeur de cette propriété est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="e00ef-115">If the wipe transition is using one of the built-in SMPTE wipes that it supports, the value of this property is an empty string.</span></span>

<span data-ttu-id="e00ef-116">L’appelant doit libérer la chaîne retournée à l’aide de la fonction **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="e00ef-116">The caller must release the returned string, using the **SysFreeString** function.</span></span>

> [!Note]  
> <span data-ttu-id="e00ef-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e00ef-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e00ef-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e00ef-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e00ef-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e00ef-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e00ef-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e00ef-120">Requirements</span></span>



| <span data-ttu-id="e00ef-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e00ef-121">Requirement</span></span> | <span data-ttu-id="e00ef-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e00ef-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e00ef-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e00ef-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e00ef-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e00ef-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e00ef-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e00ef-125">Library</span></span><br/> | <dl> <span data-ttu-id="e00ef-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e00ef-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00ef-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e00ef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00ef-128">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="e00ef-128">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="e00ef-129">**IDxtJpeg :: obtient \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="e00ef-129">**IDxtJpeg::get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




