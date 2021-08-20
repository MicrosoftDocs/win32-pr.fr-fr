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
ms.openlocfilehash: 83f0238a1e65a6c3551b7fea5262fe91d74705287aba0714dfbb4b3cc3a37976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805050"
---
# <a name="mergeclosemodule-method"></a>Merge. CloseModule, méthode

la méthode **CloseModule** de l’objet [**merge (fusion**](merge-object.md) ) ferme le module de fusion Windows Installer actuellement ouvert.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fermeture d’un module de fusion n’affecte pas les erreurs qui n’ont pas été récupérées.

### <a name="c"></a>C++

Consultez fonction [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
