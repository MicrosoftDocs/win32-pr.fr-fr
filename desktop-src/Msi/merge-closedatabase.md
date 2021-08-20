---
description: la méthode fermerbase de l’objet Merge ferme la base de données Windows Installer actuellement ouverte.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Merge. FermerBase, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3f3b250cbaebd565f14ef7f10cd8180e497f20347d00a7e96a74298d3e5dc770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013027"
---
# <a name="mergeclosedatabase-method"></a>Merge. FermerBase, méthode

la méthode **fermerbase** de l’objet [**Merge**](merge-object.md) ferme la base de données Windows Installer actuellement ouverte.

## <a name="syntax"></a>Syntaxe


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bCommit* 
</dt> <dd>

**True** si les modifications doivent être enregistrées ; sinon, **false** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La fermeture d’une base de données efface toutes les informations de dépendance, mais n’affecte pas les erreurs qui n’ont pas été récupérées.

### <a name="c"></a>C++

Consultez la fonction [**FermerBase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
