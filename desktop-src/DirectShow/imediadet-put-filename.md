---
description: La \_ méthode put filename spécifie le nom du fichier source pour le détecteur de média à utiliser.
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: IMediaDet ::p ut_Filename, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 542b84d3a1eec79b8408c7642bc08680fdc036ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544088"
---
# <a name="imediadetput_filename-method"></a><span data-ttu-id="00837-103">IMediaDet ::p ut \_ FileName, méthode</span><span class="sxs-lookup"><span data-stu-id="00837-103">IMediaDet::put\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="00837-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="00837-104">\[Deprecated.</span></span> <span data-ttu-id="00837-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="00837-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="00837-106">La `put_Filename` méthode spécifie le nom du fichier source pour le détecteur de média à utiliser.</span><span class="sxs-lookup"><span data-stu-id="00837-106">The `put_Filename` method specifies the name of the source file for the media detector to use.</span></span>

<span data-ttu-id="00837-107">N’appelez pas cette méthode deux fois sur le même objet MediaDet.</span><span class="sxs-lookup"><span data-stu-id="00837-107">Do not call this method twice on the same MediaDet object.</span></span> <span data-ttu-id="00837-108">Pour utiliser cette interface avec plusieurs fichiers sources, créez des instances distinctes de l’objet MediaDet.</span><span class="sxs-lookup"><span data-stu-id="00837-108">To use this interface with more than one source file, create separate instances of the MediaDet object.</span></span>

## <a name="syntax"></a><span data-ttu-id="00837-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00837-109">Syntax</span></span>


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="00837-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00837-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00837-111">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00837-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00837-112">Nom de fichier de la source.</span><span class="sxs-lookup"><span data-stu-id="00837-112">File name of the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00837-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00837-113">Return value</span></span>

<span data-ttu-id="00837-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="00837-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00837-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="00837-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00837-116">Notes</span><span class="sxs-lookup"><span data-stu-id="00837-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="00837-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="00837-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="00837-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="00837-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="00837-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="00837-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00837-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00837-120">Requirements</span></span>



| <span data-ttu-id="00837-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00837-121">Requirement</span></span> | <span data-ttu-id="00837-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="00837-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00837-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="00837-123">Header</span></span><br/>  | <dl> <span data-ttu-id="00837-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="00837-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="00837-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="00837-125">Library</span></span><br/> | <dl> <span data-ttu-id="00837-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00837-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00837-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00837-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00837-128">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="00837-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="00837-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="00837-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




