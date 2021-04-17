---
title: Méthode ISoftKbd ShowKeysForKeyScanMode (Softkbdc. h)
description: La méthode ISoftKbd ShowKeysForKeyScanMode affiche les clés utilisées pour le mode d’analyse de clé pour un clavier conditionnel.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Infrastructure des services de texte de méthode ShowKeysForKeyScanMode
- ShowKeysForKeyScanMode méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode ShowKeysForKeyScanMode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466299"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>ISoftKbd :: ShowKeysForKeyScanMode, méthode

La méthode **ISoftKbd :: ShowKeysForKeyScanMode** affiche les clés utilisées pour le mode d’analyse de clé pour un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpKeyID* \[ dans\]
</dt> <dd>

Pointeur vers un tableau d’éléments KEYID indiquant les identificateurs des clés à afficher.

</dd> <dt>

*iKeyNum* \[ dans\]
</dt> <dd>

Nombre de clés à afficher.

</dd> <dt>

*fHighL* \[ dans\]
</dt> <dd>

TRUE si la méthode doit mettre en surbrillance les clés et **false** dans le cas contraire.

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

 

 





