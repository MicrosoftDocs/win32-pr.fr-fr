---
title: Nuanceurs de logiciels
description: Les nuanceurs de logiciels sont mis en œuvre pour permettre le développement de nuanceurs sans prise en charge du matériel sous-jacent. Ils prennent en charge l’ensemble complet des fonctionnalités. Dans la mesure où elles sont implémentées dans le logiciel, elles ne produisent pas les meilleures performances.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36676517a1979c2bd876ad3afdb84e83d596322f25015ac2cd934d48f23c5b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949979"
---
# <a name="software-shaders"></a>Nuanceurs de logiciels

Les nuanceurs de logiciels sont mis en œuvre pour permettre le développement de nuanceurs sans prise en charge du matériel sous-jacent. Ils prennent en charge l’ensemble complet des fonctionnalités. Dans la mesure où elles sont implémentées dans le logiciel, elles ne produisent pas les meilleures performances.



| Version   | Jeu de fonctionnalités                  | Configuration requise                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| vs \_ 2 \_ SW | Toutes les fonctionnalités de vs \_ 2 \_ x | Pris en charge uniquement par le traitement du vertex logiciel et par un appareil de référence. |
| vs \_ 3 \_ SW | Toutes les fonctionnalités de vs \_ 3 \_ 0 | Pris en charge uniquement par le traitement du vertex logiciel et par un appareil de référence. |
| \_logiciel PS 2 \_ | Toutes les fonctionnalités de PS \_ 2 \_ x | Pris en charge uniquement par un appareil de référence.                                |
| \_logiciel PS 3 \_ | Toutes les fonctionnalités de PS \_ 3 \_ 0 | Pris en charge uniquement par un appareil de référence.                                |



 

Certaines validations sont assouplies pour les nuanceurs de logiciels. Cela est utile à des fins de débogage et de prototypage. Les validations suivantes sont assouplies : (toutes les autres validations restent les mêmes)



| Type de validation                                 | Relax                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre d’instructions :                             | Cela est assoupli pour vs \_ 2 \_ SW, vs \_ 3 \_ SW et PS \_ 2 \_ SW, PS \_ 3 \_ SW. Des instructions illimitées sont autorisées.                                                                                                              |
| Nombres de constantes float :                          | Cela est assoupli pour vs \_ 2 \_ SW, vs \_ 3 \_ SW et PS \_ 2 \_ SW, PS \_ 3 \_ SW. Jusqu’à 8192 constantes sont autorisées.                                                                                                                |
| Nombres de constantes entières :                        | Cela est assoupli pour vs \_ 2 \_ SW, vs \_ 3 \_ SW et PS \_ 2 \_ SW, PS \_ 3 \_ SW. Jusqu’à 2048 constantes sont autorisées.                                                                                                                |
| Nombres de constantes booléennes :                        | Cela est assoupli pour vs \_ 2 \_ SW, vs \_ 3 \_ SW et PS \_ 2 \_ SW, PS \_ 3 \_ SW. Jusqu’à 2048 constantes sont autorisées.                                                                                                                |
| Profondeur de lecture dépendante :                           | Cela est assoupli pour le \_ logiciel PS 2 \_ . Comme dans vs \_ 3 \_ 0 et PS \_ 3 \_ 0, les lectures dépendantes illimitées sont autorisées.                                                                                                                |
| Nombre d’instructions et d’étiquettes de contrôle de flow : | Cela est assoupli pour vs \_ 2 \_ SW. Les instructions de contrôle de Flow illimitées et jusqu’à 2048 étiquettes sont autorisées.                                                                                                                |
| Nombre de boucles/Démarrer/Exécuter :                          | Celles-ci sont assouplies pour vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW et PS \_ 3 \_ SW. La taille de l’étape de début et d’itération des itérations pour les instructions REP et Loop sont des intergers signés 32 bits. Le nombre d’interconnexions peut atteindre un maximum de \_ int/64. |
| Limites du port de lecture :                               | vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW et PS \_ 3 \_ SW n’ont pas de limite de lecture des ports.                                                                                                                                              |
| Nombre d’interpolateurs :                        | Il y a 16 [registres, vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) dans vs \_ 3 \_ SW et 10 [PS \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) pour PS \_ 3 \_ SW.     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du nuanceur asm](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




