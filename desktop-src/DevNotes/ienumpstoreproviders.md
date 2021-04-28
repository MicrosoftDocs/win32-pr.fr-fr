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
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089347"
---
# <a name="ienumpstoreproviders-interface"></a>Interface IEnumPStoreProviders

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fournit des méthodes d’énumération COM standard pour l’interface [**IPStore**](ipstore.md) .

## <a name="members"></a>Membres

L’interface **IEnumPStoreProviders** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreProviders** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumPStoreProviders** possède ces méthodes.



| Méthode                                      | Description                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumpstoreproviders-clone.md) | Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.<br/> |
| [**Suivant**](ienumpstoreproviders-next.md)   | Obtient le fournisseur spécifié suivant dans la séquence d’énumération.<br/>                           |
| [**Réinitialiser**](ienumpstoreproviders-reset.md) | Réinitialise au début de la séquence d’énumération.<br/>                                    |
| [**Saut**](ienumpstoreproviders-skip.md)   | Ignore le fournisseur spécifié dans la séquence d’énumération.<br/>                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
