---
title: Interface INapComponentConfig2 (NapCommon. h)
description: Fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système afin de configurer une interface utilisateur de serveur de stratégie réseau (NPS) à distance.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- NAP de l’interface INapComponentConfig2
- INapComponentConfig2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a80dfa1a9160b32b6d3c869795c9e23e41a5fdba39e38051bd29376caf8847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368373"
---
# <a name="inapcomponentconfig2-interface"></a>Interface INapComponentConfig2

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapComponentConfig2** fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système afin de configurer une interface utilisateur de serveur de stratégie réseau (NPS) à distance.

> [!Note]  
> Cette interface hérite de toutes les méthodes de [**INapComponentConfig**](inapcomponentconfig.md) et doit être utilisée à la place.

 

## <a name="members"></a>Membres

L’interface **INapComponentConfig2** hérite de [**INapComponentConfig**](inapcomponentconfig.md). **INapComponentConfig2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapComponentConfig2** possède ces méthodes.



| Méthode                                                                                                | Description                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig2::InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md)           | Implémenté par les validateurs d’intégrité du système pour gérer la configuration distante directement sur l’ordinateur spécifié.<br/>                                                                 |
| [**INapComponentConfig2::InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)   | Implémenté par les validateurs d’intégrité du système en fonction des besoins pour charger la configuration de l’ordinateur distant en mémoire et afficher une interface utilisateur qui permet la manipulation des données de configuration.<br/> |
| [**INapComponentConfig2::IsRemoteConfigSupported**](inapcomponentconfig2-isremoteconfigsupported.md) | Implémenté par les validateurs d’intégrité du système pour indiquer si la configuration distante est prise en charge.<br/>                                                                                      |



 

## <a name="remarks"></a>Remarques

Cette interface ne doit pas être implémentée par les agents d’intégrité système (SHA) ou les clients de contrainte de mise en quarantaine (QEC).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

 





