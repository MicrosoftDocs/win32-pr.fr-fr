---
description: Nombre de fois où la source réseau tente de se reconnecter au serveur et de reprendre la diffusion en continu si la connexion est perdue.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: MFNETSOURCE_AUTORECONNECTLIMIT, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac2a81cb4d47d8113059924877670458ac22ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753133"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a><span data-ttu-id="acbb9-103">MFNETSOURCE \_ propriété AUTORECONNECTLIMIT</span><span class="sxs-lookup"><span data-stu-id="acbb9-103">MFNETSOURCE\_AUTORECONNECTLIMIT property</span></span>

<span data-ttu-id="acbb9-104">Nombre de fois où la source réseau tente de se reconnecter au serveur et de reprendre la diffusion en continu si la connexion est perdue.</span><span class="sxs-lookup"><span data-stu-id="acbb9-104">The number of times the network source tries to reconnect to the server and resume streaming if the connection is lost.</span></span>



<span data-ttu-id="acbb9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="acbb9-105">Data type</span></span>

<span data-ttu-id="acbb9-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="acbb9-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="acbb9-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="acbb9-107">PROPVARIANT member</span></span>

<span data-ttu-id="acbb9-108">**DWORD** (stocké en tant que **long**)</span><span class="sxs-lookup"><span data-stu-id="acbb9-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="acbb9-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="acbb9-109">VT\_I4</span></span>

<span data-ttu-id="acbb9-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="acbb9-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="acbb9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="acbb9-111">Remarks</span></span>

<span data-ttu-id="acbb9-112">La constante **MFNETSOURCE \_ AUTORECONNECTLIMIT** définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="acbb9-112">The constant **MFNETSOURCE\_AUTORECONNECTLIMIT** defines the GUID for this property key.</span></span> <span data-ttu-id="acbb9-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="acbb9-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="acbb9-114">Les applications peuvent utiliser cette propriété pour configurer la source réseau.</span><span class="sxs-lookup"><span data-stu-id="acbb9-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="acbb9-115">Pour définir la propriété, transmettez un objet **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="acbb9-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="acbb9-116">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="acbb9-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="acbb9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acbb9-117">Requirements</span></span>



| <span data-ttu-id="acbb9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acbb9-118">Requirement</span></span> | <span data-ttu-id="acbb9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="acbb9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="acbb9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acbb9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="acbb9-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acbb9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="acbb9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acbb9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="acbb9-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acbb9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="acbb9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="acbb9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="acbb9-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="acbb9-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acbb9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acbb9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acbb9-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="acbb9-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="acbb9-128">Fonctionnalités de la source réseau</span><span class="sxs-lookup"><span data-stu-id="acbb9-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="acbb9-129">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="acbb9-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




