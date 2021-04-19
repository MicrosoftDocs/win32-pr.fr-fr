---
title: '\_ \_ Réponse d’ouverture de session EAP cred \_ (Eaptypes. h)'
description: Stocke les informations d’identification de sécurité EAP dans une \_ \_ structure de tableau de champs d’entrée de configuration EAP \_ \_ . | \_ \_ Réponse d’ouverture de session EAP cred \_ (Eaptypes. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106525833"
---
# <a name="eap_cred_logon_resp"></a><span data-ttu-id="6d9f3-105">\_ \_ réponse d’ouverture de session EAP cred \_</span><span class="sxs-lookup"><span data-stu-id="6d9f3-105">EAP\_CRED\_LOGON\_RESP</span></span>

<span data-ttu-id="6d9f3-106">La structure du **\_ \_ \_ REEE d’ouverture de session EAP cred** stocke les informations d’identification de sécurité EAP dans une structure de [**\_ \_ \_ \_ tableau de champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="6d9f3-106">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

<span data-ttu-id="6d9f3-107">**\_ \_ réponse d’ouverture de session EAP cred \_**</span><span class="sxs-lookup"><span data-stu-id="6d9f3-107">**EAP\_CRED\_LOGON\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="6d9f3-108">La structure du **\_ \_ \_ REEE d’ouverture de session EAP cred** stocke les informations d’identification de sécurité EAP vers lesquelles pointe le paramètre *pbUiData* de la structure de données de l' [**\_ \_ interface utilisateur \_ interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) lorsque le paramètre *dwDataType* du type de données de l' [**\_ \_ interface utilisateur \_ \_ interactive EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) spécifie un type de demande d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="6d9f3-108">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="6d9f3-109">Les champs d’entrée de cette structure sont les mêmes que les champs d’entrée retournés par [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="6d9f3-109">The input fields in this structure will be same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="6d9f3-110">**Protocole EAP \_ Le \_ REEE \_ d’ouverture de session cred** est utilisé dans la demande d’informations d’identification initiale et le [**\_ \_ REEE EAP cred**](eap-cred-resp.md) est utilisé dans la demande d’informations d’identification pendant une authentification.</span><span class="sxs-lookup"><span data-stu-id="6d9f3-110">**EAP\_CRED\_LOGON\_RESP** is used in the initial credential request and [**EAP\_CRED\_RESP**](eap-cred-resp.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d9f3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6d9f3-111">Remarks</span></span>

<span data-ttu-id="6d9f3-112">La structure de **\_ réponse aux \_ connexions \_ EAP cred** est utilisée pour prendre en charge l’authentification unique (SSO).</span><span class="sxs-lookup"><span data-stu-id="6d9f3-112">The **EAP\_CRED\_LOGON\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="6d9f3-113">La structure du **\_ \_ \_ REEE d’ouverture de session d’identification EAP** est identique à la structure de [**\_ \_ \_ demande d’ouverture de session EAP cred**](eap-cred-logon-req.md) .</span><span class="sxs-lookup"><span data-stu-id="6d9f3-113">The **EAP\_CRED\_LOGON\_RESP** structure is identical to the [**EAP\_CRED\_LOGON\_REQ**](eap-cred-logon-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d9f3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d9f3-114">Requirements</span></span>



| <span data-ttu-id="6d9f3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d9f3-115">Requirement</span></span> | <span data-ttu-id="6d9f3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d9f3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9f3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d9f3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9f3-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d9f3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d9f3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d9f3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9f3-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d9f3-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d9f3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d9f3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d9f3-122"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d9f3-122"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d9f3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d9f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9f3-124">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="6d9f3-124">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[<span data-ttu-id="6d9f3-125">**\_tableau de \_ champs d’entrée de configuration \_ EAP \_**</span><span class="sxs-lookup"><span data-stu-id="6d9f3-125">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="6d9f3-126">**\_ \_ demande d’ouverture de session EAP cred \_**</span><span class="sxs-lookup"><span data-stu-id="6d9f3-126">**EAP\_CRED\_LOGON\_REQ**</span></span>](eap-cred-logon-req.md)
</dt> <dt>

[<span data-ttu-id="6d9f3-127">**\_données de \_ l’interface utilisateur interactive EAP \_**</span><span class="sxs-lookup"><span data-stu-id="6d9f3-127">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="6d9f3-128">**\_type de \_ données de l’interface utilisateur interactive EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d9f3-128">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





