---
title: '\_ \_ Demande d’ouverture \_ de session EAP (Eaptypes. h)'
description: Stocke les informations d’identification de sécurité EAP dans une \_ \_ structure de tableau de champs d’entrée de configuration EAP \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032628"
---
# <a name="eap_cred_logon_req"></a><span data-ttu-id="d60a8-104">\_ \_ demande d’ouverture de session EAP cred \_</span><span class="sxs-lookup"><span data-stu-id="d60a8-104">EAP\_CRED\_LOGON\_REQ</span></span>

<span data-ttu-id="d60a8-105">La **structure \_ \_ \_ req d’ouverture de session EAP cred** stocke les informations d’identification de sécurité EAP dans une structure de [**\_ \_ \_ \_ tableau de champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="d60a8-105">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials within an [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

<span data-ttu-id="d60a8-106">**\_ \_ demande d’ouverture de session EAP cred \_**</span><span class="sxs-lookup"><span data-stu-id="d60a8-106">**EAP\_CRED\_LOGON\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="d60a8-107">La **structure \_ \_ \_ req Logon Logon d’EAP** stocke les informations d’identification de sécurité EAP vers lesquelles pointe le paramètre *pbUiData* de la structure de données de l' [**\_ \_ interface utilisateur \_ interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) lorsque le paramètre *dwDataType* du type de données de l' [**\_ \_ interface utilisateur \_ \_ interactive EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) spécifie un type de demande d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="d60a8-107">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="d60a8-108">Les champs d’entrée de cette structure sont les mêmes que les champs d’entrée retournés par [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="d60a8-108">The input fields in this structure are the same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="d60a8-109">**Protocole EAP \_ La demande d' \_ ouverture de session \_ cred** est utilisée dans la demande d’informations d’identification initiale et la demande [**EAP \_ cred \_**](eap-cred-req.md) est utilisée dans la demande d’informations d’identification pendant une authentification.</span><span class="sxs-lookup"><span data-stu-id="d60a8-109">**EAP\_CRED\_LOGON\_REQ** is used in the initial credential request and [**EAP\_CRED\_REQ**](eap-cred-req.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d60a8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d60a8-110">Remarks</span></span>

<span data-ttu-id="d60a8-111">La structure de **\_ \_ \_ demande d’ouverture de session EAP cred** est utilisée pour prendre en charge l’authentification unique (SSO).</span><span class="sxs-lookup"><span data-stu-id="d60a8-111">The **EAP\_CRED\_LOGON\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="d60a8-112">La structure de **\_ \_ \_ demande d’ouverture de session EAP cred** est identique à la structure du [**\_ \_ \_ REEE d’ouverture de session EAP cred**](eap-cred-logon-resp.md) .</span><span class="sxs-lookup"><span data-stu-id="d60a8-112">The **EAP\_CRED\_LOGON\_REQ** structure is identical to the [**EAP\_CRED\_LOGON\_RESP**](eap-cred-logon-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d60a8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d60a8-113">Requirements</span></span>



| <span data-ttu-id="d60a8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d60a8-114">Requirement</span></span> | <span data-ttu-id="d60a8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d60a8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d60a8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d60a8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d60a8-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d60a8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d60a8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d60a8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d60a8-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d60a8-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d60a8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d60a8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d60a8-121"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d60a8-121"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d60a8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d60a8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d60a8-123">**\_tableau de \_ champs d’entrée de configuration \_ EAP \_**</span><span class="sxs-lookup"><span data-stu-id="d60a8-123">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="d60a8-124">**\_demande EAP cred \_**</span><span class="sxs-lookup"><span data-stu-id="d60a8-124">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="d60a8-125">**\_données de \_ l’interface utilisateur interactive EAP \_**</span><span class="sxs-lookup"><span data-stu-id="d60a8-125">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="d60a8-126">**\_type de \_ données de l’interface utilisateur interactive EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d60a8-126">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[<span data-ttu-id="d60a8-127">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="d60a8-127">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





