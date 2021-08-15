---
description: Fournit les méthodes d’énumération COM-standard pour l’interface IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: IEnumPStoreItems, interface (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f5952dbaff2560ae4c2fc59af73246c2cd5c1d050bb53bc3c7b9091c8a39822f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542239"
---
# <a name="ienumpstoreitems-interface"></a>Interface IEnumPStoreItems

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fournit les méthodes d’énumération COM-standard pour l’interface [**IPStore**](ipstore.md) .

## <a name="members"></a>Membres

L’interface **IEnumPStoreItems** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreItems** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumPStoreItems** possède ces méthodes.



| Méthode                                  | Description                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Répliqué**](ienumpstoreitems-clone.md) | Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.<br/> |
| [**Suivant**](ienumpstoreitems-next.md)   | Obtient l’élément de données spécifié suivant dans la séquence d’énumération.<br/>                          |
| [**Initialisation**](ienumpstoreitems-reset.md) | Réinitialise au début de la séquence d’énumération.<br/>                                    |
| [**Saut**](ienumpstoreitems-skip.md)   | Ignore l’élément de données spécifié dans la séquence d’énumération.<br/>                              |



 

## <a name="remarks"></a>Remarques

Il est nécessaire de libérer chaque élément après l’avoir énuméré. L’objet énumérateur doit également être libéré lorsqu’il n’est plus utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
