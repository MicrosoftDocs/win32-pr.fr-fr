---
title: Méthode ISoftKbd ShowSoftKeyboard (Softkbdc. h)
description: La méthode ISoftKbd ShowSoftKeyboard affiche un clavier conditionnel.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- Infrastructure des services de texte de méthode ShowSoftKeyboard
- ShowSoftKeyboard méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode ShowSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032314"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a>ISoftKbd :: ShowSoftKeyboard, méthode

La méthode **ISoftKbd :: ShowSoftKeyboard** affiche un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iShow* \[ dans\]
</dt> <dd>

Entier indiquant le type de clavier logiciel à afficher.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                | Description                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | La méthode a réussi.<br/> |



 

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

 

 





