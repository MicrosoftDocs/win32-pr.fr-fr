---
title: fonction glPixelStoref (GL. h)
description: Définit les modes de stockage en pixels. | fonction glPixelStoref (GL. h)
ms.assetid: 8d5055d7-3ea4-40b7-9447-2a005129da58
keywords:
- glPixelStoref fonction OpenGL
topic_type:
- apiref
api_name:
- glPixelStoref
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc35613be68bb142b14a7e8278d6e0b89f05d78e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104553014"
---
# <a name="glpixelstoref-function"></a>glPixelStoref fonction)

Définit les modes de stockage en pixels.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPixelStoref(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* 
</dt> <dd>

Nom symbolique du paramètre à définir. Six des paramètres de stockage affectent la manière dont les données de pixels sont retournées à la mémoire du client et ne sont donc significatives que pour les commandes [**glReadPixels**](glreadpixels.md) . Les voici :



| Paramètre de stockage                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_octets d’échange de packs GL \_ \_                                       | Si la valeur est true, l’ordre des octets pour les composants de couleur multioctets, les composants de profondeur, les index de couleurs ou les index de gabarit est inversé. Autrement dit , si un composant de quatre octets est composé d’octets *b* 0, b *1, b 2*, b 3, il est stocké en mémoire sous la forme *b* 3, b 2, b 1, b 0 si les octets d’échange de     \_ packs GL \_ \_ sont vrais. \_Les octets d’échange de packs GL n' \_ \_ ont aucun effet sur l’ordre de mémoire des composants au sein d’un pixel, mais uniquement sur l’ordre des octets dans les composants ou les index. Par exemple, les trois composants d’un \_ Pixel au format RGB du GL sont toujours stockés avec les troisièmes rouges, les secondes vertes et les tiers bleus, quelle que soit la valeur des octets de l' \_ échange de packs GL \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                               |
| LSB du Pack GL en \_ \_ \_ premier                                        | Si la valeur est true, les bits sont classés dans un octet du moins significatif au plus significatif. dans le cas contraire, le premier bit de chaque octet est le plus significatif. Ce paramètre est significatif pour les données bitmap uniquement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| \_longueur de \_ ligne du Pack GL \_                                       | Si la valeur est supérieure à zéro, \_ \_ la longueur de ligne du Pack GL \_ définit le nombre de pixels dans une ligne. Si le premier pixel d’une ligne est placé à l’emplacement p en mémoire, l’emplacement du premier pixel de la ligne suivante est obtenu en ignorant ![ l’équation qui indique l’emplacement du premier pixel de la ligne suivante dans GL_PACK_ROW_LENGTH. ](images/pix01.png) \[ composants de saut \] de ligne ou index, où *n* est le nombre de composants ou d’index dans un pixel, *l* est le nombre de pixels dans une ligne \- ( \- la longueur de ligne du Pack GL \- si elle est supérieure à zéro, l’argument Width à la routine de pixel dans le cas contraire), *a* est la valeur de l' \- alignement du Pack GL \- , et *s* est la taille, en octets, d’un seul composant (si *un*  <  *s*   =  ). dans le cas de valeurs de 1 bit, l’emplacement de la ligne suivante est obtenu en ignorant ![ l’équation qui indique l’emplacement de la ligne suivante dans GL_PACK_ROW_LENGTH.](images/pix02.png)<br/> composants ou index. Le mot *composant* dans cette description fait référence aux valeurs non indexées rouge, vert, bleu, alpha et profondeur. Le format \_ de stockage RGB RGB, par exemple, a trois composants par pixel : le premier rouge, le vert et le bleu final.<br/> |
| Pack GL- \_ \_ Ignorer \_ les pixels et <br/> \_ \_ lignes ignorées du Pack GL \_ | Ces valeurs sont fournies à titre de commodité au programmeur. elles ne fournissent aucune fonctionnalité qui ne peut pas être dupliquée simplement en incrémentant le pointeur transmis à [**glReadPixels**](glreadpixels.md). Le fait \_ d' \_ Ignorer \_ les pixels  du Pack GL revient à incrémenter le pointeur par *i n* composants ou index, où *n* est le nombre de composants ou d’index dans chaque pixel. La définition \_ \_ \_ des lignes d’omission du Pack comptable à *j* équivaut à l’incrémentation du pointeur par des composants ou des index *j k* , où *k* est le nombre de composants ou d’index par ligne, tel que calculé ci-dessus dans la section de la \_ longueur de ligne du Pack GL \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_alignement du Pack GL \_                                         | Spécifie les exigences d’alignement pour le début de chaque ligne de pixel en mémoire. Les valeurs autorisées sont 1 (alignement sur les octets), 2 (lignes alignées sur octets pairs), 4 (alignement de mot) et 8 (les lignes commencent sur les limites d’un mot double).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Les six autres paramètres de stockage affectent la manière dont les données de pixels sont lues à partir de la mémoire du client. Ces valeurs sont significatives pour [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)et [**glPolygonStipple**](glpolygonstipple.md). Les voici :



| Paramètre de stockage                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_octets de swap de décompression GL \_ \_                                         | Si la valeur est true, l’ordre des octets pour les composants de couleur multioctets, les composants de profondeur, les index de couleurs ou les index de gabarit est inversé. Autrement dit, si un composant de quatre octets est composé d’octets *b* 0, b *1, b 2* *, b 3* *, il* est stocké en mémoire sous la forme *b* 3, b *2, b 1,* *b 0 si* les octets d’échange de  \_ décompression GL \_ \_ sont vrais. \_Le DÉcompresser \_ les octets d’échange n' \_ a aucun effet sur l’ordre de mémoire des composants au sein d’un pixel, mais uniquement sur l’ordre des octets dans les composants ou les index. Par exemple, les trois composants d’un \_ Pixel au format RVB sont toujours stockés avec les troisièmes rouges, les secondes vertes et les tiers bleus, quelle que soit la valeur de la \_ décompression des octets de l’échange GL \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                           |
| COMPTABILITÉ \_ DÉcompresser \_ LSB en \_ premier                                          | Si la valeur est true, les bits sont classés dans un octet du moins significatif au plus significatif. dans le cas contraire, le premier bit de chaque octet est le plus significatif. Cela est important pour les données bitmap uniquement.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_DÉcompresser \_ la \_ longueur de ligne                                         | Si la valeur est supérieure à zéro, \_ \_ la longueur de ligne décompressée \_ par GL définit le nombre de pixels dans une ligne. Si le premier pixel d’une ligne est placé à l’emplacement p en mémoire, l’emplacement du premier pixel de la ligne suivante est obtenu en ignorant ![ l’équation qui indique l’emplacement du premier pixel de la ligne suivante dans GL_UNPACK_ROW_LENGTH. ](images/pix01.png) \[ composants de saut \] de ligne ou index, où *n* est le nombre de composants ou d’index dans un pixel, *l* est le nombre de pixels dans une ligne \- ( \- la longueur de ligne du Pack GL \- si elle est supérieure à zéro, l’argument Width à la routine de pixel dans le cas contraire), *a* est la valeur de l' \- alignement du Pack GL \- , et *s* est la taille, en octets, d’un seul composant (si *un*  <  *s*   =  ). dans le cas de valeurs de 1 bit, l’emplacement de la ligne suivante est obtenu en ignorant ![ l’équation qui indique l’emplacement de la ligne suivante dans GL_UNPACK_ROW_LENGTH.](images/pix02.png)<br/> composants ou index. Le mot *composant* dans cette description fait référence aux valeurs non indexées rouge, vert, bleu, alpha et profondeur. Le format \_ de stockage RGB RGB, par exemple, a trois composants par pixel : le premier rouge, le vert et le bleu final.<br/> |
| \_DÉcompresser \_ \_ les pixels ignorés <br/> \_DÉcompresser \_ les \_ lignes ignorées | Ces valeurs sont fournies à titre de commodité au programmeur. elles ne fournissent aucune fonctionnalité qui ne peut pas être dupliquée simplement en incrémentant le pointeur passé à [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)ou [**glPolygonStipple**](glpolygonstipple.md). La définition de \_ l’option DÉcompresser les pixels DÉcompressés \_ \_ est équivalente à l’incrémentation du pointeur par les composants ou les index *i n* ,  où *n* est le nombre de composants ou d’index de chaque pixel. La définition de \_ l’option DÉcompresser \_ \_ les lignes de décompression à la valeur *j* équivaut à incrémenter le pointeur par des composants ou des index *j k* , où *k* est le nombre de composants ou d’index par ligne, comme indiqué ci-dessus dans la \_ section « décompresser la longueur de ligne de décompression \_ \_ ».                                                                                                                                                                                                                                    |
| alignement de la \_ décompression GL \_                                           | Spécifie les exigences d’alignement pour le début de chaque ligne de pixel en mémoire. Les valeurs autorisées sont 1 (alignement sur les octets), 2 (lignes alignées sur octets pairs), 4 (alignement de mot) et 8 (les lignes commencent sur les limites d’un mot double).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

Valeur définie pour l' *pname* .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **glPixelStore** définit les modes de stockage en pixels qui affectent le fonctionnement des [**glDrawPixels**](gldrawpixels.md) et [**glReadPixels**](glreadpixels.md) suivants, ainsi que la décompression des modèles de polygone stipple (consultez [**glPolygonStipple**](glpolygonstipple.md)), des bitmaps (consultez [**GlBitmap**](glbitmap.md)) et des modèles de texture (consultez [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)et [**glTexSubImage2D**](gltexsubimage2d.md)).

Le tableau suivant indique le type, la valeur initiale et la plage de valeurs valides pour chacun des paramètres de stockage qui peuvent être définis avec **glPixelStore**.



| Pname                    | Type    | Valeur initiale | Plage valide   |
|--------------------------|---------|---------------|---------------|
| \_octets d’échange de packs GL \_ \_    | Boolean | false         | True ou False |
| \_octets d’échange de packs GL \_ \_    | Boolean | false         | True ou False |
| \_longueur de \_ ligne du Pack GL \_    | integer | 0             | \[0, ?)        |
| \_ \_ lignes ignorées du Pack GL \_     | integer | 0             | \[0, ?)        |
| \_Ignorer les \_ \_ pixels du Pack GL   | integer | 0             | \[0, ?)        |
| \_alignement du Pack GL \_      | entier | 4             | 1, 2, 4 ou 8 |
| \_octets de swap de décompression GL \_ \_  | Boolean | false         | True ou False |
| COMPTABILITÉ \_ DÉcompresser \_ LSB en \_ premier   | Boolean | false         | True ou False |
| \_DÉcompresser \_ la \_ longueur de ligne  | integer | 0             | \[0, ?)        |
| \_DÉcompresser \_ les \_ lignes ignorées   | integer | 0             | \[0, ?)        |
| \_DÉcompresser \_ les \_ pixels ignorés | integer | 0             | \[0, ?)        |
| alignement de la \_ décompression GL \_    | entier | 4             | 1, 2, 4 ou 8 |



 

La fonction **glPixelStoref** peut être utilisée pour définir un paramètre de magasin de pixels. Si le type de paramètre est booléen et si *param* est 0,0, alors le paramètre a la valeur false ; Sinon, elle a la valeur true. Si *pname* est un paramètre de type entier, alors *param* est arrondi à l’entier le plus proche.

De même, la fonction **glPixelStorei** peut également être utilisée pour définir les paramètres du magasin de pixels. Les paramètres booléens ont la valeur false si *param* est 0 et true dans le cas contraire. Le paramètre *param* est converti en virgule flottante avant d’être assigné à des paramètres réels.

Les modes de stockage en pixels appliqués lorsque [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)ou [**glPolygonStipple**](glpolygonstipple.md) est placé dans une liste d’affichage contrôlent l’interprétation des données de mémoire. Les modes de stockage en pixels en vigueur lors de l’exécution d’une liste d’affichage ne sont pas significatifs.

Les fonctions suivantes récupèrent les informations relatives à **glPixelStore**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ Report GL \_ \_ octets swap

**glGet** avec argument GL \_ Pack \_ LSB en \_ premier

**glGet** avec argument de \_ la \_ longueur de ligne du Pack GL \_

**glGet** avec argument GL \_ Pack \_ Skip \_ lignes

**glGet** avec argument GL \_ Pack \_ ignore les \_ pixels

**glGet** avec argument de \_ l' \_ alignement GL Pack

**glGet** avec argument GL \_ décompresser les \_ octets d’échange \_

**glGet** avec l’argument GL \_ Unpack \_ LSB \_ First

**glGet** avec argument GL \_ décompresser la \_ longueur de ligne \_

**glGet** avec argument GL \_ décompresser les \_ \_ lignes

**glGet** avec argument GL \_ décompresser \_ Ignorer les \_ pixels

**glGet** avec l’argument GL \_ décompresser l' \_ alignement

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





