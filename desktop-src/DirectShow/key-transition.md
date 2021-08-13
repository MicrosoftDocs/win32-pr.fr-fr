---
description: Transition de clé
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transition de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fc5b905b1650b6db6bb98b542193160825b8bd6dd74626ef9bddc91b118118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397274"
---
# <a name="key-transition"></a>Transition de clé

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La transition de clé effectue la génération de clés en fonction de la valeur RVB, de la valeur alpha, de la teinte ou de la luminance.

L’illustration suivante montre la transition de clé :

![transition de clé](images/trans-key.png)

ID de classe (CLSID) : {C5B19592-145E-11D3-9F04-006008039E37}

Nom de la variable CLSID : CLSID \_ DxtKey

Nom convivial : « DxtKey »

Propriétés



| Propriété   | Type  | Plage valide           | Description                                                                                                                                                                                                                                                | S'applique à                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Teinte        | int   | 0 – 360                 | Valeur de teinte sur laquelle la clé doit être ajoutée.                                                                                                                                                                                                                             | Teinte                            |
| Inverser :     | BOOL  | **False** ou **true** | Valeur booléenne indiquant si l’opération par défaut de la clé doit être inversée. Si la **valeur est false**, les pixels de l’image superposée sont rendus transparents par défaut. Si la **valeur est true**, l’opération est inversée.                                                   | Chroma, teinte, luminance, Nonred |
| KeyType    | int   | Voir les notes           | Spécifie le type de clé. Pour plus d'informations, consultez la section Notes.                                                                                                                                                                                              | Tous                            |
| Luminance  | int   | 0 – 100                 | Valeur de luminance sur laquelle la clé doit être ajoutée.                                                                                                                                                                                                                       | Luminance                      |
| RGB        | DWORD | 0x0 – 0xFFFFFF        | Couleur sur laquelle la clé doit être représentée. La valeur est un nombre hexadécimal au format 0x *RRVVBB*, où *RR* est la valeur rouge, *GG* est la valeur verte et *BB* est la valeur bleue. (Les couleurs pures rouge, vert et bleu sont 0xFF0000, 0x00FF00 et 0x0000FF, respectivement). | Chromatique                         |
| Similarité | int   | 0 – 100                 | Plage de données de couleur qui devient transparente. À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente.                                                                                                                                        | Chroma, Nonred                 |



 

## <a name="remarks"></a>Remarques

Le type de clé effectué dépend de la valeur de la propriété **KeyType** , qui doit être l’une des suivantes :



| Valeur | Énumération       | Description                                           |
|-------|-------------------|-------------------------------------------------------|
| 0     | DXTKEY \_ RGB       | Clé Chroma (clé par valeur RVB).                        |
| 1     | DXTKEY \_ NONRED    | Clé Nonred. (Rend les zones bleues et vertes transparentes.) |
| 2     | \_luminance DXTKEY | Clé de luminance.                                        |
| 3     | DXTKEY \_ alpha     | Clé par valeur alpha.                                   |
| 4     | DXTKEY \_ teinte       | Clé par teinte.                                           |



 

Par défaut, le type de clé est DXTKEY \_ alpha.

 

 



