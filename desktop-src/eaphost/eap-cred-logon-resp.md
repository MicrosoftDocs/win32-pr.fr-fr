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
# <a name="eap_cred_logon_resp"></a>\_ \_ réponse d’ouverture de session EAP cred \_

La structure du **\_ \_ \_ REEE d’ouverture de session EAP cred** stocke les informations d’identification de sécurité EAP dans une structure de [**\_ \_ \_ \_ tableau de champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

**\_ \_ réponse d’ouverture de session EAP cred \_**
</dt> <dd>

La structure du **\_ \_ \_ REEE d’ouverture de session EAP cred** stocke les informations d’identification de sécurité EAP vers lesquelles pointe le paramètre *pbUiData* de la structure de données de l' [**\_ \_ interface utilisateur \_ interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) lorsque le paramètre *dwDataType* du type de données de l' [**\_ \_ interface utilisateur \_ \_ interactive EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) spécifie un type de demande d’informations d’identification. Les champs d’entrée de cette structure sont les mêmes que les champs d’entrée retournés par [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **Protocole EAP \_ Le \_ REEE \_ d’ouverture de session cred** est utilisé dans la demande d’informations d’identification initiale et le [**\_ \_ REEE EAP cred**](eap-cred-resp.md) est utilisé dans la demande d’informations d’identification pendant une authentification.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure de **\_ réponse aux \_ connexions \_ EAP cred** est utilisée pour prendre en charge l’authentification unique (SSO).

La structure du **\_ \_ \_ REEE d’ouverture de session d’identification EAP** est identique à la structure de [**\_ \_ \_ demande d’ouverture de session EAP cred**](eap-cred-logon-req.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[**\_tableau de \_ champs d’entrée de configuration \_ EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**\_ \_ demande d’ouverture de session EAP cred \_**](eap-cred-logon-req.md)
</dt> <dt>

[**\_données de \_ l’interface utilisateur interactive EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**\_type de \_ données de l’interface utilisateur interactive EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





