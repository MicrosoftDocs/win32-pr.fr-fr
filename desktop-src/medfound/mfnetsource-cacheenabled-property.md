---
description: Spécifie si la source réseau met en cache le contenu.
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: MFNETSOURCE_CACHEENABLED, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6f38398e44eaa25da7a5b1f88a76edb8e40924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863162"
---
# <a name="mfnetsource_cacheenabled-property"></a><span data-ttu-id="bf9cc-103">MFNETSOURCE \_ propriété CACHEENABLED</span><span class="sxs-lookup"><span data-stu-id="bf9cc-103">MFNETSOURCE\_CACHEENABLED property</span></span>

<span data-ttu-id="bf9cc-104">Spécifie si la source réseau met en cache le contenu.</span><span class="sxs-lookup"><span data-stu-id="bf9cc-104">Specifies whether the network source caches content.</span></span>



<span data-ttu-id="bf9cc-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="bf9cc-105">Data type</span></span>

<span data-ttu-id="bf9cc-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="bf9cc-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bf9cc-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="bf9cc-107">PROPVARIANT member</span></span>

<span data-ttu-id="bf9cc-108">Boolean (**long**)</span><span class="sxs-lookup"><span data-stu-id="bf9cc-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="bf9cc-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="bf9cc-109">VT\_I4</span></span>

<span data-ttu-id="bf9cc-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="bf9cc-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="bf9cc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bf9cc-111">Remarks</span></span>

<span data-ttu-id="bf9cc-112">La constante **MFNETSOURCE \_ CACHEENABLED** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="bf9cc-112">The constant **MFNETSOURCE\_CACHEENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="bf9cc-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="bf9cc-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="bf9cc-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="bf9cc-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="bf9cc-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="bf9cc-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="bf9cc-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="bf9cc-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="bf9cc-117">La valeur par défaut de cette propriété est **true**.</span><span class="sxs-lookup"><span data-stu-id="bf9cc-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf9cc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf9cc-118">Requirements</span></span>



| <span data-ttu-id="bf9cc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf9cc-119">Requirement</span></span> | <span data-ttu-id="bf9cc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf9cc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9cc-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf9cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bf9cc-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf9cc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bf9cc-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf9cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bf9cc-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf9cc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bf9cc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf9cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf9cc-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf9cc-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf9cc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf9cc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf9cc-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf9cc-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="bf9cc-129">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf9cc-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




