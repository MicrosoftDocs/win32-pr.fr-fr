---
description: Spécifie si l’application nécessite la prise en charge de Microsoft Direct3D dans le lecteur source ou le writer du récepteur.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: Attribut MF_READWRITE_D3D_OPTIONAL (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210487"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a><span data-ttu-id="37138-103">MF \_ ReadWrite de l' \_ \_ attribut facultatif D3D</span><span class="sxs-lookup"><span data-stu-id="37138-103">MF\_READWRITE\_D3D\_OPTIONAL attribute</span></span>

<span data-ttu-id="37138-104">Spécifie si l’application nécessite la prise en charge de Microsoft Direct3D dans le [lecteur source](source-reader.md) ou le [writer du récepteur](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="37138-104">Specifies whether the application requires Microsoft Direct3D support in the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="37138-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="37138-105">Data type</span></span>

<span data-ttu-id="37138-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37138-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="37138-107">Notes</span><span class="sxs-lookup"><span data-stu-id="37138-107">Remarks</span></span>

<span data-ttu-id="37138-108">Cet attribut s’applique uniquement si l’application active la prise en charge Direct3D à l’aide de l’attribut du gestionnaire [ \_ \_ D3D du lecteur \_ \_ source MF](mf-source-reader-d3d-manager.md) ou du gestionnaire D3D du [récepteur du \_ récepteur \_ \_ \_ MF](mf-sink-writer-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="37138-108">This attribute applies only if the application enables Direct3D support using the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) or [MF\_SINK\_WRITER\_D3D\_MANAGER](mf-sink-writer-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="37138-109">Si l’application active la prise en charge Direct3D, le lecteur source et le writer du récepteur essaient tous deux d’allouer des surfaces Direct3D pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="37138-109">If the application enables Direct3D support, the Source Reader and Sink Writer will both try to allocate Direct3D surfaces for video.</span></span> <span data-ttu-id="37138-110">Si cette opération échoue et que l' \_ \_ attribut facultatif MF ReadWrite D3D \_ est **true**, l’enregistreur de lecture/récepteur source revient à allouer des surfaces vidéo dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="37138-110">If this fails, and the MF\_READWRITE\_D3D\_OPTIONAL attribute is **TRUE**, the Source Reader/Sink Writer will fall back to allocating video surfaces in system memory.</span></span> <span data-ttu-id="37138-111">Sinon, si les surfaces Direct3D ne peuvent pas être allouées et que \_ \_ l’option MF ReadWrite D3D \_ facultative a la **valeur false**, une erreur se produit pendant le traitement.</span><span class="sxs-lookup"><span data-stu-id="37138-111">Otherwise, if Direct3D surfaces cannot be allocated and MF\_READWRITE\_D3D\_OPTIONAL is **FALSE**, an error occurs during processing.</span></span>

<span data-ttu-id="37138-112">Si l’application n’active pas la prise en charge Direct3D, le writer de lecteur/récepteur source utilise la mémoire système et ignore la valeur de l' \_ option MF ReadWrite \_ D3D \_ facultative.</span><span class="sxs-lookup"><span data-stu-id="37138-112">If the application does not enable Direct3D support, the Source Reader/Sink Writer uses system memory, and ignores the value of MF\_READWRITE\_D3D\_OPTIONAL.</span></span>

<span data-ttu-id="37138-113">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="37138-113">This attribute is optional.</span></span> <span data-ttu-id="37138-114">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="37138-114">The default value is **FALSE**.</span></span> <span data-ttu-id="37138-115">Définissez l’attribut lorsque vous créez le lecteur source ou le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="37138-115">Set the attribute when you create the Source Reader or Sink Writer.</span></span>

## <a name="requirements"></a><span data-ttu-id="37138-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37138-116">Requirements</span></span>



| <span data-ttu-id="37138-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37138-117">Requirement</span></span> | <span data-ttu-id="37138-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="37138-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="37138-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37138-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37138-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37138-120">Windows 8 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37138-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37138-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37138-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37138-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="37138-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="37138-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="37138-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="37138-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37138-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37138-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37138-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37138-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="37138-127">Attributs du writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="37138-127">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="37138-128">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="37138-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




