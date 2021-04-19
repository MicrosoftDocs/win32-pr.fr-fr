---
title: HasAttachedImages
description: L’attribut HasAttachedImages est un attribut de niveau fichier qui spécifie si le fichier est un fichier MP3 avec des frames ID3 APIC attachés.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Format Windows Media HasAttachedImages
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509835"
---
# <a name="hasattachedimages"></a><span data-ttu-id="ff893-104">HasAttachedImages</span><span class="sxs-lookup"><span data-stu-id="ff893-104">HasAttachedImages</span></span>

<span data-ttu-id="ff893-105">L’attribut **HasAttachedImages** est un attribut de niveau fichier qui spécifie si le fichier est un fichier mp3 avec des frames ID3 APIC attachés.</span><span class="sxs-lookup"><span data-stu-id="ff893-105">The **HasAttachedImages** attribute is a file-level attribute specifying whether the file is an MP3 file with attached APIC ID3 frames.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ff893-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="ff893-106">Global Constant</span></span>

<span data-ttu-id="ff893-107">\_wszWMHasAttachedImages g</span><span class="sxs-lookup"><span data-stu-id="ff893-107">g\_wszWMHasAttachedImages</span></span>

## <a name="data-type"></a><span data-ttu-id="ff893-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="ff893-108">Data Type</span></span>

<span data-ttu-id="ff893-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ff893-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="ff893-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ff893-110">Remarks</span></span>

<span data-ttu-id="ff893-111">Il s’agit d’un attribut codé.</span><span class="sxs-lookup"><span data-stu-id="ff893-111">This is a coded attribute.</span></span>

<span data-ttu-id="ff893-112">Cet attribut ne peut pas être dupliqué au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="ff893-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="ff893-113">Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ff893-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="ff893-114">**HasAttachedImages** a été conçu pour informer une application que des images étaient présentes afin qu’elles puissent être récupérées à l’aide de l’interface [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) .</span><span class="sxs-lookup"><span data-stu-id="ff893-114">**HasAttachedImages** was designed to inform an application that images were present so that they could be retrieved using the [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) interface.</span></span> <span data-ttu-id="ff893-115">Maintenant que les images sont prises en charge à l’aide de l’attribut [**WM/Picture**](wmpicture.md) , **HasAttachedImages** n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ff893-115">Now that images are supported using the [**WM/Picture**](wmpicture.md) attribute, **HasAttachedImages** is no longer needed.</span></span>

<span data-ttu-id="ff893-116">Pour déterminer si un fichier contient des images, appelez [**IWMHeaderInfo3 :: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) en spécifiant l’attribut **WM/Picture** .</span><span class="sxs-lookup"><span data-stu-id="ff893-116">To determine whether a file contains images, call [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specifying the **WM/Picture** attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff893-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff893-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff893-118">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="ff893-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




