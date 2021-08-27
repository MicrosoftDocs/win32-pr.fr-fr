---
title: fonction glBlendFunc (GL. h)
description: La fonction glBlendFunc spécifie des opérations arithmétiques sur les pixels.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- glBlendFunc fonction OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4b079d0eb83f401eb7e906cb399fab18e5b2fd22f06299fcc62b1e6b4a02e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082129"
---
# <a name="glblendfunc-function"></a>glBlendFunc fonction)

La fonction **glBlendFunc** spécifie des opérations arithmétiques sur les pixels.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sfactor* 
</dt> <dd>

Spécifie la manière dont les facteurs de fusion de source rouge, vert, bleu et alpha sont calculés. Neuf constantes symboliques sont acceptées : \_ zéro GL, GL \_ un, \_ couleur de l’heure d’été GL \_ , GL \_ un moins de couleur de l' \_ heure d' \_ été \_ , GL \_ src \_ alpha, GL \_ One \_ moins \_ src \_ alpha, GL \_ DST \_ alpha, GL \_ un moins d’heure d’été alpha \_ \_ \_ et GL \_ src \_ alpha \_ saturé.

</dd> <dt>

*dfactor* 
</dt> <dd>

Spécifie la manière dont les facteurs de fusion de destination rouge, vert, bleu et alpha sont calculés. Huit constantes symboliques sont acceptées : \_ zéro GL, GL \_ un, \_ couleur de la source GL \_ , GL \_ un \_ moins \_ \_ couleur SRC, GL \_ src \_ alpha, GL \_ un \_ moins \_ src \_ alpha, GL \_ DST \_ alpha et GL \_ 1 \_ moins \_ DST \_ alpha.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *Sfactor* ou *dfactor* n’était pas une valeur acceptée.<br/>                                                                   |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

En mode RVB, les pixels peuvent être dessinés à l’aide d’une fonction qui fusionne les valeurs RVBA entrantes (source) avec les valeurs RVBA qui se trouvent déjà dans le trame (valeurs de destination). Par défaut, la fusion est désactivée. Utilisez [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l' \_ argument GL Blend pour activer et désactiver la fusion.

Quand cette option est activée, **glBlendFunc** définit l’opération de fusion. Le paramètre *sfactor* spécifie laquelle des neuf méthodes est utilisée pour mettre à l’échelle les composants de couleur source. Le paramètre *dfactor* spécifie laquelle des huit méthodes est utilisée pour mettre à l’échelle les composants de couleur de destination. Les onze méthodes possibles sont décrites dans le tableau suivant. Chaque méthode définit quatre facteurs de mise à l’échelle chacun pour les couleurs rouge, vert, bleu et alpha.

Dans le tableau et dans les équations suivantes, les composants de couleur source et de destination sont appelés (*R*? , *G*? , *B*? , *Un*? ) et (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ). Elles sont comprises comme ayant des valeurs entières comprises entre zéro et (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), où

*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1

*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1

*k*<sub>b</sub> = 2 <sup>m</sup>*b* -1

*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1

et (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>a</sub> ) est le nombre de bitplanes rouge, vert, bleu et alpha.

Les facteurs de mise à l’échelle source et de destination sont appelés (*s*<sub>r</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>a</sub> ) et (*d*<sub>r</sub> , *d*<sub>g</sub> , *d*<sub>b</sub> , *d*<sub>a</sub> ). Les facteurs d’échelle décrits dans le tableau, dénotés (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), représentent les facteurs source ou de destination. Tous les facteurs de mise à l’échelle sont compris entre \[ 0 et 1 \] .



| Paramètre                  | (*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_zéro GL                   | (0, 0, 0, 0)                                                                                                                                                    |
| GL \_ 1                    | (1, 1, 1, 1)                                                                                                                                                    |
| couleur de la source du GL \_ \_             | (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ un \_ moins \_ \_ couleur SRC | (1, 1, 1, 1)-(*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                             |
| couleur de l' \_ heure d’été GL \_             | (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub></sub>  /  *k*<sub>a</sub> )             |
| \_couleur GL 1 \_ moins \_ DST \_ | (1, 1, 1, 1)-(*r*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> ) |
| source de la \_ source GL \_             | (*Un*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>A</sub> )                                                         |
| GL \_ un \_ moins de \_ src \_ alpha | (1, 1, 1, 1)-(*A*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>A</sub> )                                             |
| de l' \_ heure d’été alpha du GL \_             | (*A*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub></sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub></sub>  /  *k*<sub>a</sub> )             |
| GL \_ 1 \_ moins \_ heure d’été \_ alpha | (1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub></sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>k  /  <sub>a</sub> ) |
| \_ \_ saturation alpha de la source GL \_   | (i, i,*i,* 1)                                                                                                                                                 |



 

Dans le tableau,

*i* = min (*A*? , *k*<sub>a</sub>   -  <sub>d</sub> )/ *k*<sub>a</sub>

Pour déterminer les valeurs RVBA lissées d’un pixel lors du dessin en mode RVBA, le système utilise les équations suivantes :

*R* (*d*) = min ( *k*<sub>r</sub> , *r*? *r r*<sub>r d</sub>  +  *r*<sub></sub> <sub></sub> )

*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  *g d*<sub></sub> <sub>g</sub> )

*B* (*d*) = min ( *k*<sub>b</sub> *, b*? *s*<sub>b</sub>  +  *b*<sub>d</sub> <sub>b</sub> )

*A* (*d*) = min ( *k*<sub>a</sub> , *a*? *s*<sub>a a</sub>  +  <sub>d</sub> <sub></sub> a)

En dépit de la précision apparente des équations ci-dessus, la fusion de l’arithmétique n’est pas exactement spécifiée, car la fusion opère avec des valeurs de couleur d’entier impréciss. Toutefois, un facteur de fusion qui doit être égal à un est garanti ne pas modifier son multiplicande, et un facteur de fusion égal à zéro réduit ses multiplicande à zéro. Ainsi, par exemple, quand *sfactor* est GL \_ src \_ alpha, *dfactor* est GL \_ un \_ moins \_ src \_ alpha et *a*? est égal à *k*<sub>a</sub>, les équations réduisent le remplacement simple :

*R*<sub>d</sub>  =  ?

*G*<sub>d</sub>  =  *g*?

B<sub>d</sub>  =  ?

*A*<sub></sub>  =  ?

## <a name="examples"></a>Exemples

La transparence est implémentée au mieux à l’aide de **glBlendFunc**(GL \_ src \_ alpha, GL \_ un \_ moins \_ src \_ alpha) avec des primitives triées du plus éloigné au plus proche. Notez que ce calcul de transparence ne nécessite pas la présence d’alpha bitplanes dans le trame.

Vous pouvez également utiliser **glBlendFunc**(GL \_ src \_ alpha, GL \_ One \_ moins \_ src \_ alpha) pour le rendu des points et des lignes antialiasés dans un ordre arbitraire.

Pour optimiser l’anticrénelage des polygones, utilisez **glBlendFunc**(GL \_ src \_ alpha \_ saturé, GL \_ un) avec des polygones triés du plus proche au plus éloigné. (Voir la comptabilité \_ \_Argument Smooth polygonal dans [**glEnable**](glenable.md) pour plus d’informations sur l’anticrénelage polygonal.) Bitplanes alpha de destination, qui doit être présent pour que cette fonction Blend fonctionne correctement, stocke la couverture accumulée.

La valeur alpha entrante (source) est une opacité de matériau, comprise entre 1,0 (*K*<sub>a</sub> ), qui représente l’opacité complète, et 0,0 (0), représentant une transparence totale.

Lorsque vous activez plusieurs mémoires tampons de couleur pour le dessin, chaque mémoire tampon activée est fusionnée séparément et le contenu de la mémoire tampon est utilisé pour la couleur de destination. (Voir [**glDrawBuffer**](gldrawbuffer.md).)

La fusion affecte uniquement le rendu RVBA. Elle est ignorée par les convertisseurs d’index de couleurs.

Les fonctions suivantes récupèrent les informations relatives à **glBlendFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Blend \_ src

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Blend \_ DST

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Blend

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





