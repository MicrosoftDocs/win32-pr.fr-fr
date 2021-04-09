---
description: Liste des URL auxquelles la source réseau enverra les informations de journalisation.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: MFNETSOURCE_LOGURL, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113666"
---
# <a name="mfnetsource_logurl-property"></a><span data-ttu-id="6985f-103">MFNETSOURCE \_ propriété LOGURL</span><span class="sxs-lookup"><span data-stu-id="6985f-103">MFNETSOURCE\_LOGURL property</span></span>

<span data-ttu-id="6985f-104">Liste des URL auxquelles la source réseau enverra les informations de journalisation.</span><span class="sxs-lookup"><span data-stu-id="6985f-104">List of URLs to which the network source will send logging information.</span></span>



<span data-ttu-id="6985f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6985f-105">Data type</span></span>

<span data-ttu-id="6985f-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="6985f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6985f-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="6985f-107">PROPVARIANT member</span></span>

<span data-ttu-id="6985f-108">Tableau de chaînes de caractères larges (**CALPWSTR**)</span><span class="sxs-lookup"><span data-stu-id="6985f-108">Array of wide-character strings (**CALPWSTR**)</span></span>

<span data-ttu-id="6985f-109">\_LPWStr VT Vector \| VT \_</span><span class="sxs-lookup"><span data-stu-id="6985f-109">VT\_VECTOR \| VT\_LPWSTR</span></span>

<span data-ttu-id="6985f-110">**calpwstr**</span><span class="sxs-lookup"><span data-stu-id="6985f-110">**calpwstr**</span></span>



## <a name="remarks"></a><span data-ttu-id="6985f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6985f-111">Remarks</span></span>

<span data-ttu-id="6985f-112">La constante **MFNETSOURCE \_ LOGURL** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="6985f-112">The constant **MFNETSOURCE\_LOGURL** defines the GUID for this property key.</span></span> <span data-ttu-id="6985f-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6985f-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6985f-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="6985f-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="6985f-115">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="6985f-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="6985f-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="6985f-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6985f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6985f-117">Requirements</span></span>



| <span data-ttu-id="6985f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6985f-118">Requirement</span></span> | <span data-ttu-id="6985f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6985f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6985f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6985f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6985f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6985f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6985f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6985f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6985f-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6985f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6985f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6985f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6985f-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6985f-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6985f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6985f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6985f-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6985f-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6985f-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6985f-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




