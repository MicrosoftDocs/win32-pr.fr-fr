---
title: inscription
description: inscription
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- inscrire le langage HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0102716529471b3e867e17b0e9b635274cdfc28ec603f239d66c76ffb0fdaa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983209"
---
# <a name="register"></a>inscription

Mot clé facultatif pour l’affectation d’une variable de nuanceur à un registre particulier, qui utilise la syntaxe suivante :



| : Register ( *\[ \_ profil \] de nuanceur*, *type sous- \# \[ composant \]* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>annuler
</dt> <dd>

Mot clé requis.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[Profil de nuanceur \_\]*
</dt> <dd>

[Profil de nuanceur](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)facultatif, qui peut être une cible de nuanceur ou simplement **PS** ou **vs**.

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Sous- \# \[ composant de type\]*
</dt> <dd>

Déclarer le type, le nombre et la déclaration de sous-composant.

-   Le type est l’un des éléments suivants :

    

    | Type | Inscrire la description       |
    |------|----------------------------|
    | b    | Mémoire tampon constante            |
    | t    | Mémoire tampon de texture et de texture |
    | c    | Décalage de la mémoire tampon              |
    | s    | Échantillonneur                    |
    | u    | Vue d’accès non ordonné      |

    

     

-   *\#* Numéro du Registre, qui est un nombre entier.
-   Le sous- *composant* est un nombre entier facultatif.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez ajouter une ou plusieurs assignations de Registre à la même déclaration de variable, séparées par des espaces.

Pour les variables Direct3D 10 dans la portée globale, le mot clé **Register** agit de la même manière que le mot clé [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .

## <a name="examples"></a>Exemples

Voici quelques exemples :


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe des variables](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 