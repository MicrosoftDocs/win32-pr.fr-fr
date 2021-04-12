---
title: fonction glAddSwapHintRectWIN (GL. h)
description: La fonction de rappel glAddSwapHintRectWIN spécifie un ensemble de rectangles à copier par SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- glAddSwapHintRectWIN fonction OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384832"
---
# <a name="gladdswaphintrectwin-function"></a>glAddSwapHintRectWIN fonction)

La fonction de rappel **glAddSwapHintRectWIN** spécifie un ensemble de rectangles à copier par [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x* 
</dt> <dd>

Coordonnée *x*(en coordonnées de la fenêtre) de l’angle inférieur gauche du rectangle de la zone de l’indicateur.

</dd> <dt>

*y* 
</dt> <dd>

Coordonnée *y*(dans les coordonnées de la fenêtre) de l’angle inférieur gauche du rectangle de la zone d’indicateur.

</dd> <dt>

*width* 
</dt> <dd>

Largeur du rectangle de la zone d’indicateur.

</dd> <dt>

*height* 
</dt> <dd>

Hauteur du rectangle de la zone de l’indicateur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **glAddSwapHintRectWIN** accélère l’animation en réduisant la quantité de redessin entre les frames. Avec **glAddSwapHintRectWIN**, vous spécifiez un ensemble de zones rectangulaires que vous souhaitez copier lorsque vous appelez [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). Lorsque vous ne spécifiez pas de rectangles avec **glAddSwapHintRectWIN** avant d’appeler **SwapBuffers**, la totalité du trame est permutée. L’utilisation de **glAddSwapHintRectWIN** pour copier uniquement les parties modifiées de la mémoire tampon peut augmenter considérablement les performances de **SwapBuffers**, en particulier lorsque **SwapBuffers** est implémenté dans le logiciel.

La fonction **glAddSwapHintRectWIN** ajoute un rectangle à la région de l’indicateur. Lorsque l' \_ \_ indicateur de copie d’échange PFD de la structure de format de pixel [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) est défini, **SwapBuffers** utilise cette région pour découper la copie de la mémoire tampon d’arrière-plan dans la mémoire tampon d’arrière-plan. Vous ne spécifiez pas la \_ \_ copie d’échange PFD ; elle est définie par le matériel de compatibilité. La région de l’indicateur est effacée après chaque appel à **SwapBuffers**. Avec certaines configurations matérielles, **SwapBuffers** peut ignorer la région de l’indicateur et échanger la totalité de la mémoire tampon. **SwapBuffers** est implémenté par le système, et non par l’application.

OpenGL conserve une région d’indication distincte pour chaque fenêtre. Quand vous appelez **glAddSwapHintRectWIN** sur n’importe quel contexte de rendu associé à une fenêtre, les rectangles d’indicateurs sont combinés dans une seule région.

Appelez **glAddSwapHintRectWIN** avec un rectangle englobant pour chaque objet dessiné pour un frame et pour chaque rectangle effacé pour effacer les objets Frame précédents.

> [!Note]  
> La fonction **glAddSwapHintRectWIN** est une fonction d’extension qui ne fait pas partie de la bibliothèque OpenGL standard, mais qui fait partie de l’extension de l’indicateur de remplacement de Win pour le GL \_ \_ \_ . Pour vérifier si votre implémentation d’OpenGL prend en charge **glAddSwapHintRectWIN**, appelez **glGetString**( \_ Extensions GL). Si elle retourne l' \_ \_ indicateur de remplacement du GL Win \_ , **glAddSwapHintRectWIN** est pris en charge. Pour obtenir l’adresse d’une fonction d’extension, appelez **wglGetProcAddress**.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





