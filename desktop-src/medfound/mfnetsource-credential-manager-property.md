---
description: Contient un pointeur vers l’interface IMFNetCredentialManager.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: MFNETSOURCE_CREDENTIAL_MANAGER, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113999"
---
# <a name="mfnetsource_credential_manager-property"></a><span data-ttu-id="8c700-103">\_Propriété du gestionnaire d’informations d’identification MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="8c700-103">MFNETSOURCE\_CREDENTIAL\_MANAGER property</span></span>

<span data-ttu-id="8c700-104">Contient un pointeur vers l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="8c700-104">Contains a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="8c700-105">Utilisez cette propriété pour passer l’implémentation de [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) de l’application à la source réseau.</span><span class="sxs-lookup"><span data-stu-id="8c700-105">Use this property to pass the application's implementation of [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) to the network source.</span></span>



<span data-ttu-id="8c700-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="8c700-106">Data type</span></span>

<span data-ttu-id="8c700-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8c700-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8c700-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8c700-108">PROPVARIANT member</span></span>

<span data-ttu-id="8c700-109">**IUnknown** , pointeur</span><span class="sxs-lookup"><span data-stu-id="8c700-109">**IUnknown** pointer</span></span>

<span data-ttu-id="8c700-110">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="8c700-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="8c700-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="8c700-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="8c700-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8c700-112">Remarks</span></span>

<span data-ttu-id="8c700-113">Le **Gestionnaire des \_ informations \_ d’identification** de constante MFNETSOURCE définit le **GUID** de la clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="8c700-113">The constant **MFNETSOURCE\_CREDENTIAL\_MANAGER** defines the **GUID** for the property key.</span></span> <span data-ttu-id="8c700-114">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8c700-114">The property identifier (PID) is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c700-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c700-115">Requirements</span></span>



| <span data-ttu-id="8c700-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c700-116">Requirement</span></span> | <span data-ttu-id="8c700-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c700-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c700-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c700-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8c700-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c700-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8c700-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c700-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8c700-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c700-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8c700-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c700-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c700-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c700-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c700-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c700-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c700-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c700-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8c700-126">Authentification de la source réseau</span><span class="sxs-lookup"><span data-stu-id="8c700-126">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> <dt>

[<span data-ttu-id="8c700-127">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c700-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




