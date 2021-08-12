---
title: fonction glEnd (GL. h)
description: Les fonctions glBegin et Glend délimitent les vertex d’une primitive ou d’un groupe de primitives similaires. | fonction glEnd (GL. h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- glEnd fonction OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0817bec7874b9a3a58e28653ff10497eb1e3f5e5170c57dbe2c26a6b20b64460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616551"
---
# <a name="glend-function"></a>glEnd fonction)

Les fonctions [**glBegin**](glbegin.md) et **Glend** délimitent les vertex d’une primitive ou d’un groupe de primitives similaires.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | Une fonction autre que **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **GlEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList** ou **glCallLists** a été appelée entre **glBegin** et le **glEnd** correspondant. La fonction **glEnd** a été appelée avant l’appel de la méthode **glBegin** correspondante, ou **glBegin** a été appelée dans une  / séquence **glEnd** glBegin. <br/> |



## <a name="remarks"></a>Remarques

Les fonctions [**glBegin**](glbegin.md) et **Glend** délimitent les vertex qui définissent une primitive ou un groupe de primitives similaires. La fonction **glBegin** accepte un argument unique qui spécifie laquelle des dix primitives compose les sommets. En acceptant *n* comme nombre entier à partir de 1, et *n* comme nombre total de vertex spécifiés, les interprétations sont les suivantes :

-   Vous ne pouvez utiliser qu’un sous-ensemble de fonctions OpenGL entre **glBegin** et **glEnd**. Les fonctions que vous pouvez utiliser sont les suivantes :

    -   [**glVertex**](glvertex-functions.md)
    -   [**glColor**](glcolor-functions.md)
    -   [**glIndex**](glindex-functions.md)
    -   [**glNormal**](glnormal-functions.md)
    -   [**glTexCoord**](gltexcoord-functions.md)
    -   [**glEvalCoord**](glevalcoord-functions.md)
    -   [**glEvalPoint**](glevalpoint.md)
    -   [**glMaterial**](glmaterial-functions.md)
    -   [**glEdgeFlag**](gledgeflag-functions.md)

    Vous pouvez également utiliser [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) pour exécuter des listes d’affichage qui incluent uniquement les fonctions précédentes. Si une autre fonction OpenGL est appelée entre **glBegin** et **glEnd**, l’indicateur d’erreur est défini et la fonction est ignorée.

-   Quelle que soit la valeur choisie pour *mode* dans **glBegin**, il n’y a aucune limite au nombre de vertex que vous pouvez définir entre **glBegin** et **glEnd**. Les lignes, triangles, quadrilatères et polygones qui ne sont pas complets spécifiés ne sont pas dessinés. Les résultats de spécifications sont incomplets lorsqu’un nombre trop faible de vertex est fourni pour spécifier une seule primitive ou lorsqu’un multiple de vertex incorrect est spécifié. La primitive incomplète est ignorée ; les primitives complètes sont dessinées.
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

[**glBegin**](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
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

 

