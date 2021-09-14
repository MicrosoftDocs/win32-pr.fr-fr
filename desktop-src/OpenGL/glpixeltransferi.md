---
title: fonction glPixelTransferi (GL. h)
description: Les fonctions glPixelTransferf et glPixelTransferi définissent les modes de transfert de pixels. | fonction glPixelTransferi (GL. h)
ms.assetid: 351a872d-2cce-4fb1-b736-72201baf4157
keywords:
- glPixelTransferi fonction OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67415a8e105dc95f3e21e6968042496b9db52038
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324833"
---
# <a name="glpixeltransferi-function"></a>glPixelTransferi fonction)

Les fonctions [**glPixelTransferf**](glpixeltransferf.md) et **glPixelTransferi** définissent les modes de transfert de pixels.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPixelTransferi(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* 
</dt> <dd>

Nom symbolique du paramètre de transfert de pixels à définir. Le tableau suivant indique le type, la valeur initiale et la plage de valeurs valides pour chacun des paramètres de transfert de pixels qui sont définis avec **glPixelTransfer**.



| Pname             | Type    | Valeur initiale  | Plage valide  |
|-------------------|---------|----------------|--------------|
| couleur de la \_ carte GL \_    | Booléen | false          | true/false   |
| STENCIL de la \_ carte GL \_  | Booléen | false          | true/false   |
| décalage de l' \_ index GL \_  | entier | 0              | (8, 8)        |
| décalage de l' \_ index GL \_ | entier | 0              | (8, 8)        |
| \_échelle rouge du GL \_    | entier | 1.0            | (8, 8)        |
| \_échelle verte du GL \_  | float   | 1.0            | (8, 8)        |
| \_échelle bleue \_ GL   | float   | 1.0            | (8, 8)        |
| \_échelle alpha \_ GL  | float   | 1.0            | (8, 8)        |
| \_échelle de profondeur du GL \_  | float   | 1.0            | (8, 8)        |
| \_décalage rouge du GL \_     | float   | 0.0            | (8, 8)        |
| \_décalage vert du GL \_   | float   | 0.0            | (8, 8)        |
| \_décalage bleu du GL \_    | float   | 0.0            | (8, 8)        |
| \_décalage alpha du GL \_   | float   | 0.0            | (8, 8)        |
| \_décalage de profondeur du GL \_   | float   | 0.0            | (8, 8)        |



 

</dd> <dt>

*param* 
</dt> <dd>

Valeur définie pour l' *pname* .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **glPixelTransfer** définit les modes de transfert de pixels qui affectent le fonctionnement des commandes suivantes [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)et [**glTexSubImage2D**](gltexsubimage2d.md) . Les algorithmes qui sont spécifiés par les modes de transfert de pixels fonctionnent sur les pixels après qu’ils ont été lus à partir de trame (**glReadPixels** et **glCopyPixels**) ou décompressés de la mémoire du client (**glDrawPixels**, **glTexImage1D** et **glTexImage2D**). Les opérations de transfert de pixels se produisent dans le même ordre, et de la même manière, quelle que soit la commande ayant entraîné l’opération de pixel. Les modes de stockage en pixels ([**glPixelStore**](glpixelstore-functions.md)) contrôlent la décompression des pixels lus à partir de la mémoire du client et la compression des pixels en cours de réécriture dans la mémoire du client.

Les opérations de transfert de pixels gèrent quatre types de pixels fondamentaux : *couleur*, *index de couleur*, *profondeur* et *gabarit*. Les pixels de couleur sont constitués de quatre valeurs à virgule flottante avec des tailles de mantisse et d’exposant non spécifiées, mises à l’échelle de telle sorte que 0,0 représente une intensité nulle et 1,0 représente une intensité complète. Les index de couleurs comprennent une seule valeur à virgule fixe, avec une précision non spécifiée à droite du point binaire. Les pixels de profondeur comportent une valeur à virgule flottante unique, avec des tailles de mantisse et d’exposant non spécifiées, mises à l’échelle de telle sorte que 0,0 représente la valeur de mémoire tampon de profondeur minimale, et 1,0 représente la valeur de mémoire tampon de profondeur maximale. Enfin, les pixels du stencil comprennent une seule valeur à virgule fixe, avec une précision non spécifiée à droite du point binaire.

Les opérations de transfert de pixels effectuées sur les quatre types de pixels de base sont les suivantes :



| Type de pixel  | Opération de transfert de pixels                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Couleur       | Chacun des quatre composants de couleur est multiplié par un facteur d’échelle, puis ajouté à un facteur de décalage. Autrement dit, le composant rouge est multiplié par l’échelle du GL \_ Red \_ , puis ajouté à \_ \_ l’écart rouge du GL ; le composant vert est multiplié par l’échelle du GL du grand livre, puis ajouté à l’écart vert du GL ; le composant bleu est multiplié par l’échelle du GL du GL, puis ajouté au biais du grand livre \_ \_ bleu, \_ \_ \_ \_ \_ \_ et le composant alpha est multiplié par l' \_ \_ échelle alpha \_ \_ du GL Une fois les quatre composants de couleur mis à l’échelle et biaisés, chacun est ancré à la plage \[ 0, 1 \] . Toutes les valeurs d’échelle de couleurs et de biais sont spécifiées avec **glPixelTransfer**. <br/> Si la \_ \_ couleur de la carte GL est définie sur true, chaque composant de couleur est mis à l’échelle en fonction de la taille de la carte de couleur en couleurs correspondante, puis remplacé par le contenu de la carte indexée par le composant mis à l’échelle. Autrement dit, le composant rouge est mis à l’échelle de la \_ carte de pixels GL \_ \_ r à la \_ \_ \_ taille r, puis remplacé par le contenu de la \_ carte de pixels GL r en \_ \_ \_ \_ r indexée par lui-même. Le composant vert est mis à l’échelle de la \_ carte de pixels GL \_ \_ g à la \_ \_ \_ taille g, puis remplacé par le contenu de la \_ carte de pixels GL g en \_ \_ \_ \_ g indexé par lui-même. Le composant bleu est mis à l’échelle selon la \_ taille de la carte de pixels GL \_ \_ b \_ à \_ b \_ , puis remplacé par le contenu de la \_ carte de pixels GL \_ \_ b \_ \_ par b. Le composant alpha est mis à l’échelle \_ par \_ la carte de pixels GL \_ a \_ à \_ une \_ taille, puis remplacé par le contenu de la \_ carte de pixel GL \_ \_ a \_ sur \_ un index indexé par lui-même. Tous les composants tirés des mappages sont ensuite ancrés à la plage de \[ 0 à 1 \] . La \_ couleur de la carte GL \_ est spécifiée avec **glPixelTransfer**. Le contenu des différents mappages est spécifié avec **glPixelMap**.<br/>                                                                                                                        |
| Index des couleurs | Chaque index de couleur est décalé vers la gauche par les \_ bits de décalage de l’index GL \_ , en remplissant avec des zéros tous les bits au-delà du nombre de bits de fraction effectué par l’index à virgule fixe. Si \_ \_ le décalage de l’index GL est négatif, le décalage est à droite, à zéro. \_ \_ Le décalage de l’index GL est ensuite ajouté à l’index. Les décalages de l’index GL et de l' \_ \_ \_ index GL \_ sont spécifiés avec **glPixelTransfer**.<br/> À partir de ce point, l’opération est diverge en fonction du format requis des pixels obtenus. Si les pixels résultants doivent être écrits dans une mémoire tampon d’index de couleurs, ou s’ils sont lus dans la mémoire du client \_ dans \_ le format d’index de couleurs GL, les pixels continuent à être traités comme des index. Si la \_ couleur de la carte GL est définie sur \_ true, chaque index est masqué par 2 ^ *n* 1, où *n* est la \_ \_ carte de pixel GL \_ i \_ à \_ i \_ Size, puis remplacé par le contenu de la \_ carte de pixels GL \_ \_ i \_ à \_ indexer par la valeur masquée. La \_ couleur de la carte GL \_ est spécifiée avec **glPixelTransfer**. Le contenu du mappage d’index est spécifié avec **glPixelMap**.<br/> Si les pixels résultants doivent être écrits dans une mémoire tampon de couleur RVBA, ou s’ils sont lus dans la mémoire du client dans un format autre que le format de l' \_ index de couleur GL \_ , les pixels sont convertis des index en couleurs en faisant référence aux quatre cartes de la carte des pixels GL \_ \_ \_ i \_ à \_ R, GL \_ pixel \_ Map \_ i \_ à \_ G, GL \_ Pixel Map i \_ \_ \_ à \_ B et GL \_ pixel \_ \_ \_ \_ Avant d’être déréférencés, l’index est masqué par 2 n 1, où n est la \_ carte de pixel GL \_ \_ i \_ à \_ \_ taille pour la carte rouge, \_ carte de pixels GL \_ \_ i \_ à \_ G \_ pour la carte verte, \_ carte de pixel GL \_ \_ i \_ à \_ B \_ pour la carte bleue et la \_ \_ carte de pixels GL \_ i \_ à \_ une \_ taille pour la carte alpha. Tous les composants tirés des mappages sont ensuite ancrés à la plage de \[ 0 à 1 \] . Le contenu des quatre mappages est spécifié avec **glPixelMap**.<br/> |
| Profondeur       | Chaque valeur de profondeur est multipliée \_ par \_ l’échelle de profondeur GL, ajoutée à \_ l’écart de profondeur GL, puis fixée \_ à la plage \[ 0, 1 \] .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Stencil     | Chaque index est décalé vers le décalage de l' \_ index GL \_ comme un index de couleur, puis ajouté au décalage de l' \_ index GL \_ . Si le \_ stencil de la carte GL \_ a la valeur true, chaque index est masqué par 2n 1, où *n* est la \_ \_ carte de pixels GL \_ s \_ à \_ s \_ , puis remplacée par le contenu de la \_ carte de pixels GL s en \_ \_ \_ \_ s indexée par la valeur masquée.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

La fonction [**glPixelTransferf**](glpixeltransfer.md) peut être utilisée pour définir un paramètre de transfert de pixels. Si le type de paramètre est Boolean, 0,0 implique false et toute autre valeur implique true. Si *pname* est un paramètre entier, *param* est arrondi à l’entier le plus proche.

De même, **glPixelTransferi** peut également être utilisé pour définir les paramètres de transfert de pixels. Les paramètres booléens ont la valeur false si *param* est 0 et true dans le cas contraire. Le paramètre *param* est converti en virgule flottante avant d’être assigné à des paramètres réels.

Si une commande [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)ou [**glTexImage2D**](glteximage2d.md) est placée dans une liste d’affichage (voir [**glNewList**](glnewlist.md) et [**glCallList**](glcalllist.md)), les paramètres du mode de transfert en pixels en vigueur lors de l' *exécution* de la liste d’affichage sont ceux qui sont utilisés. Elles peuvent être différentes des paramètres lors de la compilation de la commande dans la liste d’affichage.

Les fonctions suivantes récupèrent les informations relatives à **glPixelTransfer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument couleur de la \_ carte GL \_

**glGet** avec argument stencil de la carte de GL \_ \_

**glGet** avec argument GL \_ index \_ Shift

**glGet** avec argument de \_ décalage d’index GL \_

**glGet** avec argument GL \_ Red \_ Scale

**glGet** avec argument GL \_ - \_ décalage rouge

**glGet** avec argument GL \_ vert \_ Scale

**glGet** avec argument GL \_ de \_ décalage vert

**glGet** avec argument GL de l' \_ \_ échelle bleue

**glGet** avec argument GL \_ bleu \_ biais

**glGet** avec argument GL \_ alpha \_ Scale

**glGet** avec argument GL \_ alpha \_ Bias

**glGet** avec l' \_ échelle de profondeur de l’argument GL \_

**glGet** avec argument de profondeur GL d’argument \_ \_

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





