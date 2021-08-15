---
description: La fonction FilterAddObject ajoute un objet unique à un filtre d’affichage.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: FilterAddObject, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2c7d814efbbc77816836d437161390b1e2af60e8bbf4932322dcbd606920be5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938732"
---
# <a name="filteraddobject-function"></a>FilterAddObject fonction)

La fonction **FilterAddObject** ajoute un objet unique à un [*filtre d’affichage*](d.md).

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFilter* \[ dans\]
</dt> <dd>

Handle sur le filtre d’affichage.

</dd> <dt>

*lpFilterObject* \[ à\]
</dt> <dd>

Pointeur vers une structure [FILTEROBJECT](filterobject.md) qui définit l’objet à ajouter au filtre. Chaque objet peut être un opérateur, une valeur ou une propriété.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est un code d’erreur.



| Code de retour                                                                                              | Description                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_paramètre NMERR non valide \_**</dt> </dl> | La valeur du paramètre *hFilter* n’est pas valide.<br/>                     |
| <dl> <dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt> </dl>    | Moniteur réseau ne dispose pas de suffisamment de mémoire pour créer l’objet.<br/> |



 

## <a name="remarks"></a>Remarques

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **FilterAddObject** .

La fonction **FilterAddObject** est appelée chaque fois qu’un objet de filtre est ajouté au filtre d’affichage. Le filtre d’affichage est une pile suffixée d’objets qui peut être un opérateur, une valeur ou une propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[FILTEROBJECT](filterobject.md)
</dt> </dl>

 

 




