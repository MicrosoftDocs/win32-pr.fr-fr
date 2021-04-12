---
title: Méthode ISoftKbd GetSoftKeyboardPosSize (Softkbdc. h)
description: La méthode ISoftKbd GetSoftKeyboardPosSize récupère la position de départ et la taille d’un clavier conditionnel.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Infrastructure des services de texte de méthode GetSoftKeyboardPosSize
- GetSoftKeyboardPosSize méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode GetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317341"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a>ISoftKbd :: GetSoftKeyboardPosSize, méthode

La méthode **ISoftKbd :: GetSoftKeyboardPosSize** récupère la position de départ et la taille d’un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpStartPoint* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette méthode récupère une structure de [points](/previous-versions//dd162805(v=vs.85)) indiquant les coordonnées de la position supérieure gauche du clavier conditionnel.

</dd> <dt>

*lpwidth* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette méthode récupère la largeur du clavier conditionnel.

</dd> <dt>

*lpheight* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette méthode récupère la hauteur du clavier conditionnel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L’un des paramètres n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

