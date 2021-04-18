---
title: fonction glMateriali (GL. h)
description: La fonction TheglMateriali spécifie les paramètres de matériau pour le modèle d’éclairage.
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- glMateriali fonction OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc4f1bf6628f1674cf9c3534b9f0c9d028246d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512557"
---
# <a name="glmateriali-function"></a>glMateriali fonction)

La fonction **glMateriali** spécifie les paramètres de matériau pour le modèle d’éclairage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*se* 
</dt> <dd>

Face ou faces mises à jour. Il doit s’agir de l’une des valeurs suivantes : recto GL, arrière-plan GL, arrière- \_ \_ plan GL \_ et GL \_ .

</dd> <dt>

*pname* 
</dt> <dd>

Paramètre de matériau à valeur unique de la face ou des visages mis à jour. Doit être une \_ éclat GL.



| Valeur                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_éclat GL**</dt> </dl> | Le paramètre *param* est un entier unique qui spécifie l’exposant spéculaire RVBA du matériau. Les valeurs entières sont mappées directement. Seules les valeurs de la plage \[ 0, 128 \] sont acceptées. L’exposant spéculaire par défaut pour les matériaux frontaux et à face arrière est 0. <br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Valeur à laquelle définir la brillance du GL de paramètres \_ .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                              | Signification                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>  | L’une des *visages* ou l' *pname* n’était pas une valeur acceptée.<br/>                |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | Un exposant spéculaire en dehors de la plage comprise entre \[ 0 et 128 \] a été spécifié.<br/> |



## <a name="remarks"></a>Notes

La fonction **glMateriali** affecte des valeurs aux paramètres de la documentation. Il existe deux ensembles de paramètres de matériau correspondants. L’un, le jeu de face *avant* , est utilisé pour ombrer des points, des lignes, des bitmaps et tous les polygones (lorsque l’éclairage à deux côtés est désactivé), ou simplement des polygones frontaux (lorsque l’éclairage à deux côtés est activé). L’autre jeu, *arrière-plan*, est utilisé pour ombrer les polygones de l’arrière-plan uniquement lorsque l’éclairage à deux côtés est activé. Reportez-vous à [**glLightModel**](gllightmodel-functions.md) pour plus d’informations sur les calculs d’éclairage unilatéraux et à deux côtés.

La fonction **glMateriali** accepte trois arguments. La première, *face*, spécifie si les documents \_ frontaux, les \_ documents de retour GL, ou \_ les \_ documents frontaux et Back GL \_ sont modifiés. Le deuxième, *pname*, spécifie quels paramètres dans un ou les deux jeux seront modifiés. Le troisième, *param*, spécifie la valeur qui sera assignée au paramètre spécifié.

Les paramètres de matériau sont utilisés dans l’équation d’éclairage qui est éventuellement appliquée à chaque vertex. L’équation est présentée dans [**glLightModel**](gllightmodel-functions.md).

Les paramètres de matériau peuvent être mis à jour à tout moment. En particulier, **glMateriali** peut être appelé entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md). Toutefois, si un seul paramètre de matériau doit être modifié par vertex, [**glColorMaterial**](glcolormaterial.md) est préférable à **glMateriali**.

La fonction suivante récupère des informations relatives à **glMateriali**:

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





