---
title: Constantes EAPHost (Eaptypes. h)
description: Affichez la liste des constantes EAPHost (Eaptypes. h) utilisées par les méthodes EAPHost et consultez les conditions requises pour leur utilisation.
ms.assetid: 56338B98-06E3-4CD3-B1CA-F8F45AA39566
topic_type:
- apiref
api_name:
- EAP_INTERACTIVE_UI_DATA_VERSION
- EAP_CREDENTIAL_VERSION
- EAPHOST_PEER_API_VERSION
- CERTIFICATE_HASH_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH
- EAP_UI_INPUT_FIELD_PROPS_DEFAULT
- EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT
- EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST
- EAP_UI_INPUT_FIELD_PROPS_READ_ONLY
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84704e59ed43466c47435f4804cb4dedc9c3a92d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382831"
---
# <a name="eaphost-constants"></a>Constantes EAPHost

Constantes utilisées par les méthodes EAPHost.

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**\_version des \_ données de l’interface utilisateur interactive EAP \_ \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Version des données de l’interface utilisateur interactive EAP.


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**\_version des informations d’identification EAP \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Version des informations d’identification EAP fournies par l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**VERSION de l' \_ API homologue EAPHOST \_ \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Version de l’API homologue EAPHost.


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**\_longueur du hachage du certificat \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Longueur du hachage SHA1 du certificat.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**\_longueur maximale \_ du \_ champ d’entrée de configuration EAP \_ \_**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



Spécifie la longueur maximale prise en charge d’un champ d’entrée.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**longueur maximale de la \_ \_ \_ valeur du champ d’entrée de configuration \_ EAP \_ \_**
</dt> <dd> <dl> <dt>

1 024
</dt> <dt>



Spécifie la longueur maximale prise en charge d’un champ d’entrée.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**\_ \_ \_ \_ \_ valeurs par défaut des propriétés d’entrée de l’interface utilisateur EAP**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Windows Vista avec SP1 ou version ultérieure : représente la valeur de propriété par défaut pour les entrées de champ d’entrée affichées dans l’interface utilisateur.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**\_ \_ \_ \_ \_ valeurs par défaut des propriétés d’entrée de configuration EAP**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Représente la valeur de propriété par défaut pour les entrées de champ d’entrée de configuration affichées dans l’interface utilisateur.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**\_Propriétés du \_ champ d’entrée EAP UI \_ \_ \_ non \_ affichables**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Windows Vista avec SP1 ou version ultérieure : spécifie que les entrées du champ d’entrée ne seront pas affichées dans l’interface utilisateur (par exemple, un mot de passe ou un code confidentiel).


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**\_Propriétés du \_ champ d’entrée de configuration EAP \_ \_ \_ non \_ affichables**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Spécifie que les entrées du champ d’entrée de configuration ne seront pas affichées dans l’interface utilisateur (un mot de passe ou un numéro de code confidentiel, par exemple).


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**\_Propriétés du champ d’entrée de l’interface utilisateur EAP \_ \_ \_ \_ non \_ persistantes**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



Windows Vista SP1 (ou version ultérieure) : indique que la méthode EAP ne met pas en cache les données de champ ; le demandeur doit mettre en cache les données de champ pour l’itinérance.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**\_Propriétés du \_ champ d’entrée EAP UI \_ \_ \_ en lecture \_ seule**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Windows Vista avec SP1 ou version ultérieure : indique que le champ d’entrée est en lecture seule et ne peut pas être modifié.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/> |
| Serveur<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/> |



 

 





