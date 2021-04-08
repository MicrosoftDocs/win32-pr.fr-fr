---
description: Valeur de la &\# 0034 ; c-playerid&\# 0034 ; le champ que la source réseau utilise pour la journalisation.
ms.assetid: de52cc34-9b88-41ae-b8b8-ef5dff85892c
title: MFNETSOURCE_PLAYERID, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d20754c93057ef3f000fc9c7201cda7ec287eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034892"
---
# <a name="mfnetsource_playerid-property"></a><span data-ttu-id="8fc8f-103">MFNETSOURCE \_ propriété PLAYERID</span><span class="sxs-lookup"><span data-stu-id="8fc8f-103">MFNETSOURCE\_PLAYERID property</span></span>

<span data-ttu-id="8fc8f-104">Valeur du champ « c-playerid » que la source réseau utilise pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="8fc8f-104">The value of the "c-playerid" field that the network source uses for logging.</span></span> <span data-ttu-id="8fc8f-105">Les applications peuvent définir cette propriété sur n’importe quelle valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="8fc8f-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="8fc8f-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="8fc8f-106">Data type</span></span>

<span data-ttu-id="8fc8f-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8fc8f-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8fc8f-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8fc8f-108">PROPVARIANT member</span></span>

<span data-ttu-id="8fc8f-109">Chaîne de caractères larges (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="8fc8f-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="8fc8f-110">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="8fc8f-110">VT\_LPWSTR</span></span>

<span data-ttu-id="8fc8f-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="8fc8f-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="8fc8f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8fc8f-112">Remarks</span></span>

<span data-ttu-id="8fc8f-113">La constante **MFNETSOURCE \_ PLAYERID** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="8fc8f-113">The constant **MFNETSOURCE\_PLAYERID** defines the GUID for this property key.</span></span> <span data-ttu-id="8fc8f-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8fc8f-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="8fc8f-115">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="8fc8f-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="8fc8f-116">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="8fc8f-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="8fc8f-117">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="8fc8f-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc8f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fc8f-118">Requirements</span></span>



| <span data-ttu-id="8fc8f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fc8f-119">Requirement</span></span> | <span data-ttu-id="8fc8f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fc8f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc8f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fc8f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc8f-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fc8f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8fc8f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fc8f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc8f-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fc8f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8fc8f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fc8f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fc8f-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc8f-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc8f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fc8f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc8f-128">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="8fc8f-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="8fc8f-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8fc8f-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8fc8f-130">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8fc8f-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




