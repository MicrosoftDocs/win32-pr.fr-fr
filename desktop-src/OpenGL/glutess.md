---
title: gluTessCallback, fonction (Glu. h)
description: La fonction gluTessCallback définit un rappel pour un objet pavage.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- gluTessCallback fonction OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942736"
---
# <a name="glutesscallback-function"></a>gluTessCallback fonction)

La fonction **gluTessCallback** définit un rappel pour un objet pavage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tess* 
</dt> <dd>

Objet de pavage (créé avec [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*et* 
</dt> <dd>

Rappel en cours de définition. Les valeurs suivantes sont valides : GLU \_ Tess \_ Begin, Glu \_ Tess \_ Begin \_ Data, GLU \_ Tess \_ Edge \_ indicateur, Glu Tess \_ \_ Edge \_ Flag \_ Data, Glu \_ Tess \_ vertex, GLU \_ Tess \_ Vertex Data, Glu Tess end, Glu Tess \_ \_ \_ \_ \_ End \_ Data, Glu \_ Tess \_ combine, Glu \_ Tess \_ combine Data, Glu Tess \_ \_ \_ Error et Glu \_ Tess \_ Error \_ Data.

Pour plus d’informations sur ces rappels, consultez la section Notes suivante.

</dd> <dt>

*FN* 
</dt> <dd>

Fonction à appeler.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez **gluTessCallback** pour spécifier un rappel à utiliser par un objet de pavage. Si le rappel spécifié est déjà défini, il est remplacé. Si *FN* a la **valeur null**, le rappel existant devient non défini.

L’objet pavage utilise ces rappels pour décrire comment un polygone que vous spécifiez est divisé en triangles.

Il existe deux versions de chaque rappel, une avec les données Polygon que vous pouvez définir et une autre sans. Si les deux versions d’un rappel particulier sont spécifiées, le rappel avec les données Polygon que vous spécifiez sera utilisé. Le paramètre de *\_ données Polygon* de [**gluTessBeginPolygon**](glutessbeginpolygon.md) est une copie du pointeur qui a été spécifié lors de l’appel de **gluTessBeginPolygon** .

Les rappels valides sont les suivants :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rappel</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GLU_TESS_BEGIN</td>
<td>Le rappel GLU_TESS_BEGIN est appelé comme <a href="glbegin.md"><strong>glBegin</strong></a> pour indiquer le début d’une primitive (triangle). La fonction accepte un seul argument de type <strong>GLenum</strong>. Si vous affectez à la propriété GLU_TESS_BOUNDARY_ONLY la valeur GL_FALSE, l’argument est défini sur GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP ou GL_TRIANGLES. Si vous affectez à la propriété GLU_TESS_BOUNDARY_ONLY la valeur GL_TRUE, l’argument est défini sur GL_LINE_LOOP. Le prototype de fonction pour ce rappel est le suivant : <strong>void</strong> <strong>Begin</strong> ( <em>type</em><strong>GLenum</strong> );<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_BEGIN_DATA</td>
<td>GLU_TESS_BEGIN_DATA est le même que le rappel GLU_TESS_BEGIN, sauf qu’il accepte un argument de pointeur supplémentaire. Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_EDGE_FLAG</td>
<td>Le rappel GLU_TESS_EDGE_FLAG est semblable à <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>. La fonction accepte un seul indicateur booléen qui indique les bords situés sur la limite du polygone. Si l’indicateur est GL_TRUE, chaque vertex qui suit commence un bord qui se trouve sur la limite du polygone ; autrement dit, une arête qui sépare une région intérieure d’une région extérieure. Si l’indicateur est GL_FALSE, chaque sommet qui suit commence un bord qui se trouve dans l’intérieur du polygone. Le rappel GLU_TESS_EDGE_FLAG (s’il est défini) est appelé avant le premier rappel de vertex. Étant donné que les ventilateurs et les facettes de triangle ne prennent pas en charge les indicateurs de périphérie, le rappel de début n’est pas appelé avec GL_TRIANGLE_FAN ou GL_TRIANGLE_STRIP si un rappel de l’indicateur Edge est fourni. Au lieu de cela, les ventilateurs et les bandes sont convertis en triangles indépendants. Le prototype de fonction pour ce rappel est le suivant :<br/> <strong>void</strong> <strong>edgeFlag</strong> (<strong></strong> <em>indicateur</em>GLboolean);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_EDGE_FLAG_DATA</td>
<td>Le rappel GLU_TESS_EDGE_FLAG_DATA est le même que le rappel GLU_TESS_EDGE_FLAG, sauf qu’il accepte un argument de pointeur supplémentaire. Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>Flag</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_VERTEX</td>
<td>Le rappel GLU_TESS_VERTEX est appelé entre les rappels Begin et end. Elle est similaire à glVertex et définit les sommets des triangles créés par le processus de pavage. La fonction prend un pointeur comme seul argument. Ce pointeur est identique au pointeur opaque que vous avez fourni lorsque vous avez défini le vertex (voir <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>). Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> * <em>vertex_data</em>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_VERTEX_DATA</td>
<td>Le GLU_TESS_VERTEX_DATA est le même que le rappel GLU_TESS_VERTEX, sauf qu’il accepte un argument de pointeur supplémentaire. Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Le prototype de fonction pour ce rappel est : <strong>void</strong>  <strong>vertexData</strong> (void * <em>vertex_data</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_END</td>
<td>Le rappel GLU_TESS_END a le même objectif que <a href="glend.md"><strong>glEnd</strong></a>. Elle indique la fin d’une primitive et n’accepte aucun argument. Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>end</strong> (<strong>void</strong>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_END_DATA</td>
<td>Le rappel GLU_TESS_END_DATA est le même que le rappel GLU_TESS_END, sauf qu’il accepte un argument de pointeur supplémentaire. Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>endData</strong> (<strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_COMBINE</td>
<td>Appelez le rappel GLU_TESS_COMBINE pour créer un nouveau vertex lorsque le pavage détecte une intersection ou pour fusionner des fonctionnalités. La fonction accepte quatre arguments : un tableau de trois éléments, chacun de type Gldouble.<br/> Tableau de quatre pointeurs.<br/> Tableau de quatre éléments, chacun de type GLfloat.<br/> Pointeur vers un pointeur.<br/> Le prototype de fonction pour ce rappel est le suivant : <br/> <strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>CoOrds</em>[3], <strong>void</strong> * <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>out  ** <em>Data</em>);<br/> Le vertex est défini comme une combinaison linéaire de jusqu’à quatre sommets existants, stockés dans vertex_data. Les coefficients de la combinaison linéaire sont fournis par poids ; ces pondérations sont toujours additionnées à 1,0. Tous les pointeurs de vertex sont valides même si certains des poids sont nuls. Le paramètre coords indique l’emplacement du nouveau vertex.<br/> Allouez un autre vertex, interpolez les paramètres à l’aide de la vertex_data et du poids, puis retournez le nouveau pointeur de vertex dans les données de données. Ce handle est fourni lors du rendu des rappels. Libérez de la mémoire après avoir appelé <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.<br/> Par exemple, si le polygone se trouve dans un plan arbitraire dans l’espace tridimensionnel et que vous associez une couleur à chaque vertex, le rappel GLU_TESS_COMBINE peut se présenter comme suit :<br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
Lorsque le pavage détecte une intersection, le rappel GLU_TESS_COMBINE ou GLU_TESS_COMBINE_DATA (voir ci-dessous) doit être défini et doit écrire un pointeur non<strong>null</strong> dans dataOut. Dans le cas contraire, l’erreur GLU_TESS_NEED_COMBINE_CALLBACK se produit et aucune sortie n’est générée. (Il s’agit de la seule erreur qui peut se produire pendant le pavage et le rendu.)<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_COMBINE_DATA</td>
<td>Le rappel GLU_TESS_COMBINE_DATA est le même que le rappel GLU_TESS_COMBINE, sauf qu’il accepte un argument de pointeur supplémentaire. Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>CoOrds</em>[3] <strong>, void</strong> *<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  ** <em>UNdata</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_ERROR</td>
<td>Le rappel GLU_TESS_ERROR est appelé lorsqu’une erreur est rencontrée. L’argument est de type <strong>GLenum</strong>; elle indique l’erreur spécifique qui s’est produite et est définie sur l’une des valeurs suivantes : GLU_TESS_MISSING_BEGIN_POLYGON<br/> GLU_TESS_MISSING_END_POLYGON<br/> GLU_TESS_MISSING_BEGIN_CONTOUR<br/> GLU_TESS_MISSING_END_CONTOUR<br/> GLU_TESS_COORD_TOO_LARGE<br/> GLU_TESS_NEED_COMBINE_CALLBACK<br/> Appelez gluErrorString pour récupérer les chaînes de caractères décrivant ces erreurs. Le prototype de fonction pour ce rappel est le suivant :<br/> <strong>void</strong> <strong>Error</strong> (<strong>GLenum</strong> <em>errno</em>);<br/> La bibliothèque GLU récupère les quatre premières erreurs en insérant l’appel ou les appels manquants. GLU_TESS_COORD_TOO_LARGE indique que certaines coordonnées de vertex dépassent la constante prédéfinie GLU_TESS_MAX_COORD en valeur absolue et que la valeur a été ancrée. (Les valeurs de coordonnée doivent être suffisamment petites pour que deux puissent être multipliées sans dépassement de capacité.) GLU_TESS_NEED_COMBINE_CALLBACK indique que la pavage a détecté une intersection entre deux bords dans les données d’entrée, et que le rappel GLU_TESS_COMBINE ou GLU_TESS_COMBINE_DATA n’a pas été fourni. Aucune sortie ne sera générée.<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_ERROR_DATA</td>
<td>Le rappel GLU_TESS_ERROR_DATA est le même que le rappel GLU_TESS_ERROR, sauf qu’il accepte un argument de pointeur supplémentaire. Ce pointeur est identique au pointeur opaque fourni lorsque vous appelez <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Le prototype de fonction pour ce rappel est : <strong>void</strong> <strong>ErrorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
</tbody>
</table>



 

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> <dt>

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





