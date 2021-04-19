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
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528751"
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
| [**Language**](dependency-language.md)<br/> | Retourne la langue du module.<br/>           |
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



 

 




