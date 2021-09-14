---
title: '\_ \_ Demande d’ouverture \_ de session EAP (Eaptypes. h)'
description: Stocke les informations d’identification de sécurité EAP dans une \_ \_ structure de tableau de champs d’entrée de configuration EAP \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118393"
---
# <a name="eap_cred_logon_req"></a>\_ \_ demande d’ouverture de session EAP cred \_

La **structure \_ \_ \_ req d’ouverture de session EAP cred** stocke les informations d’identification de sécurité EAP dans une structure de [**\_ \_ \_ \_ tableau de champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**\_ \_ demande d’ouverture de session EAP cred \_**
</dt> <dd>

La **structure \_ \_ \_ req Logon Logon d’EAP** stocke les informations d’identification de sécurité EAP vers lesquelles pointe le paramètre *pbUiData* de la structure de données de l' [**\_ \_ interface utilisateur \_ interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) lorsque le paramètre *dwDataType* du type de données de l' [**\_ \_ interface utilisateur \_ \_ interactive EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) spécifie un type de demande d’informations d’identification. Les champs d’entrée de cette structure sont les mêmes que les champs d’entrée retournés par [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **Protocole EAP \_ La demande d' \_ ouverture de session \_ cred** est utilisée dans la demande d’informations d’identification initiale et la demande [**EAP \_ cred \_**](eap-cred-req.md) est utilisée dans la demande d’informations d’identification pendant une authentification.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure de **\_ \_ \_ demande d’ouverture de session EAP cred** est utilisée pour prendre en charge l’authentification unique (SSO).

La structure de **\_ \_ \_ demande d’ouverture de session EAP cred** est identique à la structure du [**\_ \_ \_ REEE d’ouverture de session EAP cred**](eap-cred-logon-resp.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_tableau de \_ champs d’entrée de configuration \_ EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**\_demande EAP cred \_**](eap-cred-req.md)
</dt> <dt>

[**\_données de \_ l’interface utilisateur interactive EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**\_type de \_ données de l’interface utilisateur interactive EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





