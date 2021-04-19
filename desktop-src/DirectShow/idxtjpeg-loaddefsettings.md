---
description: La méthode LoadDefSettings restaure les paramètres par défaut de la transition de réinitialisation.
ms.assetid: 3f81002a-ecac-4d5a-8d2a-ada4d4884d7d
title: 'IDxtJpeg :: LoadDefSettings, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.LoadDefSettings
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51438a21782d1a703a3b43134517e8337ce9f75e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538136"
---
# <a name="idxtjpegloaddefsettings-method"></a><span data-ttu-id="18ff6-103">IDxtJpeg :: LoadDefSettings, méthode</span><span class="sxs-lookup"><span data-stu-id="18ff6-103">IDxtJpeg::LoadDefSettings method</span></span>

> [!Note]  
> <span data-ttu-id="18ff6-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="18ff6-104">\[Deprecated.</span></span> <span data-ttu-id="18ff6-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="18ff6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="18ff6-106">La `LoadDefSettings` méthode restaure les paramètres par défaut de la transition de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="18ff6-106">The `LoadDefSettings` method restores the default settings of the Wipe transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ff6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18ff6-107">Syntax</span></span>


```C++
HRESULT LoadDefSettings();
```



## <a name="parameters"></a><span data-ttu-id="18ff6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18ff6-108">Parameters</span></span>

<span data-ttu-id="18ff6-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="18ff6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18ff6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18ff6-110">Return value</span></span>

<span data-ttu-id="18ff6-111">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff6-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18ff6-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18ff6-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ff6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="18ff6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="18ff6-114">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="18ff6-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="18ff6-115">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="18ff6-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="18ff6-116">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="18ff6-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18ff6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18ff6-117">Requirements</span></span>



| <span data-ttu-id="18ff6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18ff6-118">Requirement</span></span> | <span data-ttu-id="18ff6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="18ff6-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18ff6-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="18ff6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="18ff6-121"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ff6-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="18ff6-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="18ff6-122">Library</span></span><br/> | <dl> <span data-ttu-id="18ff6-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18ff6-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ff6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18ff6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ff6-125">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="18ff6-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




