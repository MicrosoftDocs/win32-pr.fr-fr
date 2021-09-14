---
description: Préfixez toujours un fichier texte brut Unicode avec une marque d’ordre d’octet, qui informe une application recevant le fichier que le fichier est classé en octets.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Utilisation des marques d’ordre des octets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224097"
---
# <a name="using-byte-order-marks"></a>Utilisation des marques d’ordre des octets

Préfixez toujours un fichier texte brut Unicode avec une marque d’ordre d’octet, qui informe une application recevant le fichier que le fichier est classé en octets. Les marques d’ordre d’octet disponibles sont répertoriées dans le tableau suivant. Étant donné que le texte brut Unicode est une séquence de valeurs de code de 16 bits, il est sensible à l’ordre des octets utilisé lorsque le texte est écrit.

> [!Note]  
> Une marque d’ordre d’octet n’est pas un caractère de contrôle qui sélectionne l’ordre d’octet du texte.

 



| Marque d'ordre d'octet | Description           |
|-----------------|-----------------------|
| EF BB BF        | UTF-8                 |
| FF FE           | UTF-16, Little endian |
| FE FF           | UTF-16, Big endian    |
| FF FE 00 00     | UTF-32, Little endian |
| 00 00 FE FF     | UTF-32, Big-endian    |



 

> [!Note]  
> Microsoft utilise UTF-16, primauté des octets de poids faible.

 

Dans l’idéal, tout le texte Unicode suit un seul jeu de règles de classement des octets. Toutefois, cela n’est pas possible car les microprocesseurs diffèrent au niveau de l’emplacement de l’octet le moins significatif. Les processeurs Intel et MIPS déplacent d’abord l’octet le moins significatif, tandis que les processeurs Motorola (et tous les fichiers Unicode inversé en octets) le déplacent en dernier. Avec un seul ensemble de règles de classement des octets, les utilisateurs d’un type de microprocesseur sont obligés de permuter l’ordre des octets chaque fois qu’un fichier texte brut est lu ou écrit, même si le fichier n’est jamais transféré vers un autre système d’exploitation basé sur un microprocesseur différent.

L’emplacement par défaut pour spécifier l’ordre des octets est dans un en-tête de fichier, mais les fichiers texte n’ont pas d’en-tête. Par conséquent, Unicode a défini un caractère (U + FEFF) et un caractère non-caractère (U + FFFE) comme marques d’ordre d’octet. Il s’agit d’images en miroir les unes des autres.

Étant donné que la séquence U + FEFF est extrêmement rare au début d’un fichier texte non-Unicode normal, elle peut servir de marqueur ou de signature implicite pour identifier le fichier en tant que fichier Unicode. Les applications qui lisent à la fois les fichiers texte Unicode et non-Unicode doivent utiliser la présence de cette séquence comme un indicateur qui indique que le fichier est probablement un fichier Unicode. Comparez cette technique à l’utilisation du marqueur EOF MS-DOS pour mettre fin aux fichiers texte.

Quand une application trouve U + FEFF au début d’un fichier texte, elle traite généralement le fichier en tant que fichier Unicode, bien qu’elle puisse effectuer d’autres vérifications heuristiques pour la vérification. Une telle vérification peut être aussi simple que le test pour déterminer si la variation des octets de poids faible est beaucoup plus élevée que la variation dans les octets de poids fort. Par exemple, si le texte ASCII est converti en texte Unicode, chaque seconde octet est égal à 0. En outre, la vérification des caractères de saut de ligne et de retour chariot (U + 000A et U + 000D) et de la taille du fichier pair ou impair peut fournir un indicateur fort de la nature du fichier.

Quand une application trouve U + FFFE au début d’un fichier texte, elle l’interprète pour signifier que le fichier est un fichier Unicode inversé par octet. L’application peut échanger l’ordre des octets ou alerter l’utilisateur qu’une erreur s’est produite.

Étant donné que le caractère de marque d’ordre d’octet Unicode est introuvable dans une page de codes, il disparaît si les données sont converties en ANSI. Contrairement à d’autres caractères Unicode, il n’est pas remplacé par un caractère par défaut lorsqu’il est converti. Si une marque d’ordre d’octet se trouve au milieu d’un fichier, elle n’est pas interprétée comme un caractère Unicode et n’a aucun effet sur la sortie de texte.

> [!Note]  
> La valeur Unicode U + FFFF est illégale dans les fichiers texte bruts et ne peut pas être transmise entre les applications. Elle est réservée à l’utilisation privée d’une application.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de caractères spéciaux en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



