---
title: vs
description: Cette instruction spécifie le numéro de version du nuanceur. Cette instruction fonctionne sur toutes les versions de nuanceur.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381223"
---
# <a name="vs"></a>vs

Cette instruction spécifie le numéro de version du nuanceur. Cette instruction fonctionne sur toutes les versions de nuanceur.

## <a name="syntax"></a>Syntaxe


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a>Arguments d’entrée

Les arguments d’entrée contiennent un seul numéro de version principale avec un numéro de sous-version unique. Les combinaisons autorisées sont répertoriées dans le tableau ci-dessous.



| Versions principales | Sous-versions                   |
|---------------|--------------------------------|
| 1             | 1                              |
| 2             | 0, SW (logiciel), x (étendu) |
| 3             | 0, SW (logiciel)               |



 

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| vs                     | x    | x    | x    | x     | x    | x     |



 

Cette instruction doit être la première instruction sans commentaire dans un nuanceur de sommets.

Cette instruction est prise en charge dans toutes les versions de nuanceur de vertex.

Les versions à accélération matérielle du logiciel (versions sans \_ logiciel dans le numéro de version) peuvent traiter les vertex avec le matériel accelearation ou utiliser le traitement des vertex logiciels. Les versions de logiciels (versions avec \_ SW dans le numéro de version) traitent les vertex uniquement avec le logiciel.

## <a name="examples"></a>Exemples

Cet exemple partiel déclare un \_ nuanceur vertex version 1 1.


```
vs_1_1
```



Cet exemple partiel déclare un nuanceur vertex de la version 2.


```
vs_2_sw
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




