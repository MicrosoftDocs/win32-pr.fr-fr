---
description: Type de données utilisé pour spécifier les attributs d’accès de sécurité dans le registre.
title: REGSAM (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235205"
---
# <a name="regsam"></a>REGSAM

Type de données utilisé pour spécifier les attributs d’accès de sécurité dans le registre.



| Constante                                                                                                                                                                                   | Description                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**\_tout \_ accéder à la clé**</dt> </dl>                          | Combinaison de * * * * valeur de requête de clé \_ \_ * * * *, * * * * clé d' \_ énumération des \_ sous- \_ clés * * \_ \_ \_ \_ \_ \_ \_ * * * * \_ * * * clé de notification * * * * * * * * * clé de création de sous-clé * * * * * * * * * * clé de jeu de clés * * * * accès.<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**\_lien de création de clé \_**</dt> </dl>                       | Autorisation de créer un lien symbolique.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**CLÉ \_ créer une \_ sous- \_ clé**</dt> </dl>             | Autorisation de créer des sous-clés.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**CLÉ \_ énumérer les \_ sous- \_ clés**</dt> </dl> | Autorisation d’énumérer les sous-clés.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**exécution de la clé \_**</dt> </dl>                                    | Autorisation pour l’accès en lecture.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**CLÉ de \_ notification**</dt> </dl>                                       | Autorisation pour la notification de modification.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**\_valeur de requête de clé \_**</dt> </dl>                       | Autorisation d’interroger les données de la sous-clé.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**lecture de la clé \_**</dt> </dl>                                             | Combinaison de * * * * valeur de requête de clé \_ \_ * * * *, * * * * clé \_ énumérer \_ les sous- \_ clés * * * * et * * * * clé de \_ notification * * * * * accès.<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**\_valeur du jeu de clés \_**</dt> </dl>                             | Autorisation de définir des données de sous-clé.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**écriture de clé \_**</dt> </dl>                                          | Combinaison de * * * * \_ valeur de jeu de clés \_ * * * * et * * * * clé \_ Create \_ Sub \_ Key * * * * Access.<br/>                                                                                                                |



## <a name="remarks"></a>Notes

Une valeur **REGSAM** peut être une ou plusieurs des valeurs listées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

 




