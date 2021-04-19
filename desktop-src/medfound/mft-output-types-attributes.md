---
description: Contient les types de sortie inscrits pour une Media Foundation transformation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Attribut MFT_OUTPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518989"
---
# <a name="mft_output_types_attributes-attribute"></a><span data-ttu-id="49c52-103">\_Attribut des \_ attributs des types de sortie MFT \_</span><span class="sxs-lookup"><span data-stu-id="49c52-103">MFT\_OUTPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="49c52-104">Contient les types de sortie inscrits pour une Media Foundation transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="49c52-104">Contains the registered output types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="49c52-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="49c52-105">Data type</span></span>

<span data-ttu-id="49c52-106">**MFT \_ Enregistrer \_ les \_ \[ informations \] de type** stockées en tant qu' **octets \[ \]**</span><span class="sxs-lookup"><span data-stu-id="49c52-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="remarks"></a><span data-ttu-id="49c52-107">Notes</span><span class="sxs-lookup"><span data-stu-id="49c52-107">Remarks</span></span>

<span data-ttu-id="49c52-108">Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="49c52-108">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="49c52-109">Cet attribut contient un tableau de structures d' [**\_ informations de \_ type \_ de Registre MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) qui décrivent un ou plusieurs formats de sortie pris en charge par la table MFT.</span><span class="sxs-lookup"><span data-stu-id="49c52-109">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more output formats supported by the MFT.</span></span> <span data-ttu-id="49c52-110">Ces valeurs sont extraites du Registre et sont destinées à l’application.</span><span class="sxs-lookup"><span data-stu-id="49c52-110">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="49c52-111">La table MFT peut prendre en charge des formats supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="49c52-111">The MFT might support additional formats.</span></span> <span data-ttu-id="49c52-112">Pour définir le format de sortie réel, vous devez créer la table MFT et appeler [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="49c52-112">To set the actual output format, you must create the MFT and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="49c52-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="49c52-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c52-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49c52-114">Requirements</span></span>



| <span data-ttu-id="49c52-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49c52-115">Requirement</span></span> | <span data-ttu-id="49c52-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="49c52-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="49c52-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49c52-117">Minimum supported client</span></span><br/> | <span data-ttu-id="49c52-118">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="49c52-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="49c52-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49c52-119">Minimum supported server</span></span><br/> | <span data-ttu-id="49c52-120">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="49c52-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="49c52-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="49c52-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="49c52-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="49c52-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c52-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49c52-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c52-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="49c52-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="49c52-125">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="49c52-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




