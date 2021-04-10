---
description: Valeur de la &\# 0034 ; CS (référant) &\# 0034 ; champ que la source réseau utilise pour la journalisation.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: MFNETSOURCE_BROWSERWEBPAGE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e8222761299cad229b692ef400f69d0968ebd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951388"
---
# <a name="mfnetsource_browserwebpage-property"></a><span data-ttu-id="a029c-103">MFNETSOURCE \_ propriété BROWSERWEBPAGE</span><span class="sxs-lookup"><span data-stu-id="a029c-103">MFNETSOURCE\_BROWSERWEBPAGE property</span></span>

<span data-ttu-id="a029c-104">Valeur du champ « cs (référant) » que la source réseau utilise pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="a029c-104">The value of the "cs(Referer)" field that the network source uses for logging.</span></span> <span data-ttu-id="a029c-105">Les applications peuvent définir cette propriété sur l’URL de la page Web dans laquelle l’application a été incorporée.</span><span class="sxs-lookup"><span data-stu-id="a029c-105">Applications can set this property to the URL of the webpage in which the application was embedded.</span></span>



<span data-ttu-id="a029c-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="a029c-106">Data type</span></span>

<span data-ttu-id="a029c-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a029c-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a029c-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a029c-108">PROPVARIANT member</span></span>

<span data-ttu-id="a029c-109">Chaîne de caractères larges (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="a029c-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="a029c-110">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="a029c-110">VT\_LPWSTR</span></span>

<span data-ttu-id="a029c-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="a029c-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a029c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a029c-112">Remarks</span></span>

<span data-ttu-id="a029c-113">La constante **MFNETSOURCE \_ BROWSERWEBPAGE** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="a029c-113">The constant **MFNETSOURCE\_BROWSERWEBPAGE** defines the GUID for this property key.</span></span> <span data-ttu-id="a029c-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a029c-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a029c-115">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="a029c-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="a029c-116">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="a029c-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a029c-117">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a029c-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a029c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a029c-118">Requirements</span></span>



| <span data-ttu-id="a029c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a029c-119">Requirement</span></span> | <span data-ttu-id="a029c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a029c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a029c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a029c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a029c-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a029c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a029c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a029c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a029c-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a029c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a029c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a029c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a029c-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a029c-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a029c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a029c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a029c-128">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="a029c-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="a029c-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a029c-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a029c-130">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a029c-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




