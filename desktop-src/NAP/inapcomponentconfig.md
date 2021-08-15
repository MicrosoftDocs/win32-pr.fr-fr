---
title: Interface INapComponentConfig (NapCommon. h)
description: Fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système (SHV).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- NAP de l’interface INapComponentConfig
- INapComponentConfig interface NAP, Description
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a1c61b3681178089b0cda813155f3629caa233a7995d28cee22b1f65754ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800021"
---
# <a name="inapcomponentconfig-interface"></a>Interface INapComponentConfig

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapComponentConfig** fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système (SHV).

> [!Note]  
> [**INapComponentConfig2**](inapcomponentconfig2.md) et [**INapComponentConfig3**](inapcomponentconfig3.md) héritent de toutes les méthodes de cette interface et doivent être utilisés à la place.

 

## <a name="members"></a>Membres

L’interface **INapComponentConfig** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapComponentConfig** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapComponentConfig** possède ces méthodes.



| Méthode                                                                          | Description                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**INapComponentConfig :: GetConfig**](inapcomponentconfig-getconfig.md)         | Récupère la configuration du composant SHV.<br/>                                |
| [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)           | Lance l’interface utilisateur personnalisée pour un composant SHV.<br/>              |
| [**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md) | Spécifie si le composant SHV prend en charge une interface utilisateur personnalisée.<br/> |
| [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)         | Définit la configuration du composant SHV.<br/>                                     |



 

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

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

