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
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540386"
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
| [**Language**](error-language.md)<br/>           | Retourne la langue de l’erreur.<br/>                                                |
| [**ModuleKeys**](error-modulekeys.md)<br/>       | Retourne les clés primaires de la ligne dans la table de module qui a provoqué l’erreur.<br/>   |
| [**ModuleTable**](error-moduletable.md)<br/>     | Retourne le nom de table de la table dans le module à l’origine de l’erreur.<br/>             |
| [**D**](error-path.md)<br/>                   | Retourne le chemin d’accès au fichier ou au répertoire à l’origine de l’erreur. Actuellement inutilisé.<br/>    |
| [**Entrer**](error-type.md)<br/>                   | Retourne le type d’erreur.<br/>                                                        |



 

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



 

 




