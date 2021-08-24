---
description: Fournit des méthodes COM-standard pour gérer les éléments de données de stockage protégés.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: IPStore, interface (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d6404d182a0c46de222b64892caa8b0e853610c980bfb79d286f781277493cba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749705"
---
# <a name="ipstore-interface"></a>Interface IPStore

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Cette interface peut être modifiée ou indisponible dans les futures versions de Windows.\]

Fournit des méthodes COM-standard pour gérer les éléments de données de stockage protégés. La méthode [**PStoreCreateInstance**](pstorecreateinstance.md) retourne un pointeur vers cette interface.

## <a name="members"></a>Membres

L’interface **IPStore** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IPStore** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IPStore** possède ces méthodes.



| Méthode                                                   | Description                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**CloseItem**](ipstore-closeitem.md)                   | Ferme un élément de données spécifié à partir du stockage protégé.<br/>                                                       |
| [**CreateSubtype**](ipstore-createsubtype.md)           | Crée le sous-type spécifié dans le type spécifié.<br/>                                                   |
| [**CreateType**](ipstore-createtype.md)                 | Crée le type spécifié avec le nom spécifié.<br/>                                                        |
| [**DeleteItem**](ipstore-deleteitem.md)                 | Supprime l’élément spécifié du stockage protégé.<br/>                                                     |
| [**DeleteSubtype**](ipstore-deletesubtype.md)           | Supprime le sous-type d’élément spécifié du stockage protégé.<br/>                                             |
| [**DeleteType**](ipstore-deletetype.md)                 | Supprime le type spécifié du stockage protégé.<br/>                                                     |
| [**EnumItems**](ipstore-enumitems.md)                   | Retourne le pointeur d’interface d’un sous-type pour l’énumération des éléments dans la base de données de stockage protégée.<br/>        |
| [**EnumSubtypes**](ipstore-enumsubtypes.md)             | Retourne une interface pour l’énumération des sous-types des types actuellement enregistrés dans la base de données protégée.<br/> |
| [**EnumTypes**](ipstore-enumtypes.md)                   | Retourne une interface pour énumérer les types actuellement enregistrés dans la base de données protégée.<br/>             |
| [**GetInfo**](ipstore-getinfo.md)                       | Récupère des informations sur le fournisseur de stockage.<br/>                                                          |
| [**GetProvParam**](ipstore-getprovparam.md)             | Non implémenté.<br/>                                                                                           |
| [**GetSubtypeInfo**](ipstore-getsubtypeinfo.md)         | Récupère les informations associées à un sous-type.<br/>                                                           |
| [**GetTypeInfo**](ipstore-gettypeinfo.md)               | Récupère les informations associées à un type.<br/>                                                              |
| [**OpenItem**](ipstore-openitem.md)                     | Ouvre un élément pour plusieurs accès.<br/>                                                                       |
| [**ReadAccessRuleSet**](ipstore-readaccessruleset.md)   | Non implémenté.<br/>                                                                                           |
| [**ReadItem**](ipstore-readitem.md)                     | Lit l’élément de données spécifié à partir du stockage protégé.<br/>                                                      |
| [**SetProvParam**](ipstore-setprovparam.md)             | Définit les informations de paramètre spécifiées.<br/>                                                                  |
| [**WriteAccessRuleset**](ipstore-writeaccessruleset.md) | Non implémenté.<br/>                                                                                           |
| [**WriteItem**](ipstore-writeitem.md)                   | Écrit un élément de données dans le stockage protégé.<br/>                                                                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
