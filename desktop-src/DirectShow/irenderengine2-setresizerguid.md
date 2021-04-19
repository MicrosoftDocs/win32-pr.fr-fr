---
description: La méthode SetResizerGUID spécifie le CLSID d’un filtre de redimensionnement vidéo personnalisé.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'IRenderEngine2 :: SetResizerGUID, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530004"
---
# <a name="irenderengine2setresizerguid-method"></a><span data-ttu-id="472bd-103">IRenderEngine2 :: SetResizerGUID, méthode</span><span class="sxs-lookup"><span data-stu-id="472bd-103">IRenderEngine2::SetResizerGUID method</span></span>

> [!Note]  
> <span data-ttu-id="472bd-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="472bd-104">\[Deprecated.</span></span> <span data-ttu-id="472bd-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="472bd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="472bd-106">La `SetResizerGUID` méthode spécifie le CLSID d’un filtre de redimensionnement vidéo personnalisé.</span><span class="sxs-lookup"><span data-stu-id="472bd-106">The `SetResizerGUID` method specifies the CLSID of a custom video resizing filter.</span></span> <span data-ttu-id="472bd-107">Appelez cette méthode pour remplacer le filtre de redimensionnement par défaut utilisé par les services d’édition DirectShow.</span><span class="sxs-lookup"><span data-stu-id="472bd-107">Call this method to replace the default resizing filter used by DirectShow Editing Services.</span></span> <span data-ttu-id="472bd-108">Votre filtre doit être inscrit en tant qu’objet COM sur le système de l’utilisateur et doit prendre en charge l’interface [**IResize**](iresize.md) .</span><span class="sxs-lookup"><span data-stu-id="472bd-108">Your filter must be registered as a COM object on the user's system, and it must support the [**IResize**](iresize.md) interface.</span></span>

<span data-ttu-id="472bd-109">Appelez cette méthode avant d’appeler [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="472bd-109">Call this method before calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="472bd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="472bd-110">Syntax</span></span>


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a><span data-ttu-id="472bd-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="472bd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="472bd-112">*ResizerGuid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="472bd-112">*ResizerGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="472bd-113">CLSID du filtre.</span><span class="sxs-lookup"><span data-stu-id="472bd-113">The CLSID of the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="472bd-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="472bd-114">Return value</span></span>

<span data-ttu-id="472bd-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="472bd-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="472bd-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="472bd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="472bd-117">Notes</span><span class="sxs-lookup"><span data-stu-id="472bd-117">Remarks</span></span>

<span data-ttu-id="472bd-118">Pour rétablir la valeur par défaut DES redimensionnements, utilisez le CLSID suivant :</span><span class="sxs-lookup"><span data-stu-id="472bd-118">To revert to the default DES resizer, use the following CLSID:</span></span>


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> <span data-ttu-id="472bd-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="472bd-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="472bd-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="472bd-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="472bd-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="472bd-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="472bd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="472bd-122">Requirements</span></span>



| <span data-ttu-id="472bd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="472bd-123">Requirement</span></span> | <span data-ttu-id="472bd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="472bd-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="472bd-125">Version</span><span class="sxs-lookup"><span data-stu-id="472bd-125">Version</span></span><br/> | <span data-ttu-id="472bd-126">DirectX 9,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="472bd-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="472bd-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="472bd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="472bd-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="472bd-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="472bd-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="472bd-129">Library</span></span><br/> | <dl> <span data-ttu-id="472bd-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="472bd-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="472bd-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="472bd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472bd-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="472bd-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="472bd-133">**Interface IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="472bd-133">**IRenderEngine2 Interface**</span></span>](irenderengine2.md)
</dt> </dl>

 

 




