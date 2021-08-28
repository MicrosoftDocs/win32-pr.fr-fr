---
description: Fournit l’accès aux propriétés de l’objet de contexte qui sont liées aux transactions.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Interface IContextTransactionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: be470d2a06d5dc284963e76ded188cb6a11fabd963b4f1186a3cee697bdfb6df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793449"
---
# <a name="icontexttransactioninfo-interface"></a>Interface IContextTransactionInfo

Fournit l’accès aux propriétés de l’objet de contexte qui sont liées aux transactions.

## <a name="when-to-implement"></a>Quand implémenter

Vous ne devez pas implémenter cette interface. L’implémentation standard fournit des fonctionnalités complètes.

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette interface pour accéder aux propriétés de l’objet de contexte qui sont liées aux transactions.

## <a name="members"></a>Membres

L’interface **IContextTransactionInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextTransactionInfo** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IContextTransactionInfo** possède ces méthodes.



| Méthode                                                                                         | Description                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**FetchTransaction**](icontexttransactioninfo-registertransactionproxy.md)                   | Récupère la transaction ou le proxy de transaction associé au contexte actuel, le cas échéant.<br/>              |
| [**GetTxIsolationLevelAndTimeout**](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | Récupère le niveau d’isolation et la valeur de délai d’attente d’une transaction qui est hébergée dans le contexte de transaction racine.<br/> |
| [**RegisterTransactionProxy**](icontexttransactioninfo-fetchtransaction.md)                   | Associe une implémentation de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) avec le contexte actuel.<br/>            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/> |



 

