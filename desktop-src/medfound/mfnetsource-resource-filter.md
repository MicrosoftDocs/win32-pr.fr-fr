---
description: Contient un pointeur vers l’interface de rappel IMFNetResourceFilter pour le flux d’octets HTTP Microsoft Media Foundation.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: MFNETSOURCE_RESOURCE_FILTER, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754260"
---
# <a name="mfnetsource_resource_filter-property"></a><span data-ttu-id="05e86-103">Propriété de filtre de \_ ressource MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="05e86-103">MFNETSOURCE\_RESOURCE\_FILTER property</span></span>

<span data-ttu-id="05e86-104">Contient un pointeur vers l’interface de rappel [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) pour le flux d’octets http Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05e86-104">Contains a pointer to the [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) callback interface for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="05e86-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="05e86-105">Data type</span></span>

<span data-ttu-id="05e86-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="05e86-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="05e86-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="05e86-107">PROPVARIANT member</span></span>

<span data-ttu-id="05e86-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="05e86-108">\**IUnknown\** _</span></span>

<span data-ttu-id="05e86-109">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="05e86-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="05e86-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="05e86-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="05e86-111">Notes</span><span class="sxs-lookup"><span data-stu-id="05e86-111">Remarks</span></span>

<span data-ttu-id="05e86-112">Utilisez cette propriété pour configurer le flux d’octets HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="05e86-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="05e86-113">Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="05e86-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="05e86-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="05e86-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05e86-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05e86-115">Requirements</span></span>



| <span data-ttu-id="05e86-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05e86-116">Requirement</span></span> | <span data-ttu-id="05e86-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="05e86-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05e86-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05e86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05e86-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05e86-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="05e86-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05e86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05e86-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05e86-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="05e86-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="05e86-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="05e86-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05e86-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05e86-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05e86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e86-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05e86-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
