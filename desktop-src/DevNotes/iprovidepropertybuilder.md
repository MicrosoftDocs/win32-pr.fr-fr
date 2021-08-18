---
description: L’interface IProvidePropertyBuilder, lorsqu’elle est implémentée, permet aux objets de spécifier des objets de générateur de propriétés pour les propriétés.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Interface IProvidePropertyBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: d6d82cdafbf775c7316ed882cf3776aaf216fcb82938825d8c939f21e60cc0e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750019"
---
# <a name="iprovidepropertybuilder-interface"></a>Interface IProvidePropertyBuilder

L’interface **IProvidePropertyBuilder** , lorsqu’elle est implémentée, permet aux objets de spécifier des objets de générateur de propriétés pour les propriétés. les générateurs sont appelés par un bouton de sélection ( \[ ... \] ) dans l’explorateur de propriétés Microsoft Visual Studio et sont appelés via [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) quand le bouton est enfoncé. Pour fournir un générateur pour une propriété donnée, retournez un GUID pour le générateur de propriétés qui doit être appelé pour la propriété actuelle à partir de [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md). Les générateurs sont généralement implémentés par le biais de boîtes de dialogue modales.

La version de cette interface est 1,0. Les appels de méthode sont reçus au niveau d’un point de terminaison attribué dynamiquement (comme décrit dans la documentation binaire MSMQ sur le mappage de point de terminaison) et utilisent l’UUID (identificateur unique universel) « 33C0C1D8-33CF-11d3-BFF2-00C04F990235 ».

## <a name="members"></a>Membres

L’interface **IProvidePropertyBuilder : IUnknown** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IProvidePropertyBuilder** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IProvidePropertyBuilder : IUnknown** possède ces méthodes.



| Méthode                                                                       | Description                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md)             | Avertit un objet qu’il doit afficher son générateur pour la propriété spécifiée.<br/> |
| [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md) | Vérifie si un générateur doit être associé à une propriété particulière.<br/>         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



 

 
