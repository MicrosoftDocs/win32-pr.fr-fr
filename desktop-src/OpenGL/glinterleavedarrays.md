---
title: fonction glInterleavedArrays (GL. h)
description: La fonction glInterleavedArrays spécifie et active simultanément plusieurs tableaux entrelacés dans un plus grand tableau d’agrégats.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- glInterleavedArrays fonction OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3b37186614fa431585c1e5a932edab946afd6d881ba1cf8eb5c5690220f603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938560"
---
# <a name="glinterleavedarrays-function"></a>glInterleavedArrays fonction)

La fonction **glInterleavedArrays** spécifie et active simultanément plusieurs tableaux entrelacés dans un plus grand tableau d’agrégats.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*format* 
</dt> <dd>

Type de tableau à activer. Le paramètre peut prendre l’une des valeurs symboliques suivantes : GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL C4F N3F V3F, \_ \_ \_ GL \_ T2F \_ V3F, GL \_ T4F \_ V4F, GL \_ T2F \_ C4UB \_ V3F, GL T2F C3F V3F, GL T2F N3F V3F \_ \_ \_ \_ \_ \_ , GL \_ T2F \_ C4F N3F V3F \_ \_ ou GL \_ T4F \_ \_ \_ C4F N3F V4F.

</dd> <dt>

*progrès* 
</dt> <dd>

Offset, en octets, entre chaque élément de tableau d’agrégation.

</dd> <dt>

*pointeur* 
</dt> <dd>

Pointeur vers le premier élément d’un tableau d’agrégats.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *format* n’est pas une valeur acceptée.<br/>                                                                                        |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *Stride* était une valeur négative.<br/>                                                                                             |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

Avec la fonction **glInterleavedArrays** , vous pouvez spécifier et activer simultanément plusieurs tableaux de couleur, de texture normale, de texture et de vertex entrelacés dont les éléments font partie d’un élément de tableau d’agrégats plus grand. Pour certaines architectures de mémoire, cette solution est plus efficace que la spécification des tableaux séparément.

Si le paramètre *Stride* est égal à zéro, les éléments de tableau d’agrégation sont stockés consécutivement ; Sinon, les octets *Stride* se produisent entre les éléments du tableau d’agrégation.

Le paramètre de *format* sert de clé qui décrit comment extraire des tableaux individuels du tableau d’agrégats :

-   Si le *format* contient un T, les coordonnées de texture sont extraites du tableau entrelacé.
-   Si C est présent, les valeurs de couleur sont extraites.
-   Si N est présent, les coordonnées normales sont extraites.
-   Les coordonnées de vertex sont toujours extraites.
-   Les chiffres 2, 3 et 4 désignent le nombre de valeurs extraites.
-   F indique que les valeurs sont extraites en tant que valeurs à virgule flottante.
-   Si 4UB suit le C, les couleurs peuvent également être extraites sous forme de 4 octets non signés. Si une couleur est extraite sous la forme de 4 octets non signés, l’élément de tableau de vertex qui suit se trouve à la première adresse alignée à virgule flottante possible.

Si vous appelez **glInterleavedArrays** lors de la compilation d’une liste d’affichage, celle-ci n’est pas compilée dans la liste mais est exécutée immédiatement.

Vous ne pouvez pas inclure d’appels à **glInterleavedArrays** dans **glDisableClientState** entre les appels à [**glBegin**](glbegin.md) et l’appel correspondant à **glEnd**.

> [!Note]  
> La fonction **glInterleavedArrays** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

La fonction **glInterleavedArrays** est implémentée côté client sans protocole. Étant donné que les paramètres du tableau de vertex sont des États côté client, ils ne sont pas enregistrés ou restaurés par [**glPushAttrib**](glpushattrib.md) et **glPopAttrib**. Utilisez [**glPushClientAttrib**](glpushclientattrib.md) et **glPopClientAttrib** à la place.

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





