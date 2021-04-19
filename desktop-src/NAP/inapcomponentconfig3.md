---
title: Interface INapComponentConfig3 (NapCommon. h)
description: Fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système (SHV) afin de définir et de modifier les données de configuration d’un ID de configuration spécifique.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- NAP de l’interface INapComponentConfig3
- INapComponentConfig3 interface NAP, Description
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510304"
---
# <a name="inapcomponentconfig3-interface"></a>Interface INapComponentConfig3

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapComponentConfig3** fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système (SHV) afin de définir et de modifier les données de configuration d’un ID de configuration spécifique.

> [!Note]  
> Cette interface hérite de toutes les méthodes de [**INapComponentConfig2**](inapcomponentconfig2.md) et doit être utilisée à la place.

 

## <a name="members"></a>Membres

L’interface **INapComponentConfig3** hérite de [**INapComponentConfig2**](inapcomponentconfig2.md). **INapComponentConfig3** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapComponentConfig3** possède ces méthodes.



| Méthode                                                                                | Description                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3 ::D eleteAllConfig**](inapcomponentconfig3-deleteallconfig.md) | Implémenté par les validateurs d’intégrité du système pour fournir un moyen de réinitialiser le magasin SHV à son état d’origine après l’installation.<br/>      |
| [**INapComponentConfig3 ::D eleteConfig**](inapcomponentconfig3-deleteconfig.md)       | Implémenté par les validateurs d’intégrité du système pour fournir un moyen de supprimer des données de configuration pour un ID de configuration spécifique.<br/>  |
| [**INapComponentConfig3::GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md) | Implémenté par les validateurs d’intégrité du système pour fournir un moyen d’obtenir des données de configuration pour un ID de configuration spécifique.<br/>  |
| [**INapComponentConfig3 :: NewConfig**](inapcomponentconfig3-newconfig.md)             | Implémenté par les validateurs d’intégrité du système pour fournir un moyen de créer des données de configuration pour un ID de configuration spécifique.<br/>  |
| [**INapComponentConfig3::SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)     | Implémenté par les validateurs d’intégrité du système pour fournir un moyen de définir les données de configuration pour un ID de configuration spécifique.<br/> |



 

## <a name="remarks"></a>Notes

Cette interface ne doit pas être implémentée par les agents d’intégrité système (SHA) ou les clients de contrainte de mise en quarantaine (QEC).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

 





