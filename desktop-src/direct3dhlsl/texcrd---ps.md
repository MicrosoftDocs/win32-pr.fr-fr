---
title: texcrd-PS
description: Copie les données de coordonnée de texture du registre d’itérateur de coordonnées de texture source en tant que données de couleur dans le registre de destination.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990924"
---
# <a name="texcrd---ps"></a>texcrd-PS

Copie les données de coordonnée de texture du registre d’itérateur de coordonnées de texture source en tant que données de couleur dans le registre de destination.

## <a name="syntax"></a>Syntaxe



| texcrd DST, SRC |
|-----------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcrd                |      |      |      | x    |      |      |       |      |       |



 

Cette instruction interprète les données de coordonnée comme des données de couleur (RVBA).

Aucune texture n’est échantillonnée par cette instruction. Seules les coordonnées de texture définies pour cette étape de texture sont pertinentes.

Lorsque vous utilisez texcrd, gardez à l’esprit les détails suivants sur la façon dont les données sont copiées du Registre source vers le registre de destination. Le registre de coordonnées de texture source (t \# ) contient des données dans la plage \[ D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , tandis que le registre de destination (r \# ) peut contenir des données uniquement dans la plage (probablement plus petite) \[ -D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] . Notez que pour le nuanceur de pixels version 1 \_ , D3DCAPS9. PixelShader1xMaxValue doit avoir une valeur minimale de huit. L’instruction texcrd, en cours de verrouillage des données sources qui est hors limites du registre de destination, est susceptible de se comporter différemment sur un matériel différent. Le premier matériel nuanceur de pixels version 1 \_ 4 sur le marché exécutera une bride spéciale pour les valeurs en dehors de la plage. Ce collier est conçu pour produire un nombre pouvant tenir dans le registre de destination, mais également pour conserver le comportement d’adressage des textures pour les données hors limites (voir [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) si les données doivent être utilisées par la suite pour l’échantillonnage de texture. Toutefois, le nouveau matériel de différents fabricants peut ne pas présenter ce comportement et peut simplement détailler les données en fonction de la plage de registres de destination. Par conséquent, le plus sûr en ce qui concerne l’utilisation de nuanceur de pixels version 1 \_ texcrd consiste à fournir des données de coordonnée de texture uniquement dans le nuanceur de pixels qui se trouve déjà dans la plage \[ 8, 8 afin de ne \] pas compter sur la façon dont les brides matérielles s’appuient.

Contrairement à texcoord \_ , texcrd n’attache pas de valeurs comprises entre 0 et 1.

Règles d’utilisation de texcrd :

1.  Le même modificateur. xyz ou. XYW doit être appliqué à chaque lecture d’un registre t (n) individuel au sein d’une instruction texcrd ou texld.
2.  Le résultat du quatrième canal de texcrd est unset/non défini dans tous les cas.
3.  Le troisième canal est unset/non défini pour le cas XYW \_ DW.

## <a name="examples"></a>Exemples

L’ensemble complet de syntaxe autorisée pour texcrd, en tenant compte de toutes les combinaisons valides de modificateurs de source/sélecteur et de masque d’écriture de destination, est illustré ci-dessous. Notez que la notation. RVBA et. XYZW peut être utilisée de façon interchangeable.

Copie les trois premiers canaux du registre des itérateurs de coordonnées de texture, t (n), dans r (m). Le quatrième canal de r (m) n’est pas initialisé.


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



Place les premier, deuxième et quatrième composants de t (n) dans les trois premiers canaux de r (m). Le quatrième canal de r (m) n’est pas initialisé.


```
texcrd  r(m).rgb, t(n).xyw
```



Voici un exemple de division projective qui utilise le \_ modificateur DW.

Cet exemple copie x/w et y/w de t (n) dans les deux premiers canaux de r (m). Les troisième et quatrième canaux de r (m) ne sont pas initialisés. Toutes les données précédemment écrites sur le troisième canal de r (m) seront perdues. Les données du quatrième canal r (m) sont perdues en raison du marqueur de phase. Pour la version 1 \_ 4, l' \_ indicateur D3DTTFF projeté est ignoré.


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 