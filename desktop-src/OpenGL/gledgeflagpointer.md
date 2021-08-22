---
title: fonction glEdgeFlagPointer (GL. h)
description: La fonction glEdgeFlagPointer définit un tableau d’indicateurs de bord.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- glEdgeFlagPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa648a15542a3f3f2f35f577760991da74bc978c0464c1373c8eddea38941a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061637"
---
# <a name="gledgeflagpointer-function"></a>glEdgeFlagPointer fonction)

La fonction **glEdgeFlagPointer** définit un tableau d’indicateurs de bord.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*progrès* 
</dt> <dd>

Décalage d’octet entre les indicateurs de bord consécutifs. Lorsque la valeur de *Stride* est égale à zéro, les indicateurs de périphérie sont étroitement empaquetés dans le tableau.

</dd> <dt>

*pointeur* 
</dt> <dd>

Pointeur vers le premier indicateur de bord dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                             | Signification                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl> | *Stride* ou *Count* était négatif.<br/> |



## <a name="remarks"></a>Remarques

La fonction **glEdgeFlagPointer** spécifie l’emplacement et les données d’un tableau d’indicateurs de bord booléen à utiliser lors du rendu. Le paramètre *Stride* détermine le décalage d’octets d’un indicateur de bord à l’autre, ce qui permet d’empaqueter des vertex et des attributs dans un tableau unique ou un stockage dans des tableaux séparés. Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés.

Un tableau d’indicateurs de bord est activé quand vous spécifiez \_ la \_ \_ constante de tableau d’indicateurs de périphérie GL avec [**glEnableClientState**](glenableclientstate.md). Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md) ou [**glArrayElement**](glarrayelement.md) utilise le tableau d’indicateurs de bord. Par défaut, le tableau d’indicateurs de bord est désactivé.

Utilisez **glDrawArrays** pour construire une séquence de primitives (du même type) à partir de tableaux d’attributs vertex et vertex prédéfinis. Utilisez **glArrayElement** pour spécifier des primitives en indexant des vertex et des attributs de vertex, et [**glDrawElements**](gldrawelements.md) pour construire une séquence de primitives en indexant des vertex et des attributs de vertex.

Vous ne pouvez pas inclure des **glEdgeFlagPointer** dans des listes d’affichage.

Lorsque vous spécifiez un tableau d’indicateurs de bord à l’aide de **glEdgeFlagPointer**, les valeurs de tous les paramètres de tableau de l’indicateur de bord de la fonction sont enregistrées dans un État côté client et les éléments de tableau statique peuvent être mis en cache. Étant donné que les paramètres de tableau de l’indicateur de bord sont dans un État côté client, [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) n’enregistrent ni ne restaurent leurs valeurs.

Bien que l’appel de **glEdgeFlagPointer** dans une paire de [](glbegin.md) / [**Glend**](glend.md) glBegin ne génère pas d’erreur, les résultats ne sont pas définis.

Les fonctions suivantes récupèrent les informations relatives à la fonction **glEdgeFlagPointer** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Edge \_ indicateur \_ tableau \_ Stride

**glGet** avec argument valeur de tableau de l' \_ \_ indicateur de périphérie du \_ GL \_

[**glGetPointerv**](glgetpointerv.md) avec argument du \_ pointeur de tableau de l’indicateur de bord GL \_ \_ \_

[**glIsEnabled**](glisenabled.md) avec argument du \_ \_ tableau d’indicateurs de périphérie du GL \_

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





