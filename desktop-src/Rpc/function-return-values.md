---
title: Valeurs de retour de fonction
description: Les valeurs de retour de fonction sont similaires aux paramètres \ out \ uniquement car leurs données ne sont pas fournies par l’application cliente.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509467"
---
# <a name="function-return-values"></a>Valeurs de retour de fonction

Les valeurs de retour de fonction sont similaires aux paramètres de **\[ sortie \]** uniquement, car leurs données ne sont pas fournies par l’application cliente. Toutefois, elles sont gérées différemment. Contrairement aux paramètres de **\[ sortie \]** seule, il n’est pas nécessaire qu’ils soient des pointeurs. La procédure distante peut retourner n’importe quel type de données valide, à l’exception des pointeurs de référence et des unions non encapsulées.

Toutefois, il est recommandé d’utiliser un paramètre **\[ out \]** au lieu d’une valeur de retour pour les types de données complexes. Lors du retour de types de données complexes, le compilateur MIDL génère un stub en mode/OS. Par conséquent, toutes les informations récentes de vérification des erreurs fournies par/Robust sont perdues.

Les valeurs de retour de fonction qui sont des types pointeur sont allouées par le stub client avec un appel à [MIDL \_ User \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). En conséquence, seul l’attribut de pointeur complet ou unique peut être appliqué à un type de retour de fonction de pointeur.

 

 