---
description: L’objet de dépendance retourne un module dont dépend le module en cours et qui n’a pas encore été fusionné dans la base de données d’installation actuelle.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Objet de dépendance (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: ac5786dcf3d4818fdfb3f0458cbfa85c923e5200ae69b5cb93d38330c322abf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378888"
---
# <a name="dependency-object"></a>Objet de dépendance

L’objet de **dépendance** retourne un module dont dépend le module en cours et qui n’a pas encore été fusionné dans la base de données d’installation actuelle.

## <a name="members"></a>Membres

L’objet de **dépendance** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet de **dépendance** possède ces propriétés.



| Propriété                                           | Description                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Langage**](dependency-language.md)<br/> | Retourne la langue du module.<br/>           |
| [**Module**](dependency-module.md)<br/>     | Retourne l’ID du module requis.<br/> |
| [**Version**](dependency-version.md)<br/>   | Retourne la version du module requis.<br/>   |



 

## <a name="c"></a>C++

interface **IMsmDependency : IDispatch**

## <a name="interface-id"></a>ID d’interface



| Constante                | Valeur                                  |
|-------------------------|----------------------------------------|
| **IID \_ IMsmDependency** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




