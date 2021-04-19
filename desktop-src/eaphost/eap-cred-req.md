---
title: '\_Demande EAP cred \_ (Eaptypes. h)'
description: Stocke les informations d’identification de sécurité EAP dans une \_ \_ structure de tableau de champs d’entrée de configuration EAP \_ \_ . | \_Demande EAP cred \_ (Eaptypes. h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524818"
---
# <a name="eap_cred_req"></a><span data-ttu-id="8452b-105">\_demande EAP cred \_</span><span class="sxs-lookup"><span data-stu-id="8452b-105">EAP\_CRED\_REQ</span></span>

<span data-ttu-id="8452b-106">La structure de **\_ \_ demande** d’identification EAP stocke les informations d’identification de sécurité EAP dans une structure de [**\_ \_ \_ \_ tableau de champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="8452b-106">The **EAP\_CRED\_REQ** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

<span data-ttu-id="8452b-107">**\_demande EAP cred \_**</span><span class="sxs-lookup"><span data-stu-id="8452b-107">**EAP\_CRED\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="8452b-108">La structure de demande d’identification EAP stocke les anciennes et les nouvelles informations d’identification de sécurité EAP pointées par le paramètre *pbUiData* de la structure de données de l' [**\_ \_ interface utilisateur \_ interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) lorsque le paramètre *dwDataType* du type de données de l' [**\_ \_ interface utilisateur \_ \_ interactive EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) spécifie un type de demande d’informations d’identification. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="8452b-108">The **EAP\_CRED\_REQ** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8452b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8452b-109">Remarks</span></span>

<span data-ttu-id="8452b-110">La structure des **\_ \_ demandes EAP cred** est utilisée pour prendre en charge l’authentification unique (SSO).</span><span class="sxs-lookup"><span data-stu-id="8452b-110">The **EAP\_CRED\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="8452b-111">La structure des **\_ \_ demandes EAP cred** est identique à la structure du [**\_ \_ REEE**](eap-cred-resp.md) d’identification EAP.</span><span class="sxs-lookup"><span data-stu-id="8452b-111">The **EAP\_CRED\_REQ** structure is identical to the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8452b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8452b-112">Requirements</span></span>



| <span data-ttu-id="8452b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8452b-113">Requirement</span></span> | <span data-ttu-id="8452b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8452b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8452b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8452b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8452b-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8452b-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8452b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8452b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8452b-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8452b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8452b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="8452b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8452b-120"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8452b-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8452b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8452b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8452b-122">Structures du demandeur EAPHost</span><span class="sxs-lookup"><span data-stu-id="8452b-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="8452b-123">**réponse d’identification EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8452b-123">**EAP\_CRED\_RESP**</span></span>](eap-cred-resp.md)
</dt> <dt>

[<span data-ttu-id="8452b-124">**demande d’expiration d’un \_ cred EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8452b-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="8452b-125">[**réponse d’expiration d’un \_ cred EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8452b-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8452b-126">**\_données de \_ l’interface utilisateur interactive EAP \_**</span><span class="sxs-lookup"><span data-stu-id="8452b-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="8452b-127">SSO et PLAP</span><span class="sxs-lookup"><span data-stu-id="8452b-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

