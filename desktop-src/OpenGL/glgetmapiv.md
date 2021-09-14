---
title: fonction glGetMapiv (GL. h)
description: Les fonctions glGetMapdv, glGetMapfv et glGetMapiv retournent les paramètres de l’évaluateur. | fonction glGetMapiv (GL. h)
ms.assetid: bc055451-7c20-4a8a-96dd-55c877700714
keywords:
- glGetMapiv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetMapiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fc8bf74a80916434f806e2e1f46b633b7243e61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229499"
---
# <a name="glgetmapiv-function"></a>glGetMapiv fonction)

Les fonctions [**glGetMapdv**](glgetmapdv.md), [**glGetMapfv**](glgetmapfv.md)et **glGetMapiv** retournent les paramètres de l’évaluateur.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetMapiv(
   GLenum target,
   GLenum query,
   GLint  *v
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Nom symbolique d’une carte. Les valeurs acceptées sont les suivantes : GL \_ Map1 \_ couleur \_ 4, \_ index GL Map1 \_ , GL \_ Map1 \_ normal, GL \_ Map1 \_ texture \_ Coord \_ 1, GL \_ Map1 \_ texture \_ Coord \_ 2, GL \_ Map1 \_ texture \_ Coord \_ 3, GL \_ Map1 \_ texture \_ Coord \_ 4, GL \_ Map1 \_ vertex \_ 3, GL \_ Map1 \_ vertex \_ 4, GL map2 couleur 4, GL map2 index, GL map2 normal, GL map2 texture Coord 1, GL map2 texture Coord \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 2, GL map2 texture Coord \_ \_ \_ \_ \_ \_ \_ \_ 3, GL \_ map2 texture Coord \_ \_ \_ 4, GL \_ map2 \_ vertex \_ 3 et GL \_ map2 \_ vertex \_ 4.

</dd> <dt>

*query* 
</dt> <dd>

Spécifie le paramètre à retourner. Les noms symboliques suivants sont acceptés.



| Valeur                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**\_Coeff GL**</dt> </dl>    | Le paramètre *v* retourne les points de contrôle de la fonction évaluateur. Les évaluateurs unidimensionnels retournent des points de contrôle d' *ordre* et les évaluateurs à deux dimensions retournent des points de contrôle *uorder* *x* *Vorder* . Chaque point de contrôle est constitué d’un, deux, trois ou quatre valeurs à virgule flottante, à virgule flottante simple précision ou à virgule flottante double précision, selon le type de l’évaluateur. Les points de contrôle à deux dimensions sont retournés dans l’ordre ligne-principal, ce qui incrémente rapidement l’index *uorder* et l’index *Vorder* après chaque ligne. Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant les valeurs à virgule flottante internes aux valeurs entières les plus proches.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**\_commande GL**</dt> </dl>    | Le paramètre *v* retourne l’ordre de la fonction évaluateur. Les évaluateurs unidimensionnels retournent une valeur unique, *Order*. Les évaluateurs à deux dimensions retournent deux valeurs, *uorder* et *Vorder*.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**\_domaine GL**</dt> </dl> | Le paramètre *v* retourne les paramètres de mappage linéaires *u* et *v* . Les évaluateurs unidimensionnels retournent deux valeurs, *u* 1 et *u* 2, comme spécifié par [**glMap1**](glmap1.md). Les évaluateurs à deux dimensions retournent quatre valeurs (*U1*, *U2*, *v1* et *v2*), comme spécifié par [**glMap2**](glmap2.md). Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant les valeurs à virgule flottante internes aux valeurs entières les plus proches.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*v* 
</dt> <dd>

Retourne les données demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible* ou la *requête* n’était pas une valeur acceptée.<br/>                                                                             |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Les fonctions **glGetMap** retournent les paramètres de l’évaluateur. (Les fonctions **glMap1** et **glMap2** définissent les évaluateurs.) Le paramètre *target* spécifie un mappage, la *requête* sélectionne un paramètre spécifique, et *v* pointe vers le stockage où les valeurs sont retournées.

Les valeurs acceptables pour le paramètre *target* sont décrites dans [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md).

Si une erreur est générée, aucune modification n’est apportée au contenu de *v*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





