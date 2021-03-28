---
description: Récupère les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.
title: Message NCM_GETALLOWTYPE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034097"
---
# <a name="ncm_getallowtype-message"></a><span data-ttu-id="a25f0-103">\_Message NCM GETALLOWTYPE</span><span class="sxs-lookup"><span data-stu-id="a25f0-103">NCM\_GETALLOWTYPE message</span></span>

<span data-ttu-id="a25f0-104">Récupère les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.</span><span class="sxs-lookup"><span data-stu-id="a25f0-104">Retrieves the network address types that a specified network address control accepts.</span></span>


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="a25f0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a25f0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a25f0-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a25f0-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a25f0-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a25f0-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a25f0-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a25f0-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a25f0-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a25f0-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a25f0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a25f0-110">Return value</span></span>

<span data-ttu-id="a25f0-111">Retourne les types d’adresses réseau autorisés comme une ou plusieurs des constantes de [**\_ chaîne net**](net-string.md) .</span><span class="sxs-lookup"><span data-stu-id="a25f0-111">Returns the allowed network address types as one or more of the [**NET\_STRING**](net-string.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="a25f0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a25f0-112">Remarks</span></span>

<span data-ttu-id="a25f0-113">Le masque retourné est le critère utilisé pour valider une adresse réseau dans le message [**NCM \_ GETADDRESS**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="a25f0-113">The returned mask is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="a25f0-114">Utilisez ce message pour un contrôle d’adresse réseau uniquement.</span><span class="sxs-lookup"><span data-stu-id="a25f0-114">Use this message for a network address control only.</span></span> <span data-ttu-id="a25f0-115">Pour instancier, utilisez la classe **msctls \_ NetAddress** définie dans shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="a25f0-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="a25f0-116">Appelez [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) au moment de l’exécution avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="a25f0-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="a25f0-117">Cette commande initialise la bibliothèque de contrôles communs qui contient le contrôle d’adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="a25f0-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a25f0-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a25f0-118">Requirements</span></span>



| <span data-ttu-id="a25f0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a25f0-119">Requirement</span></span> | <span data-ttu-id="a25f0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a25f0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a25f0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a25f0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a25f0-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a25f0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a25f0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a25f0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a25f0-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a25f0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a25f0-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a25f0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a25f0-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a25f0-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a25f0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a25f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a25f0-128">**NCM \_ SETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="a25f0-128">**NCM\_SETALLOWTYPE**</span></span>](ncm-setallowtype.md)
</dt> <dt>

[<span data-ttu-id="a25f0-129">**GetAllowType NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="a25f0-129">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




