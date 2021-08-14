---
description: dans Windows Installer versions 1,0 et 1,1, la propriété Path est toujours la chaîne vide. Les versions ultérieures peuvent utiliser cette valeur pour retourner le chemin d’accès au fichier ou au répertoire qui n’a pas pu être créé.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Error. Path, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7787fcd5bad5550b933b2a866308c1d5b77dd24f60fce23ebc3b227829528307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378150"
---
# <a name="errorpath-property"></a>Error. Path, propriété

dans Windows Installer versions 1,0 et 1,1, la propriété Path est toujours la chaîne vide. Les versions ultérieures peuvent utiliser cette valeur pour retourner le chemin d’accès au fichier ou au répertoire qui n’a pas pu être créé.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Error.Path
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Cette valeur est valide uniquement pour les erreurs de type msmErrorFileCreate ou msmErrorDirCreate. Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .

### <a name="c"></a>C++

Consultez la fonction [**obtenir le \_ chemin**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

