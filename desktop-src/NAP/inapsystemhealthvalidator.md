---
title: Interface INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Doit être implémentée par les développeurs SHV pour permettre au système NAP de communiquer avec un SHV.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- NAP de l’interface INapSystemHealthValidator
- INapSystemHealthValidator interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110617"
---
# <a name="inapsystemhealthvalidator-interface"></a>Interface INapSystemHealthValidator

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

**INapSystemHealthValidator** fournit des méthodes qui doivent être implémentées par les développeurs SHV pour permettre au système NAP de communiquer avec un SHV.

## <a name="members"></a>Membres

L’interface **INapSystemHealthValidator** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthValidator** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapSystemHealthValidator** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidator :: Validate**](inapsystemhealthvalidator-validate-method.md) | Le système NAP appelle cette méthode définie par l’application pour valider les [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) reçus d’un client. <br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

