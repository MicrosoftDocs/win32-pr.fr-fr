---
description: La \_ méthode put CurrentStream spécifie le numéro de flux du détecteur de média à utiliser.
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: IMediaDet ::p ut_CurrentStream, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864848f646e4a9e06ca12e2bfec742c1741d77e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539658"
---
# <a name="imediadetput_currentstream-method"></a><span data-ttu-id="84587-103">IMediaDet ::p ut \_ CurrentStream, méthode</span><span class="sxs-lookup"><span data-stu-id="84587-103">IMediaDet::put\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="84587-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="84587-104">\[Deprecated.</span></span> <span data-ttu-id="84587-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="84587-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="84587-106">La `put_CurrentStream` méthode spécifie le numéro de flux du détecteur de média à utiliser.</span><span class="sxs-lookup"><span data-stu-id="84587-106">The `put_CurrentStream` method specifies the stream number for the media detector to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="84587-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84587-107">Syntax</span></span>


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="84587-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84587-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84587-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84587-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84587-110">Numéro de flux.</span><span class="sxs-lookup"><span data-stu-id="84587-110">Stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84587-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84587-111">Return value</span></span>

<span data-ttu-id="84587-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="84587-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="84587-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="84587-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="84587-114">Notes</span><span class="sxs-lookup"><span data-stu-id="84587-114">Remarks</span></span>

<span data-ttu-id="84587-115">Avant d’appeler cette méthode, appelez [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) pour définir le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="84587-115">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="84587-116">Appelez [**IMediaDet :: obtenir \_ OutputStreams**](imediadet-get-outputstreams.md) pour déterminer le nombre de flux contenus dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="84587-116">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to determine the number of streams contained in the source file.</span></span>

<span data-ttu-id="84587-117">Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="84587-117">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="84587-118">Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="84587-118">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="84587-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="84587-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="84587-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="84587-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="84587-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="84587-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="84587-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84587-122">Requirements</span></span>



| <span data-ttu-id="84587-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84587-123">Requirement</span></span> | <span data-ttu-id="84587-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="84587-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84587-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="84587-125">Header</span></span><br/>  | <dl> <span data-ttu-id="84587-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="84587-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="84587-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="84587-127">Library</span></span><br/> | <dl> <span data-ttu-id="84587-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84587-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84587-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84587-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84587-130">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="84587-130">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="84587-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="84587-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




