---
description: Valeur de la &\# 0034 ; c-hostexe&\# 0034 ; le champ que la source réseau utilise pour la journalisation.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: MFNETSOURCE_HOSTEXE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ac786fe08ede556537703d2eb886b30be39207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759075"
---
# <a name="mfnetsource_hostexe-property"></a><span data-ttu-id="8dcd0-103">MFNETSOURCE \_ propriété HOSTEXE</span><span class="sxs-lookup"><span data-stu-id="8dcd0-103">MFNETSOURCE\_HOSTEXE property</span></span>

<span data-ttu-id="8dcd0-104">Valeur du champ « c-hostexe » que la source réseau utilise pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="8dcd0-104">The value of the "c-hostexe" field that the network source uses for logging.</span></span> <span data-ttu-id="8dcd0-105">Les applications peuvent définir cette propriété sur le nom de l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="8dcd0-105">Applications can set this property to the name of the host application.</span></span> <span data-ttu-id="8dcd0-106">Par exemple, la valeur peut être « iexplore.exe » si l’application est hébergée dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="8dcd0-106">For example, the value could be "iexplore.exe" if the application is hosted in a webpage.</span></span>



<span data-ttu-id="8dcd0-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="8dcd0-107">Data type</span></span>

<span data-ttu-id="8dcd0-108">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8dcd0-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8dcd0-109">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8dcd0-109">PROPVARIANT member</span></span>

<span data-ttu-id="8dcd0-110">Chaîne de caractères larges (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="8dcd0-110">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="8dcd0-111">\_LPWStr VT</span><span class="sxs-lookup"><span data-stu-id="8dcd0-111">VT\_LPWSTR</span></span>

<span data-ttu-id="8dcd0-112">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="8dcd0-112">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="8dcd0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8dcd0-113">Remarks</span></span>

<span data-ttu-id="8dcd0-114">La constante **MFNETSOURCE \_ HOSTEXE** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="8dcd0-114">The constant **MFNETSOURCE\_HOSTEXE** defines the GUID for this property key.</span></span> <span data-ttu-id="8dcd0-115">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8dcd0-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="8dcd0-116">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="8dcd0-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="8dcd0-117">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="8dcd0-117">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="8dcd0-118">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="8dcd0-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8dcd0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dcd0-119">Requirements</span></span>



| <span data-ttu-id="8dcd0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dcd0-120">Requirement</span></span> | <span data-ttu-id="8dcd0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcd0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8dcd0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dcd0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8dcd0-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dcd0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8dcd0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dcd0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8dcd0-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dcd0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8dcd0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8dcd0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dcd0-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dcd0-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dcd0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dcd0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dcd0-129">Journalisation du client</span><span class="sxs-lookup"><span data-stu-id="8dcd0-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="8dcd0-130">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8dcd0-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8dcd0-131">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8dcd0-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




