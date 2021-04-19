---
description: La méthode Connect de l’objet Merge connecte un module à une fonctionnalité supplémentaire. Le module doit avoir déjà été fusionné dans la base de données ou sera fusionné dans la base de données. La fonctionnalité doit exister avant d’appeler cette fonction.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Merge. Connect, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543796"
---
# <a name="mergeconnect-method"></a>Merge. Connect, méthode

La méthode **Connect** de l’objet [**Merge**](merge-object.md) connecte un module à une fonctionnalité supplémentaire. Le module doit avoir déjà été fusionné dans la base de données ou sera fusionné dans la base de données. La fonctionnalité doit exister avant d’appeler cette fonction.

Les modifications apportées à la base de données ne sont pas enregistrées sur le disque, sauf si la méthode [**FermerBase**](merge-closedatabase.md) est appelée avec *BCommit* défini sur **true**.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Fonctionnalité* 
</dt> <dd>

Nom d’une fonctionnalité déjà existante dans la base de données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les erreurs peuvent être récupérées par le biais de la propriété [**Errors**](merge-errors.md) . Les erreurs et les messages d’information sont publiés dans le fichier journal actuel.

### <a name="c"></a>C++

Consultez [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) , fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
