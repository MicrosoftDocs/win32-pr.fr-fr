---
description: Définit les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.
title: Message NCM_SETALLOWTYPE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753053"
---
# <a name="ncm_setallowtype-message"></a><span data-ttu-id="52766-103">\_Message NCM SETALLOWTYPE</span><span class="sxs-lookup"><span data-stu-id="52766-103">NCM\_SETALLOWTYPE message</span></span>

<span data-ttu-id="52766-104">Définit les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.</span><span class="sxs-lookup"><span data-stu-id="52766-104">Sets the network address types that a specified network address control accepts.</span></span>


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="52766-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52766-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52766-106">*addrMask* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52766-106">*addrMask* \[in\]</span></span>
</dt> <dd><span data-ttu-id="52766-107">Spécifie les types d’adresses réseau sous la forme d’une ou de plusieurs constantes de <a href="net-string.md">**\_ chaîne net**</a> .</span><span class="sxs-lookup"><span data-stu-id="52766-107">Specifies the network address types as one or more of the <a href="net-string.md">**NET\_STRING**</a> constants.</span></span></dd> <dt>

<span data-ttu-id="52766-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52766-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="52766-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="52766-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52766-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52766-110">Return value</span></span>

<span data-ttu-id="52766-111">Retourne S \_ OK en cas de réussite, ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="52766-111">Returns S\_OK if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="52766-112">Notes</span><span class="sxs-lookup"><span data-stu-id="52766-112">Remarks</span></span>

<span data-ttu-id="52766-113">L’ensemble de masques est le critère utilisé pour valider une adresse réseau dans le message [**NCM \_ GETADDRESS**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="52766-113">The mask set is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="52766-114">Utilisez ce message pour un contrôle d’adresse réseau uniquement.</span><span class="sxs-lookup"><span data-stu-id="52766-114">Use this message for a network address control only.</span></span> <span data-ttu-id="52766-115">Pour instancier, utilisez la classe **msctls \_ NetAddress** définie dans shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="52766-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="52766-116">Appelez [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) au moment de l’exécution avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="52766-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="52766-117">Cette commande initialise la bibliothèque de contrôles communs qui contient le contrôle d’adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="52766-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="52766-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="52766-118">Requirements</span></span>



| <span data-ttu-id="52766-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52766-119">Requirement</span></span> | <span data-ttu-id="52766-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="52766-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52766-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52766-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52766-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52766-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52766-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52766-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52766-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52766-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52766-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="52766-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="52766-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="52766-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52766-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52766-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52766-128">**NCM \_ GETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="52766-128">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="52766-129">**SetAllowType NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="52766-129">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




