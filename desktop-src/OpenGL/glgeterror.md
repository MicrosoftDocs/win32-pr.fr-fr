---
title: fonction glGetError (GL. h)
description: La fonction glGetError retourne des informations sur l’erreur.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- glGetError fonction OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229523"
---
# <a name="glgeterror-function"></a>glGetError fonction)

La fonction **glGetError** retourne des informations sur l’erreur.

## <a name="syntax"></a>Syntaxe


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

La fonction **glGetError** retourne l’un des codes d’erreur suivants.



| Code de retour                                                                                           | Description                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | Une valeur inacceptable est spécifiée pour un argument énuméré. La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.<br/>         |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | Un argument numérique est hors limites. La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.<br/>                                    |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | L’opération spécifiée n’est pas autorisée dans l’état actuel. La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.<br/>           |
| <dl> <dt>**GL- \_ aucune \_ erreur**</dt> </dl>          | Aucune erreur n’a été enregistrée. La valeur de cette constante symbolique est garantie égale à zéro.<br/>                                                                         |
| <dl> <dt>**dépassement de capacité de la \_ pile GL \_**</dt> </dl>    | Cette fonction provoquerait un dépassement de capacité de la pile. La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.<br/>                            |
| <dl> <dt>**DÉPASSEMENT de capacité de la \_ pile GL \_**</dt> </dl>   | Cette fonction provoque un dépassement de capacité négatif de la pile. La fonction incriminée est ignorée, ce qui n’a aucun effet secondaire que de définir l’indicateur d’erreur.<br/>                           |
| <dl> <dt>**\_mémoire insuffisante \_ du GL \_**</dt> </dl>    | Il n’y a pas assez de mémoire pour exécuter la fonction. L’état de OpenGL n’est pas défini, à l’exception de l’état des indicateurs d’erreur, après l’enregistrement de cette erreur.<br/> |



 

Notez que **glGetError** retourne \_ une opération GL non valide \_ si elle est appelée entre un appel à [**glBegin**](glbegin.md) et son appel correspondant à [**glEnd**](glend.md).

## <a name="remarks"></a>Notes

Chaque erreur détectable est assignée à un code numérique et à un nom symbolique. Lorsqu’une erreur se produit, l’indicateur d’erreur est défini sur la valeur de code d’erreur appropriée. Aucune autre erreur n’est enregistrée tant que **glGetError** n’est pas appelé, le code d’erreur est retourné et l’indicateur est réinitialisé sur GL \_ no \_ Error. Si un appel à **glGetError** retourne GL \_ no \_ Error, aucune erreur détectable n’est survenue depuis le dernier appel à **glGetError** ou depuis que OpenGL a été initialisé.

Pour permettre les implémentations distribuées, il peut y avoir plusieurs indicateurs d’erreur. Si un indicateur d’erreur unique a enregistré une erreur, la valeur de cet indicateur est retournée et cet indicateur est réinitialisé sur GL \_ no \_ Error quand **glGetError** est appelé. Si plusieurs indicateurs ont enregistré une erreur, **glGetError** retourne et efface une valeur d’indicateur d’erreur arbitraire. Si tous les indicateurs d’erreur doivent être réinitialisés, vous devez toujours appeler **glGetError** dans une boucle jusqu’à ce qu’il retourne GL \_ no \_ Error.

Initialement, tous les indicateurs d’erreur sont définis sur GL \_ no \_ Error.

Lorsqu’un indicateur d’erreur est défini, les résultats d’une opération OpenGL ne sont pas définis uniquement si la \_ mémoire insuffisante du GL s’est \_ \_ produite. Dans tous les autres cas, la fonction qui génère l’erreur est ignorée et n’a aucun effet sur l’État OpenGL ou le contenu trame.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





