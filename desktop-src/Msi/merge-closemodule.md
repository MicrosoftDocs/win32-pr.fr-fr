---
description: la méthode CloseModule de l’objet merge (fusion) ferme le module de fusion Windows Installer actuellement ouvert.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Merge. CloseModule, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021349"
---
# <a name="mergeclosemodule-method"></a>Merge. CloseModule, méthode

la méthode **CloseModule** de l’objet [**merge (fusion**](merge-object.md) ) ferme le module de fusion Windows Installer actuellement ouvert.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fermeture d’un module de fusion n’affecte pas les erreurs qui n’ont pas été récupérées.

### <a name="c"></a>C++

Consultez fonction [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
