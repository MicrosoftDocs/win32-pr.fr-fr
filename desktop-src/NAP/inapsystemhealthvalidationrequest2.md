---
title: Interface INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Fournit des méthodes qui sont utilisées pour prendre en charge les validateurs d’intégrité du système qui sont définis par le développeur de l’application.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- NAP de l’interface INapSystemHealthValidationRequest2
- INapSystemHealthValidationRequest2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513044"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>Interface INapSystemHealthValidationRequest2

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapSystemHealthValidationRequest2** fournit des méthodes qui sont utilisées pour prendre en charge les validateurs d’intégrité du système qui sont définis par le développeur de l’application.

> [!Note]  
> Cette interface hérite de toutes les méthodes de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) et doit être utilisée à la place.

 

## <a name="members"></a>Membres

L’interface **INapSystemHealthValidationRequest2** hérite de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md). **INapSystemHealthValidationRequest2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapSystemHealthValidationRequest2** possède ces méthodes.



| Méthode                                                                                                    | Description                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2::GetConfigId**](inapsystemhealthvalidationrequest2-getconfigid.md) | Récupère l’ID de configuration dans une demande de validation.<br/> |



 

## <a name="remarks"></a>Notes

Si un SHV ne prend pas en charge [**INapComponentConfig3**](inapcomponentconfig3.md), cette interface ne s’applique pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

 





