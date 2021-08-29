---
description: Définit la liste des ID de groupe persistants pour tous les profils qui sont rendus persistants par votre application.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: WFDDisplaySinkSetPersistedGroupIDList, fonction (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: ce31b6e4bf6336baede3767d3457f44d92dde0e39f6418bcc3c2529b644fe24c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800389"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a>WFDDisplaySinkSetPersistedGroupIDList fonction)

Définit la liste des ID de groupe persistants pour tous les profils qui sont rendus persistants par votre application. Votre application doit appeler cette méthode chaque fois qu’elle ajoute ou supprime un profil de son stockage.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cGroupIDList* \[ dans\]
</dt> <dd>

Nombre d’ID de groupe pointés par *pGroupIDList*.

</dd> <dt>

*pGroupIDList* \[ dans\]
</dt> <dd>

Pointeur vers un tableau d’ID de groupe *cGroupIDList* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

## <a name="remarks"></a>Remarques

Cette méthode est toujours supposée être appelée avec la liste entière, et non comme un sous-ensemble. Il est OK d’appeler cette méthode avec 0 Profile lorsque le magasin de profils est vide.

Un nouvel appel pour un ID de groupe qui ne fait pas partie de la liste fournie échoue avec «Fail ; Groupe P2P inconnu» (État 8).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows 10<br/>                                                                      |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2016<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




