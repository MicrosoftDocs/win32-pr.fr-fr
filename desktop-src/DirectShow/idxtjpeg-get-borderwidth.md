---
description: La \_ méthode obtenir BorderWidth récupère la largeur de la bordure unie le long des bords du motif de réinitialisation.
ms.assetid: 85c62524-5936-475e-a73b-7a3c926bb5f0
title: 'IDxtJpeg :: get_BorderWidth, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28405c08d5666c8f182e0ffdb6ed1aa7bac599d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521644"
---
# <a name="idxtjpegget_borderwidth-method"></a><span data-ttu-id="dc238-103">IDxtJpeg :: obtient la \_ méthode BorderWidth</span><span class="sxs-lookup"><span data-stu-id="dc238-103">IDxtJpeg::get\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="dc238-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dc238-104">\[Deprecated.</span></span> <span data-ttu-id="dc238-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc238-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dc238-106">La `get_BorderWidth` méthode récupère la largeur de la bordure unie le long des bords du motif de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="dc238-106">The `get_BorderWidth` method retrieves the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc238-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc238-107">Syntax</span></span>


```C++
HRESULT get_BorderWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="dc238-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc238-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc238-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="dc238-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dc238-110">Reçoit la largeur de la bordure, en pixels.</span><span class="sxs-lookup"><span data-stu-id="dc238-110">Receives the width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc238-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc238-111">Return value</span></span>

<span data-ttu-id="dc238-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dc238-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc238-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dc238-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc238-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dc238-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dc238-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="dc238-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dc238-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dc238-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dc238-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dc238-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dc238-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc238-118">Requirements</span></span>



| <span data-ttu-id="dc238-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc238-119">Requirement</span></span> | <span data-ttu-id="dc238-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc238-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc238-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc238-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dc238-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc238-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dc238-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dc238-123">Library</span></span><br/> | <dl> <span data-ttu-id="dc238-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc238-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc238-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc238-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc238-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="dc238-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




