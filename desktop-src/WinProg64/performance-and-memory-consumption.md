---
title: Performances et consommation de mémoire sous WOW64
description: Les performances et la consommation de mémoire sous WOW64 sont déterminées par les facteurs suivants.
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- performances sous WOW64 64 bits Windows programmation
- consommation de mémoire sous WOW64 64 bits Windows programmation
- Windows de la programmation WOW64 64 bits, performances
- programmation Windows WOW64 64 bits, consommation de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d5dd20cb42245318bf2666da788b9eea9e371c3945155c1b03b876fa513f5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613829"
---
# <a name="performance-and-memory-consumption-under-wow64"></a>Performances et consommation de mémoire sous WOW64

Les performances et la consommation de mémoire sous WOW64 sont déterminées par les facteurs suivants :

-   Matériel du processeur. L’émulation d’instruction est effectuée sur la puce. Sur le processeur x64, les instructions x86 sont exécutées en mode natif par le processeur. Par conséquent, la vitesse d’exécution sous WOW64 sur x64 est semblable à celle de la Windows 32 bits. Sur le processeur Intel Itanium et les processeurs ARM64, un plus grand nombre de logiciels est impliqué dans l’émulation et les performances en sont affectées.
-   Surcharge d’API de thunk. Cette surcharge est faible par rapport aux appels système au noyau NT. Les fonctions du noyau NT sont conçues pour être rarement appelées.
-   Taille de la mémoire virtuelle. Sur le processeur Intel Itanium, WOW64 ajoute une surcharge significative si au moins deux instances de la même application 32 bits s’exécutent simultanément. Cela est dû aux pages natives de 8 Ko sur Intel Itanium, qui compliquent l’émulation des pages de 4 Ko natives sur l’architecture x86 (d’autres pages sont marquées comme étant accessibles en écriture ; toutes les pages accessibles en écriture sont privées pour le processus). Cela peut nuire à l’évolutivité des services Terminal Server sur certains processeurs. Ce n’est pas le cas pour le processeur x64.
-   Plage de travail. WOW64 augmente la taille de la plage de travail de l’application.

WOW64 permet aux applications 32 bits de tirer parti du noyau 64 bits. Par conséquent, les applications 32 bits peuvent utiliser un plus grand nombre de handles de noyau et de handles de fenêtre. Toutefois, les applications 32 bits peuvent ne pas être en mesure de créer autant de threads sous WOW64 qu’elles le peuvent quand elles s’exécutent en mode natif sur des systèmes x86, car WOW64 alloue une pile 64 bits supplémentaire (généralement 512 Ko) pour chaque thread. En outre, une certaine quantité d’espace d’adressage est réservée pour WOW64 et les structures de données qu’elle utilise. La quantité réservée dépend du processeur. davantage est réservé sur Intel Itanium que sur les processeurs x64 ou ARM64.

Si l’indicateur de prise [**en \_ \_ charge d' \_ adresses \_ volumineux du fichier image**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) est défini dans l’en-tête de l’image, chaque application 32 bits reçoit 4 Go d’espace d’adressage virtuel dans l’environnement WOW64. Si l’indicateur de **\_ \_ \_ \_ reconnaissance d’adresse importante du fichier image** n’est pas défini, chaque application 32 bits reçoit 2 Go d’espace d’adressage virtuel dans l’environnement WOW64.

 

 