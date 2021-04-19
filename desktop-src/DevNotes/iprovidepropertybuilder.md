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
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520812"
---
# <a name="iprovidepropertybuilder-interface"></a>Interface IProvidePropertyBuilder

L’interface **IProvidePropertyBuilder** , lorsqu’elle est implémentée, permet aux objets de spécifier des objets de générateur de propriétés pour les propriétés. Les générateurs sont appelés par un bouton de sélection ( \[ ... \] ) dans l’Explorateur de propriétés Microsoft Visual Studio et sont appelés via [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) quand le bouton est enfoncé. Pour fournir un générateur pour une propriété donnée, retournez un GUID pour le générateur de propriétés qui doit être appelé pour la propriété actuelle à partir de [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md). Les générateurs sont généralement implémentés par le biais de boîtes de dialogue modales.

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



 

 
