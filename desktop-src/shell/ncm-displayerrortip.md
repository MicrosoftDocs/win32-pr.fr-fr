---
description: Affiche un message d’erreur dans l’info-bulle associée au contrôle d’adresse réseau.
title: Message NCM_DISPLAYERRORTIP (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991112"
---
# <a name="ncm_displayerrortip-message"></a><span data-ttu-id="ca252-103">\_Message NCM DISPLAYERRORTIP</span><span class="sxs-lookup"><span data-stu-id="ca252-103">NCM\_DISPLAYERRORTIP message</span></span>

<span data-ttu-id="ca252-104">Affiche un message d’erreur dans l’info-bulle associée au contrôle d’adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="ca252-104">Displays an error message in the balloon tip associated with the network address control.</span></span>


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="ca252-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca252-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca252-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca252-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ca252-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ca252-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ca252-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca252-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ca252-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ca252-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca252-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca252-110">Return value</span></span>

<span data-ttu-id="ca252-111">Si ce message est correctement exécuté, il renvoie la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ca252-111">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ca252-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca252-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca252-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ca252-113">Remarks</span></span>

<span data-ttu-id="ca252-114">Envoyer ce message pour afficher un message d’erreur quand une adresse tapée dans le contrôle n’est pas validée par rapport aux types d’adresses réseau autorisés définis avec le message [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) .</span><span class="sxs-lookup"><span data-stu-id="ca252-114">Send this message to display an error message when an address typed into the control does not validate against the allowed network address types set with the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message.</span></span> <span data-ttu-id="ca252-115">Utilisez le message [**NCM \_ GETADDRESS**](ncm-getaddress.md) pour valider l’adresse.</span><span class="sxs-lookup"><span data-stu-id="ca252-115">Use the [**NCM\_GETADDRESS**](ncm-getaddress.md) message to validate the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca252-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ca252-116">Requirements</span></span>



| <span data-ttu-id="ca252-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca252-117">Requirement</span></span> | <span data-ttu-id="ca252-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca252-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca252-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca252-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ca252-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca252-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca252-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca252-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ca252-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca252-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca252-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca252-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca252-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca252-124"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca252-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca252-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca252-126">**DisplayErrorTip NETADDR \_**</span><span class="sxs-lookup"><span data-stu-id="ca252-126">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




