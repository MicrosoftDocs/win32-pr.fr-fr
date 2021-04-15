---
title: Interface INapServerCallback (NapSystemHealthValidator. h)
description: Les validateurs d’intégrité utilisent pour signaler la fin de la requête asynchrone.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- NAP de l’interface INapServerCallback
- INapServerCallback interface NAP, Description
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464342"
---
# <a name="inapservercallback-interface"></a>Interface INapServerCallback

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

**INapServerCallback** fournit une méthode que les validateurs d’intégrité du système utilisent pour signaler la fin de la requête asynchrone.

## <a name="members"></a>Membres

L’interface **INapServerCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapServerCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapServerCallback** possède ces méthodes.



| Méthode                                                                         | Description                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapServerCallback :: OnComplete**](inapservercallback-oncomplete-method.md) | Utilisé par les validateurs d’intégrité du système pour signaler la fin de la requête asynchrone.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

