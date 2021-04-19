---
description: Active le mode de téléchargement privé dans la source réseau.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: MFNETSOURCE_ENABLE_PRIVATEMODE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531809"
---
# <a name="mfnetsource_enable_privatemode-property"></a><span data-ttu-id="97e05-103">MFNETSOURCE \_ activer la \_ propriété PRIVATEMODE</span><span class="sxs-lookup"><span data-stu-id="97e05-103">MFNETSOURCE\_ENABLE\_PRIVATEMODE property</span></span>

<span data-ttu-id="97e05-104">Active le mode de téléchargement privé dans la source réseau.</span><span class="sxs-lookup"><span data-stu-id="97e05-104">Enables private download mode in the network source.</span></span>



<span data-ttu-id="97e05-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="97e05-105">Data type</span></span>

<span data-ttu-id="97e05-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="97e05-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="97e05-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="97e05-107">PROPVARIANT member</span></span>

<span data-ttu-id="97e05-108">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="97e05-108">**BOOL**</span></span>

<span data-ttu-id="97e05-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="97e05-109">VT\_I4</span></span>

<span data-ttu-id="97e05-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="97e05-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="97e05-111">Notes</span><span class="sxs-lookup"><span data-stu-id="97e05-111">Remarks</span></span>

<span data-ttu-id="97e05-112">Si cette propriété a la **valeur true**, le cache est effacé à la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="97e05-112">If this property is **TRUE**, the cache is cleared when the session ends.</span></span>

<span data-ttu-id="97e05-113">La constante **MFNETSOURCE \_ CLIENTGUID** définit le GUID de la clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="97e05-113">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="97e05-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="97e05-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="97e05-115">Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="97e05-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="97e05-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="97e05-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97e05-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97e05-117">Requirements</span></span>



| <span data-ttu-id="97e05-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97e05-118">Requirement</span></span> | <span data-ttu-id="97e05-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="97e05-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97e05-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e05-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97e05-121">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97e05-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="97e05-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e05-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97e05-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e05-123">None supported</span></span><br/>                                                          |
| <span data-ttu-id="97e05-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="97e05-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e05-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97e05-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e05-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97e05-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e05-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97e05-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="97e05-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97e05-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




