---
title: ps
description: Cette instruction spécifie le numéro de version du nuanceur et fonctionne sur toutes les versions de nuanceur.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06e070c16c482038097245325d884ef6b71d2249afb2aa89ad5ec1d37f86c9e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906346"
---
# <a name="ps"></a>ps

Cette instruction spécifie le numéro de version du nuanceur et fonctionne sur toutes les versions de nuanceur.

## <a name="syntax"></a>Syntaxe


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a>Arguments d’entrée

Les arguments d’entrée contiennent un seul numéro de version principale avec un numéro de sous-version unique. Les combinaisons autorisées sont répertoriées dans le tableau ci-dessous.



| Versions principales | Sous-versions                   |
|---------------|--------------------------------|
| 1             | 1, 2, 3, 4                     |
| 2             | 0, x (étendu), SW (logiciel) |
| 3             | 0, SW (logiciel)               |



 

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| ps                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Cette instruction doit être la première instruction sans commentaire dans un nuanceur de pixels.

Les versions à accélération matérielle du logiciel (versions sans \_ logiciel dans le numéro de version) peuvent traiter les vertex avec le matériel accelearation ou utiliser le traitement des vertex logiciels. Les versions de logiciels (versions avec \_ SW dans le numéro de version) traitent les vertex uniquement avec le logiciel.

## <a name="examples"></a>Exemples

Cet exemple partiel déclare un nuanceur de pixels de la version 1 \_ .


```
ps_1_1
```



Cet exemple partiel déclare un nuanceur de pixels de la version 1 \_ .


```
ps_1_4
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




