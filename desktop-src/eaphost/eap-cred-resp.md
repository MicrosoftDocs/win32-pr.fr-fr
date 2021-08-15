---
title: Protocole EAP \_ cred \_ REEE (Eaptypes. h)
description: Stocke les informations d’identification de sécurité EAP dans une \_ \_ structure de tableau de champs d’entrée de configuration EAP \_ \_ . | Protocole EAP \_ cred \_ REEE (Eaptypes. h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b9bda55ed1b4aee9a9847740b25d46418c6ec3544dfdd6ba71b2c282042b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904636"
---
# <a name="eap_cred_resp"></a>réponse d’identification EAP \_ \_

La structure du **\_ \_ REEE EAP cred** stocke les informations d’identification de sécurité EAP dans une structure de [**\_ \_ \_ \_ tableau de champs d’entrée de configuration EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

**réponse d’identification EAP \_ \_**
</dt> <dd>

La structure du **\_ \_ REEE EAP cred** stocke à la fois les informations d’identification de sécurité EAP anciennes et nouvelles pointées par le paramètre *pbUiData* de la structure de données de l' [**\_ \_ interface utilisateur \_ interactive EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) lorsque le paramètre *dwDataType* du type de données de l' [**\_ \_ interface utilisateur \_ \_ interactive EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) spécifie un type de réponse des informations d’identification.

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure du **\_ \_ REEE EAP cred** est utilisée pour prendre en charge l’authentification unique (SSO).

La structure du **\_ \_ REEE EAP cred** est identique à la structure de [**\_ \_ demande**](eap-cred-req.md) d’identification EAP.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures du demandeur EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**\_demande EAP cred \_**](eap-cred-req.md)
</dt> <dt>

[**demande d’expiration d’un \_ cred EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**réponse d’expiration d’un \_ cred EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**\_données de \_ l’interface utilisateur interactive EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO et PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

