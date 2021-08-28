---
description: Interface IEnumPStoreTypes-fournit des méthodes d’énumération COM pour l’interface IPStore.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: IEnumPStoreTypes, interface (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 668ed2b7177344004cb4b872ff47a5924fdcc1778cfbfbb3c6d3d447b624546c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955958"
---
# <a name="ienumpstoretypes-interface"></a>Interface IEnumPStoreTypes

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fournit des méthodes d’énumération COM standard pour l’interface [**IPStore**](ipstore.md) .

## <a name="members"></a>Membres

L’interface **IEnumPStoreTypes** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreTypes** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumPStoreTypes** possède ces méthodes.



| Méthode                                  | Description                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Répliqué**](ienumpstoretypes-clone.md) | Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.<br/> |
| [**Suivant**](ienumpstoretypes-next.md)   | Obtient le type de fournisseur spécifié suivant dans la séquence d’énumération.<br/>                      |
| [**Initialisation**](ienumpstoretypes-reset.md) | Réinitialise au début de la séquence d’énumération.<br/>                                    |
| [**Saut**](ienumpstoretypes-skip.md)   | Ignore le type de fournisseur spécifié dans la séquence d’énumération.<br/>                          |



 

## <a name="remarks"></a>Remarques

L’objet énumérateur doit être libéré lorsqu’il n’est plus utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
