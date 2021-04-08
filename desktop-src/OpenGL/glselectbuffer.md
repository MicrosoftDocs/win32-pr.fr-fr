---
title: fonction glSelectBuffer (GL. h)
description: La fonction glSelectBuffer établit une mémoire tampon pour les valeurs du mode de sélection.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- glSelectBuffer fonction OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740037"
---
# <a name="glselectbuffer-function"></a>glSelectBuffer fonction)

La fonction **glSelectBuffer** établit une mémoire tampon pour les valeurs du mode de sélection.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*size* 
</dt> <dd>

Taille de la *mémoire tampon*.

</dd> <dt>

*mémoire tampon* 
</dt> <dd>

Retourne les données de sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *taille* était négative.<br/>                                                                                                       |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée alors que le mode de rendu était « GL \_ Select ».<br/>                                                              |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glSelectBuffer** a deux paramètres : la *mémoire tampon* est un pointeur vers un tableau d’entiers non signés et la *taille* indique la taille du tableau. Le paramètre *buffer* retourne des valeurs à partir de la pile de noms (consultez [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) lorsque le mode de rendu est GL \_ Select (voir [**glRenderMode**](glrendermode.md)). La fonction **glSelectBuffer** doit être émise avant l’activation du mode de sélection, et elle ne doit pas être émise tant que le mode de rendu est GL \_ Select.

La sélection est utilisée par un programmeur pour déterminer quelles primitives sont dessinées dans une région d’une fenêtre. La région est définie par les matrices de modelview et de perspective actuelles.

En mode de sélection, aucun fragment de pixel n’est produit à partir de la pixellisation. Au lieu de cela, si une primitive croise le volume de clip défini par l’frustum de visualisation et les plans de découpage définis par l’utilisateur, cette primitive provoque un accès à la sélection. (Avec les polygones, aucun accès n’a lieu si le polygone est éliminé.) Lorsqu’une modification est apportée à la pile de noms, ou lorsque [**glRenderMode**](glrendermode.md) est appelé, un enregistrement d’accès est copié dans *buffer* si des accès ont eu lieu depuis le dernier événement de ce type (modification de la pile de noms ou appel **glRenderMode** ). L’enregistrement d’accès se compose du nombre de noms dans la pile de noms au moment de l’événement ; suivi des valeurs de profondeur minimale et maximale de tous les vertex ayant atteint depuis l’événement précédent ; suivi du nom du contenu de la pile, en commençant par le nom inférieur.

Les valeurs de profondeur retournées sont mappées de telle sorte que la plus grande valeur entière non signée correspond à la profondeur de la coordonnée 1,0 et zéro correspond à la profondeur de la coordonnée de la fenêtre 0,0.

Un index interne dans la *mémoire tampon* est réinitialisé à zéro chaque fois que le mode de sélection est entré. Chaque fois qu’un enregistrement atteint est copié dans la *mémoire tampon*, l’index est incrémenté pour pointer vers la cellule située juste après la fin du bloc de namesthat, vers la cellule suivante disponible. Si l’enregistrement d’accès est plus grand que le nombre d’emplacements restants dans la *mémoire tampon*, autant de données que possible est copié, et l’indicateur de dépassement de capacité est défini. Si la pile de noms est vide lorsqu’un enregistrement d’accès est copié, cet enregistrement se compose de zéro suivi des valeurs de profondeur minimale et maximale.

Le mode de sélection est fermé en appelant **glRenderMode** avec un argument autre que GL \_ Select. Chaque fois que **glRenderMode** est appelé alors que le mode de rendu est GL \_ Select, il retourne le nombre d’enregistrements d’accès copiés dans la *mémoire tampon*, réinitialise l’indicateur de dépassement de capacité et le pointeur de mémoire tampon de sélection, puis initialise la pile de noms pour qu’elle soit vide. Si le bit de dépassement de capacité a été défini lors de l’appel de **glRenderMode** , un nombre d’enregistrements d’accès négatif est retourné.

Le contenu de *buffer* n’est pas défini tant que [**glRenderMode**](glrendermode.md) n’est pas appelé avec un argument autre que GL \_ Select.

Les  / primitives **glEnd** glBegin et les appels à [**glRasterPos**](glrasterpos-functions.md) peuvent entraîner des résultats.

La fonction suivante récupère des informations relatives à **glSelectBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la \_ pile nom GL \_ \_

## <a name="requirements"></a>Configuration requise



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
</dt> <dt>

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





