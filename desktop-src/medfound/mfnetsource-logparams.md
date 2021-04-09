---
description: Tableau de chaînes avec les paramètres à envoyer au serveur de journal.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: MFNETSOURCE_LOGPARAMS, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951532"
---
# <a name="mfnetsource_logparams-property"></a><span data-ttu-id="c7c6c-103">MFNETSOURCE \_ propriété LOGPARAMS</span><span class="sxs-lookup"><span data-stu-id="c7c6c-103">MFNETSOURCE\_LOGPARAMS property</span></span>

<span data-ttu-id="c7c6c-104">Tableau de chaînes avec les paramètres à envoyer au serveur de journal.</span><span class="sxs-lookup"><span data-stu-id="c7c6c-104">Array of strings with the parameters to send to the log server.</span></span>



<span data-ttu-id="c7c6c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c7c6c-105">Data type</span></span>

<span data-ttu-id="c7c6c-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="c7c6c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c7c6c-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="c7c6c-107">PROPVARIANT member</span></span>

<span data-ttu-id="c7c6c-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="c7c6c-108">\**WCHAR\** _</span></span>

<span data-ttu-id="c7c6c-109">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="c7c6c-109">VT\_LPWSTR</span></span>

<span data-ttu-id="c7c6c-110">_ *pwszVal*\*</span><span class="sxs-lookup"><span data-stu-id="c7c6c-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="c7c6c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c7c6c-111">Remarks</span></span>

<span data-ttu-id="c7c6c-112">La constante **MFNETSOURCE \_ LOGPARAMS** définit le GUID de la clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="c7c6c-112">The **MFNETSOURCE\_LOGPARAMS** constant defines the GUID for the property key.</span></span> <span data-ttu-id="c7c6c-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c7c6c-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="c7c6c-114">Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="c7c6c-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="c7c6c-115">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="c7c6c-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c6c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7c6c-116">Requirements</span></span>



| <span data-ttu-id="c7c6c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7c6c-117">Requirement</span></span> | <span data-ttu-id="c7c6c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7c6c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c6c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7c6c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c6c-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7c6c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c7c6c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7c6c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c6c-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7c6c-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c7c6c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7c6c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7c6c-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c6c-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c6c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7c6c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c6c-126">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7c6c-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c7c6c-127">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7c6c-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




