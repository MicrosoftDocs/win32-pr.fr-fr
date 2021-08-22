---
description: Les constantes suivantes sont utilisées par PStore.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Constantes PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 69a82241e8f270389c5385143e83973d380f5671e30e2086749a75c984670cf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386039"
---
# <a name="pstore-constants"></a>Constantes PStore

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Les constantes suivantes sont utilisées par PStore.

Codes d’erreur Stockage protégés



| Constante/valeur                                                                                                                                                                                                                               | Description                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <dt>**Fichier PST \_ E \_ OK**</dt> <dt>0x00000000L</dt> </dl>                             | L'opération a réussi.<br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <dt>**Fichier PST \_ Le \_ type E \_ existe**</dt> <dt>0x800C0004L</dt> </dl> | L’élément de données existe déjà dans le stockage protégé. <br/> |



Valeurs de clause d’accès



| Constante/valeur                                                                                                                                                                                                                                      | Description                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <dt>**Fichier PST \_ AUTHENTICODE**</dt> <dt>1</dt> </dl>                       | Pointe vers une [**structure \_ AUTHENTICODEDATA PST**](pst-authenticodedata.md) .<br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <dt> **\_ \_ Vérification binaire PST**</dt> <dt>2</dt> </dl>                   | Pointe vers une **structure \_ BINARYCHECKDATA PST** .<br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <dt>**Fichier PST \_ \_Descripteur de sécurité**</dt> <dt>4</dt> </dl> | pointe vers un descripteur de sécurité Windows valide. <br/>                              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
