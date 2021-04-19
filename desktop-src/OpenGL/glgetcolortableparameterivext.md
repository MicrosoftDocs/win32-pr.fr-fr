---
title: fonction glGetColorTableParameterivEXT (GL. h)
description: Les fonctions glGetColorTableParameterfvEXT et glGetColorTableParameterivEXT obtiennent des paramètres de palette à partir des tables de couleurs. | fonction glGetColorTableParameterivEXT (GL. h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- glGetColorTableParameterivEXT fonction OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897dd11781968838bb8c26a716e3857acc119e9c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524825"
---
# <a name="glgetcolortableparameterivext-function"></a>glGetColorTableParameterivEXT fonction)

Les fonctions [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) et **glGetColorTableParameterivEXT** obtiennent des paramètres de palette à partir des tables de couleurs.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Texture cible de la palette pour laquelle vous souhaitez obtenir des données de paramètre. Doit être une TEXTURE \_ 1D, une texture \_ 2D, une texture de proxy \_ \_ 1D ou une texture de proxy \_ \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

Constante symbolique pour le type de données de paramètre de palette vers lequel pointe les *paramètres.*

Voici les constantes symboliques acceptées et leurs significations.



| Valeur                                                                                                                                                                                                             | Signification                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**\_format de table de couleurs GL \_ \_ \_ ext**</dt> </dl>              | Retourne le format interne spécifié par l’appel le plus récent à [**glColorTableEXT**](glcolortableext.md) ou la valeur par défaut.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**\_largeur de table de couleur GL \_ \_ \_ ext**</dt> </dl>                 | Retourne la largeur de la palette actuelle.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**Table des couleurs GL- \_ \_ \_ \_ taille rouge \_ ext**</dt> </dl>       | Retourne la taille réelle utilisée en interne pour stocker le composant rouge des données de la palette.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**taille de la table de couleur GL- \_ \_ \_ \_ \_ ext**</dt> </dl> | Retourne la taille réelle utilisée en interne pour stocker le composant vert des données de la palette.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**taille de la table de couleur GL en \_ \_ \_ bleu \_ \_ ext**</dt> </dl>    | Retourne la taille réelle utilisée en interne pour stocker le composant bleu des données de palette.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**Table des couleurs GL- \_ \_ \_ \_ taille alpha \_ ext**</dt> </dl> | Retourne la taille réelle utilisée en interne pour stocker le composant alpha des données de palette.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Pointe vers les données de paramètre de table de couleurs spécifiées par le paramètre *pname* .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Vous utilisez les fonctions **glGetColorTableParameterivEXT** et [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) pour récupérer des données de paramètres spécifiques à partir de tables de couleurs définies avec [**glColorTableEXT**](glcolortableext.md) pour les palettes de texture ciblées. Vous pouvez également utiliser ces fonctions pour déterminer le nombre d’entrées de table des couleurs retournées par **glGetColorTableEXT** .

Lorsque le paramètre *cible* est \_ une texture \_ de proxy de GL \_ 1D ou \_ une texture de proxy GL \_ \_ 2D, et que l’implémentation ne prend pas en charge les valeurs spécifiées pour le *format* ou la *largeur*, **glColorTableEXT** peut ne pas réussir à créer la table de couleurs demandée. Dans ce cas, la table des couleurs est vide et tous les paramètres récupérés sont nuls. Vous pouvez déterminer si OpenGL prend en charge un format et une taille de table de couleur particuliers en appelant **glColorTableEXT** avec une cible de proxy, puis en appelant **glGetColorTableParameterivEXT** ou [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) pour déterminer si le paramètre Width correspond à celui défini par **glColorTableEXT**. Si la largeur Récupérée est égale à zéro, la requête de la table de couleurs par **glColorTable** a échoué. Si la largeur Récupérée n’est pas égale à zéro, vous pouvez appeler **glColorTable** avec la cible réelle avec la texture \_ 1D ou texture \_ 2D pour définir la table des couleurs.

Les fonctions **glGetColorTableParameterivEXT** et [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) sont des fonctions d’extension qui ne font pas partie de la bibliothèque OpenGL standard, mais font partie de l’extension de \_ texture de palette ext GL \_ \_ . Pour vérifier si votre implémentation de OpenGL prend en charge **glGetColorTableParameterivEXT** et **glGetColorTableParameterfvEXT**, appelez [**glGetString**](glgetstring.md)**(** \_ Extensions GL **)**. Si elle retourne la \_ texture de palette ext GL \_ \_ , **glGetColorTableParameterivEXT** et **glGetColorTableParameterfvEXT** sont pris en charge. Pour obtenir l’adresse de fonction d’une fonction d’extension, appelez [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





