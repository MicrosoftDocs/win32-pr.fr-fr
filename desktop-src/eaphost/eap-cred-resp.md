---
title: Protocole EAP \_ cred \_ REEE (Eaptypes. h)
description: Stocke les informations d’identification de sécurité EAP dans une \_ \_ structure de tableau de champs d’entrée de configuration EAP \_ \_ . | Protocole EAP \_ cred \_ REEE (Eaptypes. h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c2176377dbde0f7c02d2a7d8083ad1bcff9e71
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523771"
---
# <a name="eap_cred_resp"></a><span data-ttu-id="4c0a8-105">réponse d’identification EAP \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c0a8-105">EAP\_CRED\_RESP</span></span>

<span data-ttu-id="4c0a8-106">La structure du **\_ \_ REEE EAP cred** stocke les informations d’identification de sécurité EAP dans une structure de [**\_ \_ \_ \_ tableau de champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="4c0a8-106">The **EAP\_CRED\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

<span data-ttu-id="4c0a8-107">**réponse d’identification EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4c0a8-107">**EAP\_CRED\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="4c0a8-108">La structure du **\_ \_ REEE EAP cred** stocke à la fois les informations d’identification de sécurité EAP anciennes et nouvelles pointées par le paramètre *pbUiData* de la structure de données de l' [**\_ \_ interface utilisateur \_ interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) lorsque le paramètre *dwDataType* du type de données de l' [**\_ \_ interface utilisateur \_ \_ interactive EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) spécifie un type de réponse des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="4c0a8-108">The **EAP\_CRED\_RESP** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential response type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c0a8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4c0a8-109">Remarks</span></span>

<span data-ttu-id="4c0a8-110">La structure du **\_ \_ REEE EAP cred** est utilisée pour prendre en charge l’authentification unique (SSO).</span><span class="sxs-lookup"><span data-stu-id="4c0a8-110">The **EAP\_CRED\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="4c0a8-111">La structure du **\_ \_ REEE EAP cred** est identique à la structure de [**\_ \_ demande**](eap-cred-req.md) d’identification EAP.</span><span class="sxs-lookup"><span data-stu-id="4c0a8-111">The **EAP\_CRED\_RESP** structure is identical to the [**EAP\_CRED\_REQ**](eap-cred-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c0a8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c0a8-112">Requirements</span></span>



| <span data-ttu-id="4c0a8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c0a8-113">Requirement</span></span> | <span data-ttu-id="4c0a8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c0a8-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c0a8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c0a8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4c0a8-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c0a8-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c0a8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c0a8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4c0a8-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c0a8-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c0a8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c0a8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c0a8-120"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c0a8-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c0a8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c0a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c0a8-122">Structures du demandeur EAPHost</span><span class="sxs-lookup"><span data-stu-id="4c0a8-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="4c0a8-123">**\_demande EAP cred \_**</span><span class="sxs-lookup"><span data-stu-id="4c0a8-123">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="4c0a8-124">**demande d’expiration d’un \_ cred EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4c0a8-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="4c0a8-125">[**réponse d’expiration d’un \_ cred EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c0a8-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4c0a8-126">**\_données de \_ l’interface utilisateur interactive EAP \_**</span><span class="sxs-lookup"><span data-stu-id="4c0a8-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="4c0a8-127">SSO et PLAP</span><span class="sxs-lookup"><span data-stu-id="4c0a8-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

