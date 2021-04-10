---
title: fonction glGetString (GL. h)
description: La fonction glGetString retourne une chaîne décrivant la connexion OpenGL actuelle.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- glGetString fonction OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942739"
---
# <a name="glgetstring-function"></a>glGetString fonction)

La fonction **glGetString** retourne une chaîne décrivant la connexion OpenGL actuelle.

## <a name="syntax"></a>Syntaxe


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*name* 
</dt> <dd>

L’une des constantes symboliques suivantes.



| Valeur                                                                                                                                                         | Signification                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <dt>**fournisseur du GL \_**</dt> </dl>             | Retourne la société responsable de cette implémentation OpenGL. Ce nom ne passe pas de Release à Release.<br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <dt>**\_convertisseur GL**</dt> </dl>       | Retourne le nom du convertisseur. Ce nom est généralement spécifique à une configuration particulière d’une plateforme matérielle. Il ne passe pas de Release à Release.<br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <dt>**VERSION du GL \_**</dt> </dl>          | Retourne un numéro de version ou de version.<br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <dt>**EXTENSIONS du GL \_**</dt> </dl> | Retourne une liste séparée par des espaces des extensions prises en charge par OpenGL.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *nom* n’est pas une valeur acceptée.<br/>                                                                                          |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glGetString** retourne un pointeur vers une chaîne statique décrivant certains aspects de la connexion OpenGL actuelle.

Comme OpenGL n’inclut pas de requêtes pour les caractéristiques de performances d’une implémentation, il est prévu que certaines applications soient écrites pour reconnaître les plateformes connues et modifient leur utilisation de OpenGL en fonction des caractéristiques de performances connues de ces plateformes. Les chaînes fournisseur du GL \_ et \_ convertisseur GL regroupent de façon unique une plateforme, et ne changent pas d’une version à l’autres. Ils doivent être utilisés en tant que tels par les algorithmes de reconnaissance de plateforme.

Le format et le contenu de la chaîne retournée par **glGetString** dépendent de l’implémentation, à l’exception de :

-   Les noms d’extension n’incluent pas de caractères d’espace et seront séparés par des espaces dans la \_ chaîne d’extensions GL.
-   La chaîne de version du GL \_ commence par un numéro de version. Le numéro de version utilise l’une des formes suivantes :

    *\_ nombre majeur*. *\_ nombre mineur*

    *\_ nombre majeur*. *\_ nombre mineur*. *\_ numéro de version*

-   Les informations spécifiques au fournisseur peuvent suivre le numéro de version. Son format dépend de l’implémentation, mais un espace sépare toujours le numéro de version et les informations spécifiques au fournisseur.
-   Toutes les chaînes se terminent par un caractère null.

Si une erreur est générée, **glGetString** retourne zéro.

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





