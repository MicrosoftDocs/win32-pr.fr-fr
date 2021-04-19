---
description: La méthode obtenir un nom \_ de fichier récupère le nom du fichier source actuellement utilisé par le détecteur de média.
ms.assetid: 68f0f1ea-74a2-4b65-9f1d-8699326d9d04
title: 'IMediaDet :: get_Filename, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95a350dde3dfdc1c6046c8e31b8a2d9e62684788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533391"
---
# <a name="imediadetget_filename-method"></a><span data-ttu-id="aea3e-103">IMediaDet :: obten, \_ méthode de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="aea3e-103">IMediaDet::get\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="aea3e-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="aea3e-104">\[Deprecated.</span></span> <span data-ttu-id="aea3e-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aea3e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aea3e-106">La `get_Filename` méthode récupère le nom du fichier source actuellement utilisé par le détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="aea3e-106">The `get_Filename` method retrieves the name of the source file currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea3e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aea3e-107">Syntax</span></span>


```C++
HRESULT get_Filename(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="aea3e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aea3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aea3e-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="aea3e-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="aea3e-110">Reçoit le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="aea3e-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aea3e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aea3e-111">Return value</span></span>

<span data-ttu-id="aea3e-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aea3e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aea3e-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aea3e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aea3e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="aea3e-114">Remarks</span></span>

<span data-ttu-id="aea3e-115">La méthode alloue de la mémoire pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="aea3e-115">The method allocates memory for the string.</span></span> <span data-ttu-id="aea3e-116">L’application doit appeler **SysFreeString** pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="aea3e-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="aea3e-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="aea3e-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aea3e-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aea3e-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aea3e-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="aea3e-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aea3e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aea3e-120">Requirements</span></span>



| <span data-ttu-id="aea3e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aea3e-121">Requirement</span></span> | <span data-ttu-id="aea3e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="aea3e-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aea3e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="aea3e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="aea3e-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="aea3e-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aea3e-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aea3e-125">Library</span></span><br/> | <dl> <span data-ttu-id="aea3e-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aea3e-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea3e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aea3e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea3e-128">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="aea3e-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="aea3e-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="aea3e-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




