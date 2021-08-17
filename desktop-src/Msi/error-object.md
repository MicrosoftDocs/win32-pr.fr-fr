---
description: L’objet Error retourne les informations d’une erreur de fusion unique.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Objet Error (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 237cf88b2830bf210e84d016b52b7fd0b0183c0c0072ac8f654663e2cd3c12dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947030"
---
# <a name="error-object"></a>Objet d’erreur

L’objet **Error** retourne les informations d’une erreur de fusion unique.

## <a name="members"></a>Membres

L’objet **Error** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **Error** a ces propriétés.



| Propriété                                                | Description                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**DatabaseKeys**](error-databasekeys.md)<br/>   | Retourne les clés primaires de la ligne dans la table de base de données qui a provoqué l’erreur.<br/> |
| [**DatabaseTable**](error-databasetable.md)<br/> | Retourne le nom de table de la table dans la base de données à l’origine de l’erreur.<br/>           |
| [**Langage**](error-language.md)<br/>           | Retourne la langue de l’erreur.<br/>                                                |
| [**ModuleKeys**](error-modulekeys.md)<br/>       | Retourne les clés primaires de la ligne dans la table de module qui a provoqué l’erreur.<br/>   |
| [**ModuleTable**](error-moduletable.md)<br/>     | Retourne le nom de table de la table dans le module à l’origine de l’erreur.<br/>             |
| [**Chemin**](error-path.md)<br/>                   | Retourne le chemin d’accès au fichier ou au répertoire à l’origine de l’erreur. Actuellement inutilisé.<br/>    |
| [**Type**](error-type.md)<br/>                   | Retourne le type d’erreur.<br/>                                                        |



 

## <a name="c"></a>C++

interface **IMsmError : IDispatch**

## <a name="interface-id"></a>ID d’interface



| Constante           | Valeur                                  |
|--------------------|----------------------------------------|
| **IID \_ IMsmError** | {0ADDA828-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




