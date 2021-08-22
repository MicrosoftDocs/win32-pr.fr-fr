---
title: gluQuadricCallback, fonction (Glu. h)
description: La fonction gluQuadricCallback définit un rappel pour un objet quadric.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- gluQuadricCallback fonction OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ce32bf041a59f272b18ebe17916963c4e5fd8d208da9d739468c88b9286dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488789"
---
# <a name="gluquadriccallback-function"></a>gluQuadricCallback fonction)

La fonction **gluQuadricCallback** définit un rappel pour un objet quadric.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*qobj* 
</dt> <dd>

Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*et* 
</dt> <dd>

Rappel en cours de définition. La seule valeur valide est GLU \_ Error.



| Valeur                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <dt>**\_erreur Glu**</dt> </dl> | La fonction **gluQuadricCallback** est appelée lorsqu’une erreur est rencontrée. Son argument unique est de type **GLenum** et indique l’erreur spécifique qui s’est produite. Les chaînes de caractères décrivant ces erreurs peuvent être récupérées avec l’appel [**gluErrorString**](gluerrorstring.md) .<br/> |



 

</dd> <dt>

*FN* 
</dt> <dd>

Fonction à appeler.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Utilisez **gluQuadricCallback** pour définir un nouveau rappel devant être utilisé par un objet quadric. Si le rappel spécifié est déjà défini, il est remplacé. Si *FN* a la **valeur null**, tous les rappels existants sont effacés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





