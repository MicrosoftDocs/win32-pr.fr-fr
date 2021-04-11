---
description: La mémoire qui appartient à un processus est implicitement protégée par son espace d’adressage virtuel privé.
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: Protection de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30df8084c91a62c28414f4a8142397ee777e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115919"
---
# <a name="memory-protection"></a>Protection de la mémoire

La mémoire qui appartient à un processus est implicitement protégée par son espace d’adressage virtuel privé. En outre, Windows fournit une protection de la mémoire à l’aide du matériel de mémoire virtuelle. L’implémentation de cette protection varie en fonction du processeur, par exemple, les pages de codes de l’espace d’adressage d’un processus peuvent être marquées en lecture seule et protégées contre les modifications des threads en mode utilisateur.

Pour obtenir la liste complète des attributs, consultez [constantes de protection](memory-protection-constants.md)de la mémoire.

## <a name="copy-on-write-protection"></a>Protection par copie sur écriture

La protection par copie sur écriture est une optimisation qui permet à plusieurs processus de mapper leurs espaces d’adresses virtuelles de façon à ce qu’ils partagent une page physique jusqu’à ce que l’un des processus modifie la page. Cela fait partie d’une technique appelée *évaluation différée*, qui permet au système d’économiser la mémoire physique et le temps en n’effectuant pas d’opération tant qu’il n’est pas absolument nécessaire.

Par exemple, supposons que deux processus chargent des pages à partir de la même DLL dans leurs espaces de mémoire virtuelle. Ces pages de mémoire virtuelle sont mappées aux mêmes pages de mémoire physique pour les deux processus. Tant qu’aucun processus n’écrit dans ces pages, ils peuvent mapper et partager les mêmes pages physiques, comme indiqué dans le diagramme suivant.

![zones et flèches des pages du processus 1 et 2 mappées à la même mémoire physique](images/mem1.png)

Si le processus 1 écrit dans l’une de ces pages, le contenu de la page physique est copié vers une autre page physique et le mappage de mémoire virtuelle est mis à jour pour le processus 1. Les deux processus disposent désormais de leur propre instance de la page dans la mémoire physique. Par conséquent, il n’est pas possible qu’un processus écrive sur une page physique partagée et que l’autre processus affiche les modifications.

![zones et flèches de processus et de remappage de la mémoire physique](images/mem2.png)

## <a name="loading-applications-and-dlls"></a>Chargement d’applications et de dll

Lorsque plusieurs instances de la même application Windows sont chargées, chaque instance est exécutée dans son propre espace d’adressage virtuel protégé. Toutefois, leurs handles d’instance (*HINSTANCE*) ont généralement la même valeur. Cette valeur représente l’adresse de base de l’application dans son espace d’adressage virtuel. Si chaque instance peut être chargée dans son adresse de base par défaut, elle peut mapper et partager les mêmes pages physiques avec les autres instances, à l’aide de la protection de copie sur écriture. Le système permet à ces instances de partager les mêmes pages physiques jusqu’à ce que l’une d’elles modifie une page. Si, pour une raison quelconque, une de ces instances ne peut pas être chargée dans l’adresse de base souhaitée, elle reçoit ses propres pages physiques.

Les dll sont créées avec une adresse de base par défaut. Chaque processus qui utilise une DLL essaiera de charger la DLL dans son propre espace d’adressage à l’adresse virtuelle par défaut de la DLL. Si plusieurs applications peuvent charger une DLL à son adresse virtuelle par défaut, elles peuvent partager les mêmes pages physiques pour la DLL. Si, pour une raison quelconque, un processus ne peut pas charger la DLL à l’adresse par défaut, il charge la DLL ailleurs. La protection de copie sur écriture force certaines des pages de la DLL à être copiées dans différentes pages physiques pour ce processus, car les correctifs pour les instructions de saut sont écrits dans les pages de la DLL et sont différents pour ce processus. Si la section de code contient de nombreuses références à la section de données, cela peut entraîner la copie de la section de code entière sur les nouvelles pages physiques.

 

 



