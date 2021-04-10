---
title: fonction glBegin (GL. h)
description: Les fonctions glBegin et Glend délimitent les vertex d’une primitive ou d’un groupe de primitives similaires. | fonction glBegin (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- glBegin fonction OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953672"
---
# <a name="glbegin-function"></a>glBegin fonction)

Les fonctions **glBegin** et [**Glend**](glend.md) délimitent les vertex d’une primitive ou d’un groupe de primitives similaires.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Primitives ou primitives qui seront créées à partir des vertex présentés entre les **glBegin** et les [**Glend**](glend.md)suivants. Les constantes symboliques acceptées et leurs significations sont les suivantes :



| Valeur                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**POINTS du GL \_**</dt> </dl>                          | Traite chaque vertex comme un point unique. Le vertex *n* définit le point *n*. *N* points sont dessinés.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**\_lignes GL**</dt> </dl>                             | Traite chaque paire de vertex comme un segment de ligne indépendant. Vertex *2n-1* et *2n* définir la ligne *n*. Les lignes *N/2* sont dessinées.<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**\_bande de lignes GL \_**</dt> </dl>             | Dessine un groupe connecté de segments de ligne du premier vertex au dernier. Les vertex *n* et *n + 1* définissent la ligne *n*. *N-1* lignes sont dessinées.<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**\_boucle de lignes GL \_**</dt> </dl>                | Dessine un groupe connecté de segments de ligne à partir du premier vertex jusqu’au dernier, puis de nouveau vers le premier. Les vertex *n* et *n + 1* définissent la ligne *n*. La dernière ligne, toutefois, est définie par les vertex *N* et *1*. *N* lignes sont dessinées.<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**\_TRIangles GL**</dt> </dl>                 | Traite chaque triplet de vertex comme un triangle indépendant. Vertex *3n-2*, *3n-1* et *3N* définissent le triangle *n*. Les triangles *N/3* sont dessinés.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**\_bande triangulaire GL \_**</dt> </dl> | Dessine un groupe de triangles connecté. Un triangle est défini pour chaque vertex présenté après les deux premiers sommets. Pour *n*, les vertex *n*, *n + 1* et *n + 2* définissent le triangle *n*. Pour *n*, les sommets *n + 1*, *n* et *n + 2* définissent le triangle *n*. Les triangles *N-2* sont dessinés.<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**\_ventilateur à triangles GL \_**</dt> </dl>       | Dessine un groupe de triangles connecté. un triangle est défini pour chaque vertex présenté après les deux premiers sommets. Vertex *1*, *n + 1*, *n + 2* définissent le triangle *n*. Les triangles *N-2* sont dessinés.<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**à \_ quatre processeurs GL**</dt> </dl>                             | Traite chaque groupe de quatre vertex comme un quadrangulaires indépendant. Vertex *4n-3*, *4N-2*, *4N-1* et *4N* définir quadrangulaires *n*. Les quadrilatères *N/4* sont dessinés.<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**à \_ quatre \_ bandes GL**</dt> </dl>             | Dessine un groupe connecté de quadrilatères. Un quadrangulaires est défini pour chaque paire de vertex présentée après la première paire. Les vertex *2n-1* *, 2n,* *2n + 2* et *2n + 1* définissent quadrangulaires *n*. *N/2-1* quadrilatères sont dessinés. Notez que l’ordre dans lequel les vertex sont utilisés pour construire un quadrangulaires à partir de données de bandes est différent de celui utilisé avec les données indépendantes.<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**Polygone du GL \_**</dt> </dl>                       | Dessine un polygone unique et convexe. Les vertex *1* à *N* définissent ce polygone.<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mode* a été défini sur une valeur non acceptée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | Une fonction autre que [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [GlEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)ou [**glCallLists**](glcalllists.md) a été appelée entre **glBegin** et le [**Glend**](glend.md)correspondant. La fonction **Glend** a été appelée avant l’appel de la méthode **glBegin** correspondante, ou **glBegin** a été appelée dans une  / séquence **Glend** glBegin. <br/> |



## <a name="remarks"></a>Notes

Les fonctions **glBegin** et [**Glend**](glend.md) délimitent les vertex qui définissent une primitive ou un groupe de primitives similaires. La fonction **glBegin** accepte un argument unique qui spécifie laquelle des dix primitives compose les sommets. En acceptant *n* comme nombre entier à partir de 1, et *n* comme nombre total de vertex spécifiés, les interprétations sont les suivantes :

-   Vous ne pouvez utiliser qu’un sous-ensemble de fonctions OpenGL entre **glBegin** et [**Glend**](glend.md). Les fonctions que vous pouvez utiliser sont les suivantes :

    [**glVertex**](glvertex-functions.md)

     

    [**glColor**](glcolor-functions.md)

     

    [**glIndex**](glindex-functions.md)

     

    [**glNormal**](glnormal-functions.md)

     

    [**glTexCoord**](gltexcoord-functions.md)

     

    [**glEvalCoord**](glevalcoord-functions.md)

     

    [**glEvalPoint**](glevalpoint.md)

     

    [**glMaterial**](glmaterial-functions.md)

     

    [**glEdgeFlag**](gledgeflag-functions.md)

    Vous pouvez également utiliser [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) pour exécuter des listes d’affichage qui incluent uniquement les fonctions précédentes. Si une autre fonction OpenGL est appelée entre **glBegin** et [**Glend**](glend.md), l’indicateur d’erreur est défini et la fonction est ignorée.

-   Quelle que soit la valeur choisie pour *mode* dans **glBegin**, il n’y a aucune limite au nombre de vertex que vous pouvez définir entre **glBegin** et [**Glend**](glend.md). Les lignes, triangles, quadrilatères et polygones qui ne sont pas complets spécifiés ne sont pas dessinés. Les résultats de spécifications sont incomplets lorsqu’un nombre trop faible de vertex est fourni pour spécifier une seule primitive ou lorsqu’un multiple de vertex incorrect est spécifié. La primitive incomplète est ignorée ; les primitives complètes sont dessinées.
-   La spécification minimale des vertex pour chaque primitive est la suivante : 

    | Nombre minimal de vertex | Type de primitive |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | triangle          |
    | 4                          | quadrangulaires     |
    | 3                          | polygon           |

    

     

-   Les modes qui requièrent un certain nombre de vertex sont les lignes de GL \_ (2), les \_ triangles GL (3), \_ les quads GL (4) et le GL \_ Quad \_ Strip (2).

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](/windows/desktop/OpenGL/glend)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

