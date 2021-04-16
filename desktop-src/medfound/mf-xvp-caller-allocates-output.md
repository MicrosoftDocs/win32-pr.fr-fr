---
description: Spécifie si l’appelant doit allouer les textures utilisées pour la sortie.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Attribut MF_XVP_CALLER_ALLOCATES_OUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527394"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a><span data-ttu-id="06073-103">L' \_ appelant MF XVP \_ \_ alloue l' \_ attribut de sortie</span><span class="sxs-lookup"><span data-stu-id="06073-103">MF\_XVP\_CALLER\_ALLOCATES\_OUTPUT attribute</span></span>

<span data-ttu-id="06073-104">Spécifie si l’appelant doit allouer les textures utilisées pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="06073-104">Specifies whether that the caller will allocate the textures used for output.</span></span>

## <a name="data-type"></a><span data-ttu-id="06073-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="06073-105">Data type</span></span>

<span data-ttu-id="06073-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06073-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="06073-107">Notes</span><span class="sxs-lookup"><span data-stu-id="06073-107">Remarks</span></span>

<span data-ttu-id="06073-108">Si cet attribut a la **valeur true**, le processeur vidéo s’attend à ce que la texture de sortie soit allouée par l’appelant, même en mode d’accélération vidéo DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="06073-108">If this attribute is **TRUE**, the video processor expect output textures to be allocated by the caller, even when operating in DirectX Video Acceleration (DXVA) mode.</span></span> <span data-ttu-id="06073-109">Si cet attribut a la **valeur false**, le processeur vidéo alloue les textures de sortie en mode DXVA, et échoue si l’appelant a fourni des textures de sortie.</span><span class="sxs-lookup"><span data-stu-id="06073-109">If this attribute is **FALSE**, the video processor will allocate the output textures when operating in DXVA mode, and will fail if caller provided output textures are provided.</span></span>

<span data-ttu-id="06073-110">Pour définir cet attribut :</span><span class="sxs-lookup"><span data-stu-id="06073-110">To set this attribute:</span></span>

1.  <span data-ttu-id="06073-111">Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="06073-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="06073-112">Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="06073-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="06073-113">Définissez l’attribut avant le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="06073-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="06073-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06073-114">Requirements</span></span>



| <span data-ttu-id="06073-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06073-115">Requirement</span></span> | <span data-ttu-id="06073-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="06073-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="06073-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06073-117">Minimum supported client</span></span><br/> | <span data-ttu-id="06073-118">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06073-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="06073-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06073-119">Minimum supported server</span></span><br/> | <span data-ttu-id="06073-120">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06073-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="06073-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="06073-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="06073-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="06073-122"><dt>Mfidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="06073-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="06073-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06073-124"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06073-124"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06073-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06073-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06073-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06073-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




