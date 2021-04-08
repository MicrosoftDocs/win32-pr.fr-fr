---
title: WM/ContainerFormat
description: L’attribut WM/ContainerFormat spécifie le type de fichier chargé dans l’objet appelant.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Format Windows Media WM/ContainerFormat
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678594"
---
# <a name="wmcontainerformat"></a><span data-ttu-id="804ea-104">WM/ContainerFormat</span><span class="sxs-lookup"><span data-stu-id="804ea-104">WM/ContainerFormat</span></span>

<span data-ttu-id="804ea-105">L’attribut **WM/ContainerFormat** spécifie le type de fichier chargé dans l’objet appelant.</span><span class="sxs-lookup"><span data-stu-id="804ea-105">The **WM/ContainerFormat** attribute specifies the type of file that is loaded in the calling object.</span></span>

## <a name="global-constant"></a><span data-ttu-id="804ea-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="804ea-106">Global Constant</span></span>

<span data-ttu-id="804ea-107">\_wszWMContainerFormat g</span><span class="sxs-lookup"><span data-stu-id="804ea-107">g\_wszWMContainerFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="804ea-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="804ea-108">Data Type</span></span>

<span data-ttu-id="804ea-109">[**WMT \_ \_format de stockage**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (type de stockage **WMT \_ \_ binaire**)</span><span class="sxs-lookup"><span data-stu-id="804ea-109">[**WMT\_STORAGE\_FORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="804ea-110">Notes</span><span class="sxs-lookup"><span data-stu-id="804ea-110">Remarks</span></span>

<span data-ttu-id="804ea-111">Cet attribut est utilisé à la place de **IWMProfile3 :: GetStorageFormat** et **IWMProfile3 :: SetStorageFormat**, qui ne sont plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="804ea-111">This attribute is used in place of **IWMProfile3::GetStorageFormat** and **IWMProfile3::SetStorageFormat**, which are no longer supported.</span></span>

<span data-ttu-id="804ea-112">Il s’agit d’un attribut codé.</span><span class="sxs-lookup"><span data-stu-id="804ea-112">This is a coded attribute.</span></span>

<span data-ttu-id="804ea-113">Cet attribut ne peut pas être dupliqué au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="804ea-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="804ea-114">Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="804ea-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="804ea-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="804ea-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804ea-116">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="804ea-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




