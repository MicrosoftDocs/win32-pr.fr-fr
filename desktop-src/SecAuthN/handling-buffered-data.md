---
description: Plusieurs fonctions du fournisseur de réseau prennent l’adresse et la taille d’une mémoire tampon dans laquelle la fonction place une structure de données de taille variable.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Gestion des données mises en mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01cac833b0c7b76bf09a6735d719a001c8393383f1dd031ff741900a1c9dcf2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623099"
---
# <a name="handling-buffered-data"></a>Gestion des données mises en mémoire tampon

Plusieurs fonctions du fournisseur de réseau prennent l’adresse et la taille d’une mémoire tampon dans laquelle la fonction place une structure de données de taille variable.

Dans chaque cas, le mécanisme utilisé est le même. L’appelant alloue une mémoire tampon et passe son adresse à la fonction. Il passe également l’adresse d’une **valeur DWORD** qui spécifie la taille de la mémoire tampon, en octets.

La fonction copie ensuite la plus grande partie de la structure de données demandée, telle qu’elle peut être dans la mémoire tampon. Si toutes les données tiennent dans la mémoire tampon, la fonction retourne la valeur WN \_ Success. Si les données ne tiennent pas dans la mémoire tampon, les données peuvent ne pas être incomplètes et la fonction définit l' \_ erreur WN More \_ Data. Dans les deux cas, la valeur **DWORD** indiquant la taille de la mémoire tampon est définie sur le nombre d’octets réellement requis par la structure de données. De cette façon, si la mémoire tampon transmise est trop petite et que la fonction a échoué, l’appelant peut allouer une nouvelle mémoire tampon de la taille requise et appeler à nouveau la fonction.

Lorsque les structures de données retournées incluent des chaînes de longueur variable, les structures de données individuelles contiennent généralement des pointeurs vers ces chaînes. Les chaînes elles-mêmes doivent également être placées dans la mémoire tampon. Toutefois, il est important de les placer à la fin de la mémoire tampon. Dans le cas contraire, elles feront de l’indexation sur la nième structure impossible. En d’autres termes, toutes les structures se trouvent contiguës au début de la mémoire tampon. Les pointeurs vers des chaînes ou des données de longueur variable doivent être des pointeurs réels, et non des décalages dans la mémoire tampon.

Lorsqu’une mémoire tampon est utilisée pour transmettre et retourner des données qui se composent uniquement de chaînes, la valeur **DWORD** spécifiant la taille de la mémoire tampon doit être définie sur le nombre total de caractères pouvant tenir dans ces chaînes, et non sur le nombre d’octets.

 

 



