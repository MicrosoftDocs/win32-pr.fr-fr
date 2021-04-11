---
description: Identificateur unique par lequel le serveur identifie le client.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: MFNETSOURCE_CLIENTGUID, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114002"
---
# <a name="mfnetsource_clientguid-property"></a><span data-ttu-id="70346-103">MFNETSOURCE \_ propriété CLIENTGUID</span><span class="sxs-lookup"><span data-stu-id="70346-103">MFNETSOURCE\_CLIENTGUID property</span></span>

<span data-ttu-id="70346-104">Identificateur unique par lequel le serveur identifie le client.</span><span class="sxs-lookup"><span data-stu-id="70346-104">Unique identifier by which the server identifies the client.</span></span>



<span data-ttu-id="70346-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="70346-105">Data type</span></span>

<span data-ttu-id="70346-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="70346-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="70346-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="70346-107">PROPVARIANT member</span></span>

<span data-ttu-id="70346-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="70346-108">**GUID**</span></span>

<span data-ttu-id="70346-109">\_CLSID VT</span><span class="sxs-lookup"><span data-stu-id="70346-109">VT\_CLSID</span></span>

<span data-ttu-id="70346-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="70346-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="70346-111">Notes</span><span class="sxs-lookup"><span data-stu-id="70346-111">Remarks</span></span>

<span data-ttu-id="70346-112">La constante **MFNETSOURCE \_ CLIENTGUID** définit le GUID de la clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="70346-112">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="70346-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="70346-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="70346-114">Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="70346-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="70346-115">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="70346-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="70346-116">Si la valeur n’est pas définie ou définie en tant que **GUID \_ NULL**, Microsoft Media Foundation génère un GUID anonyme par session qui garantit la confidentialité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="70346-116">If not set or set as **GUID\_NULL**, Microsoft Media Foundation generates an anonymous GUID per session that ensures the user's privacy.</span></span>

## <a name="requirements"></a><span data-ttu-id="70346-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70346-117">Requirements</span></span>



| <span data-ttu-id="70346-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70346-118">Requirement</span></span> | <span data-ttu-id="70346-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="70346-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70346-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70346-120">Minimum supported client</span></span><br/> | <span data-ttu-id="70346-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70346-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="70346-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70346-122">Minimum supported server</span></span><br/> | <span data-ttu-id="70346-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70346-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="70346-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="70346-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="70346-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="70346-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70346-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70346-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70346-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70346-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="70346-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70346-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




