---
title: gluNurbsProperty, fonction (Glu. h)
description: La fonction gluNurbsProperty définit une propriété NURBS B-spline (NURBS) non uniforme.
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
keywords:
- gluNurbsProperty fonction OpenGL
topic_type:
- apiref
api_name:
- gluNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cbc52bd1405d15967db4aa1ef4941d0c4e166420d25d6d1fcb1ba4db0a6e744
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489029"
---
# <a name="glunurbsproperty-function"></a>gluNurbsProperty fonction)

La fonction **gluNurbsProperty** définit une propriété NURBS B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nobj* 
</dt> <dd>

Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Propriété à définir. Les valeurs suivantes sont valides :



| Value                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_SAMPLING_TOLERANCE"></span><span id="glu_sampling_tolerance"></span><dl> <dt>**\_tolérance d’échantillonnage Glu \_**</dt> </dl>       | Spécifie la longueur maximale, en pixels, à utiliser lorsque la méthode d’échantillonnage est définie sur la \_ longueur du chemin d’accès Glu \_ . La valeur par défaut est 50,0 pixels.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GLU_DISPLAY_MODE"></span><span id="glu_display_mode"></span><dl> <dt>**\_mode d’affichage Glu \_**</dt> </dl>                         | Le paramètre *value* définit le mode de rendu d’une surface NURBS. Vous pouvez définir la *valeur* sur Glu \_ Fill, Glu \_ contour \_ Polygon ou Glu \_ Outline \_ patch. <br/> \_remplissage Glu. La surface est rendue sous la forme d’un ensemble de polygones. Il s'agit de la valeur par défaut. <br/> \_polygone de contour Glu \_ . La bibliothèque NURBS dessine uniquement les contours des polygones créés par pavage. <br/> \_correctif Glu plan \_ . Seules les contours des carreaux et des courbes de rognage définies par l’utilisateur sont dessinées.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CULLING"></span><span id="glu_culling"></span><dl> <dt>**élimination des GLU \_**</dt> </dl>                                         | Le paramètre de *valeur* est une valeur booléenne. Lorsque la valeur est définie sur GL \_ true, les courbes NURBS dont les points de contrôle se trouvent en dehors de la fenêtre d’affichage actuelle sont ignorées avant le pavage. La valeur par défaut est GL \_ false (car une courbe NURBS ne peut pas être entièrement comprise dans la coque convexe de ses points de contrôle).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GLU_AUTO_LOAD_MATRIX"></span><span id="glu_auto_load_matrix"></span><dl> <dt>**\_matrice de \_ chargement \_ automatique Glu**</dt> </dl>            | Le paramètre de *valeur* est une valeur booléenne. Lorsqu’il est défini sur GL \_ true, le code nurbs télécharge la matrice de projection, la matrice modelview et la fenêtre d’affichage à partir du serveur OpenGL pour calculer les matrices d’échantillonnage et d’élimination pour chaque courbe NURBS rendue. Les matrices d’échantillonnage et d’élimination sont requises pour déterminer le pavage d’une surface NURBS dans des segments de ligne ou des polygones et pour le Culling d’une surface NURBS si elle se trouve en dehors de la fenêtre d’affichage. <br/> Si ce mode est défini sur GL \_ false, vous devez fournir une matrice de projection, une matrice modelview et une fenêtre d’affichage pour le convertisseur NURBS à utiliser pour construire des matrices d’échantillonnage et d’élimination. Vous pouvez le faire avec la fonction [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md) .<br/> La valeur par défaut de ce mode est GL \_ true. La modification de ce mode de \_ la valeur GL true à GL \_ false n’affecte pas les matrices d’échantillonnage et de Culling tant que vous n’avez pas appelé [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md). <br/> Les paramètres de propriété suivants sont pris en charge dans GLU version 1,1 ou ultérieure et ne sont pas valides pour GLU version 1,0 : GLU \_ tolérance paramétrique \_ , \_ méthode d’échantillonnage Glu \_ , Glu \_ U \_ étape et \_ étape Glu V \_ .<br/> Les paramètres de valeur suivants sont pris en charge dans GLU version 1,1 ou ultérieure et ne sont pas valides pour GLU version 1,0 : GLU \_ chemin \_ longueur, Glu \_ erreur paramétrique \_ et \_ distance du domaine Glu \_ .<br/> |
| <span id="GLU_PARAMETRIC_TOLERANCE"></span><span id="glu_parametric_tolerance"></span><dl> <dt>**\_tolérance paramétrique \_ Glu**</dt> </dl> | Spécifie la distance maximale, en pixels, à utiliser lorsque la méthode d’échantillonnage est définie sur GLU erreur paramétrique \_ \_ . La valeur par défaut est 0,5.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_SAMPLING_METHOD"></span><span id="glu_sampling_method"></span><dl> <dt>**\_méthode d’échantillonnage Glu \_**</dt> </dl>                | Spécifie comment tessallate une surface NURBS. \_ \_ La méthode d’échantillonnage Glu peut avoir l’une des trois valeurs suivantes. <br/> \_longueur du chemin d’accès Glu \_ . Valeur par défaut. Spécifie que les surfaces rendues avec la longueur maximale, en pixels, des bords des polygones de pavage ne sont pas supérieures à la valeur spécifiée par la \_ tolérance d’échantillonnage Glu \_ . <br/> \_erreur paramétrique Glu \_ . Spécifie que, lors du rendu de la surface, la valeur de la \_ tolérance paramétrique Glu \_ spécifie la distance maximale, en pixels, entre les polygones de pavage et les surfaces qu’ils approchent. <br/> \_distance du domaine Glu \_ . Spécifie, dans les coordonnées paramétriques, le nombre de points d’échantillonnage par longueur d’unité à prendre dans les dimensions *u* et *v* .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GLU_U_STEP"></span><span id="glu_u_step"></span><dl> <dt>**GLU \_ U \_ étape**</dt> </dl>                                           | Spécifie le nombre de points d’échantillonnage par longueur d’unité pris le long de la dimension *u* dans les coordonnées paramétriques. La valeur de GLU \_ U \_ Step est utilisée lorsque la \_ méthode d’échantillonnage Glu \_ est définie sur Glu \_ Domain \_ distance. La valeur par défaut est 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_V_STEP"></span><span id="glu_v_step"></span><dl> <dt>**\_étape Glu V \_**</dt> </dl>                                           | Spécifie le nombre de points d’échantillonnage par longueur d’unité pris le long de la dimension *v* dans les coordonnées paramétriques. La valeur de GLU \_ V \_ Step est utilisée lorsque la \_ méthode d’échantillonnage Glu \_ est définie sur Glu \_ Domain \_ distance. La valeur par défaut est 100.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*value* 
</dt> <dd>

Valeur à laquelle définir la propriété indiquée. Le paramètre de *valeur* peut être une valeur numérique ou l’une des trois valeurs suivantes : \_ longueur du chemin d’accès Glu \_ , \_ erreur paramétrique GLU \_ ou \_ distance du domaine Glu \_ .



| Valeur                                                                                                                                                                               | Signification                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_PATH_LENGTH"></span><span id="glu_path_length"></span><dl> <dt>**\_longueur du chemin d’accès Glu \_**</dt> </dl>                | Valeur par défaut. Spécifie que les surfaces rendues avec la longueur maximale, en pixels, des bords des polygones de pavage ne sont pas supérieures à la valeur spécifiée par la \_ tolérance d’échantillonnage Glu \_ .<br/> |
| <span id="GLU_PARAMETRIC_ERROR"></span><span id="glu_parametric_error"></span><dl> <dt>**\_erreur paramétrique \_ Glu**</dt> </dl> | Spécifie que, lors du rendu de la surface, la valeur de la \_ tolérance paramétrique Glu \_ spécifie la distance maximale, en pixels, entre les polygones de pavage et les surfaces qu’ils approchent.<br/>       |
| <span id="GLU_DOMAIN_DISTANCE"></span><span id="glu_domain_distance"></span><dl> <dt>**\_distance du domaine Glu \_**</dt> </dl>    | Spécifie, dans les coordonnées paramétriques, le nombre de points d’échantillonnage par longueur d’unité à prendre dans les dimensions *u* et *v* .<br/>                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Utilisez **gluNurbsProperty** pour contrôler les propriétés stockées dans un objet NURBS. Ces propriétés affectent le mode de rendu d’une courbe NURBS.





 

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

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluGetString**](glugetstring.md)
</dt> <dt>

[**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





