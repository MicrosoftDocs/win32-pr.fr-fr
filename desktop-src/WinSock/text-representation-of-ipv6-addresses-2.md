---
description: Cette section est copiée à partir de &\# 0034 ; architecture d’adressage IPv6&\# 0034 ; par R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Représentation textuelle des adresses IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d71ad1f98652a0f00e4f14f957bcedc27316444ceabc3e5c35ee2bcf81b5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733349"
---
# <a name="text-representation-of-ipv6-addresses"></a>Représentation textuelle des adresses IPv6

Cette section est copiée à partir de « architecture d’adressage IPv6 » par R. Hinden et S. Deering. Il existe trois formes conventionnelles pour représenter les adresses IPv6 en tant que chaînes de texte :

-   La forme préférée est x :x: x :x: x :x: x :x, où les « x » sont les valeurs hexadécimales des parties 8 16 bits de l’adresse.

    Exemples :

    <dl> FEDC : BA98:7654:3210 : FEDC : BA98:7654:3210  
    1080:0 : 0:0 : 8:800:200C : 417A  
    </dl>

> [!Note]  
> Il n’est pas nécessaire d’écrire les zéros non significatifs dans un champ individuel, mais il doit y avoir au moins un chiffre dans chaque champ (sauf dans le cas décrit dans le deuxième formulaire).

 

-   En raison de la méthode d’allocation de certains styles d’adresses IPv6, il est courant que les adresses contiennent des chaînes longues de zéro bits. Pour faciliter l’écriture d’adresses contenant zéro bits, une syntaxe spéciale est disponible pour compresser les zéros. L’utilisation de deux-points («  :: ») indique plusieurs groupes de zéros de 16 bits.

    Par exemple, l’adresse de multidiffusion

    <dl> FF01:0 : 0:0 : 0:0 : 0:0 : 43  
    </dl>

    peut être représenté comme suit :

    <dl> FF01 :: 43  
    </dl>

    Les guillemets doubles (" ::") ne peuvent apparaître qu’une seule fois dans une adresse. Elles peuvent être utilisées pour compresser des zéros de début ou de fin dans une adresse.

-   Une autre forme qui peut être plus pratique pour gérer un environnement mixte de nœuds IPv4 et IPv6 est x :x: x :x: x :x: d. d. d. d, où les valeurs « x » sont les valeurs hexadécimales des six parties de l’adresse (16 bits) de poids fort, et les valeurs décimales des quatre éléments 8 bits de poids faible de l’adresse (représentation IPv4 standard).

    Exemples :

    <dl> 0:0 : 0:0 : 0:0 : 0:13.1.68.3  
    0:0 : 0:0 : 0 : FFFF : 129.144.52.38  
    </dl>

    ou sous forme compressée :

    <dl> ::13.1.68.3  
    :: FFFF : 129.144.52.38  
    </dl>

 

 



