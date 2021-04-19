---
description: La méthode OpenDatabase de l’objet Merge ouvre une base de données d’installation Windows Installer, située dans un chemin d’accès spécifié, qui doit être fusionnée avec un module.
ms.assetid: 86f168e5-bc76-476d-9757-9b2a21bb9c4b
title: Merge. OpenDatabase, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenDatabase
- IMsmMerge.OpenDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 2e200da6fe3f4913e53d96a237cac2b4d4c9b77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537811"
---
# <a name="mergeopendatabase-method"></a>Merge. OpenDatabase, méthode

La méthode **OpenDatabase** de l’objet [**Merge**](merge-object.md) ouvre une base de données d’installation Windows Installer, située dans un chemin d’accès spécifié, qui doit être fusionnée avec un module.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.OpenDatabase(
  Path
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* 
</dt> <dd>

Chemin d’accès à la base de données en cours d’ouverture.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="c"></a>C++

Consultez fonction [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
