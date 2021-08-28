---
description: Interface IEnumPStoreProviders-fournit des méthodes d’énumération COM pour l’interface IPStore.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: IEnumPStoreProviders, interface (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: eb73345dd594f3583b4a6cfbc6e0462848d85de0e9470e6bc8177574a2fff20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017707"
---
# <a name="ienumpstoreproviders-interface"></a>Interface IEnumPStoreProviders

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fournit des méthodes d’énumération COM standard pour l’interface [**IPStore**](ipstore.md) .

## <a name="members"></a>Membres

L’interface **IEnumPStoreProviders** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreProviders** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumPStoreProviders** possède ces méthodes.



| Méthode                                      | Description                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Répliqué**](ienumpstoreproviders-clone.md) | Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.<br/> |
| [**Suivant**](ienumpstoreproviders-next.md)   | Obtient le fournisseur spécifié suivant dans la séquence d’énumération.<br/>                           |
| [**Initialisation**](ienumpstoreproviders-reset.md) | Réinitialise au début de la séquence d’énumération.<br/>                                    |
| [**Saut**](ienumpstoreproviders-skip.md)   | Ignore le fournisseur spécifié dans la séquence d’énumération.<br/>                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
