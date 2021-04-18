---
description: La méthode SetBufferSamples spécifie s’il faut copier les exemples de données dans une mémoire tampon à mesure qu’elle passe par le filtre.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'ISampleGrabber :: SetBufferSamples, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528916"
---
# <a name="isamplegrabbersetbuffersamples-method"></a><span data-ttu-id="70fda-103">ISampleGrabber :: SetBufferSamples, méthode</span><span class="sxs-lookup"><span data-stu-id="70fda-103">ISampleGrabber::SetBufferSamples method</span></span>

> [!Note]  
> <span data-ttu-id="70fda-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="70fda-104">\[Deprecated.</span></span> <span data-ttu-id="70fda-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70fda-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="70fda-106">La méthode **SetBufferSamples** spécifie s’il faut copier les exemples de données dans une mémoire tampon à mesure qu’elle passe par le filtre.</span><span class="sxs-lookup"><span data-stu-id="70fda-106">The **SetBufferSamples** method specifies whether to copy sample data into a buffer as it goes through the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="70fda-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70fda-107">Syntax</span></span>


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a><span data-ttu-id="70fda-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70fda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70fda-109">*BufferThem*</span><span class="sxs-lookup"><span data-stu-id="70fda-109">*BufferThem*</span></span> 
</dt> <dd>

<span data-ttu-id="70fda-110">Valeur booléenne spécifiant si les exemples de données doivent être mis en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="70fda-110">Boolean value specifying whether to buffer sample data.</span></span> <span data-ttu-id="70fda-111">Si la **valeur est true**, le filtre copie les exemples de données dans une mémoire tampon interne.</span><span class="sxs-lookup"><span data-stu-id="70fda-111">If **TRUE**, the filter copies sample data into an internal buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70fda-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70fda-112">Return value</span></span>

<span data-ttu-id="70fda-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="70fda-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70fda-114">Notes</span><span class="sxs-lookup"><span data-stu-id="70fda-114">Remarks</span></span>

<span data-ttu-id="70fda-115">Pour récupérer la mémoire tampon copiée, appelez [**ISampleGrabber :: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="70fda-115">To get the copied buffer, call [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="70fda-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="70fda-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="70fda-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="70fda-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="70fda-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="70fda-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70fda-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70fda-119">Requirements</span></span>



| <span data-ttu-id="70fda-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70fda-120">Requirement</span></span> | <span data-ttu-id="70fda-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="70fda-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70fda-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="70fda-122">Header</span></span><br/>  | <dl> <span data-ttu-id="70fda-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="70fda-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="70fda-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="70fda-124">Library</span></span><br/> | <dl> <span data-ttu-id="70fda-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70fda-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70fda-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70fda-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70fda-127">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="70fda-127">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="70fda-128">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="70fda-128">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




