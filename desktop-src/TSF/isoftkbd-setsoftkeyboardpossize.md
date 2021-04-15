---
title: Méthode ISoftKbd SetSoftKeyboardPosSize (Softkbdc. h)
description: La méthode ISoftKbd SetSoftKeyboardPosSize définit la position de départ et la taille d’un clavier conditionnel.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Infrastructure des services de texte de méthode SetSoftKeyboardPosSize
- SetSoftKeyboardPosSize méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466302"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a>ISoftKbd :: SetSoftKeyboardPosSize, méthode

La méthode **ISoftKbd :: SetSoftKeyboardPosSize** définit la position de départ et la taille d’un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartPoint* \[ dans\]
</dt> <dd>

Structure de [points](/previous-versions//dd162805(v=vs.85)) indiquant les coordonnées de la position supérieure gauche du clavier conditionnel.

</dd> <dt>

*largeur* \[ dans\]
</dt> <dd>

Largeur du clavier conditionnel.

</dd> <dt>

*hauteur* \[ dans\]
</dt> <dd>

Hauteur du clavier conditionnel.

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
</dt> </dl>

 

