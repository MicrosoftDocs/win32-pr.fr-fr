---
description: Active ou désactive le mode aperçu, ce qui permet à l’application de remplacer la logique de mise en mémoire tampon initiale.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: MFNETSOURCE_PREVIEWMODEENABLED, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541874"
---
# <a name="mfnetsource_previewmodeenabled-property"></a><span data-ttu-id="55af1-103">MFNETSOURCE \_ propriété PREVIEWMODEENABLED</span><span class="sxs-lookup"><span data-stu-id="55af1-103">MFNETSOURCE\_PREVIEWMODEENABLED property</span></span>

<span data-ttu-id="55af1-104">Active ou désactive le mode aperçu, ce qui permet à l’application de remplacer la logique de mise en mémoire tampon initiale.</span><span class="sxs-lookup"><span data-stu-id="55af1-104">Enables or disables preview mode, which enables the application to overwrite the initial buffering logic.</span></span>



<span data-ttu-id="55af1-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="55af1-105">Data type</span></span>

<span data-ttu-id="55af1-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="55af1-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="55af1-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="55af1-107">PROPVARIANT member</span></span>

<span data-ttu-id="55af1-108">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="55af1-108">**BOOL**</span></span>

<span data-ttu-id="55af1-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="55af1-109">VT\_BOOL</span></span>

<span data-ttu-id="55af1-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="55af1-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="55af1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="55af1-111">Remarks</span></span>

<span data-ttu-id="55af1-112">La constante **MFNETSOURCE \_ PREVIEWMODEENABLED** définit le GUID de la clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="55af1-112">The constant **MFNETSOURCE\_PREVIEWMODEENABLED** defines the GUID for the property key.</span></span> <span data-ttu-id="55af1-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="55af1-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="55af1-114">Cette propriété est définie sur la source réseau en passant un pointeur **IPropertyStore** vers le programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="55af1-114">This property is set on the network source by passing an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="55af1-115">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="55af1-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55af1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55af1-116">Requirements</span></span>



| <span data-ttu-id="55af1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55af1-117">Requirement</span></span> | <span data-ttu-id="55af1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="55af1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55af1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55af1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55af1-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55af1-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="55af1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55af1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55af1-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55af1-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="55af1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="55af1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55af1-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55af1-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55af1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55af1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55af1-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55af1-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="55af1-127">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55af1-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




