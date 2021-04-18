---
description: Lorsque le système démarre un programme qui utilise la liaison dynamique au moment du chargement, il utilise les informations que l’éditeur de liens place dans le fichier pour localiser les noms des DLL utilisées par le processus.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time la liaison dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530015"
---
# <a name="load-time-dynamic-linking"></a>Load-Time la liaison dynamique

Lorsque le système démarre un programme qui utilise la liaison dynamique au moment du chargement, il utilise les informations que l’éditeur de liens place dans le fichier pour localiser les noms des DLL utilisées par le processus. Le système recherche ensuite les dll. Pour plus d’informations, consultez ordre de recherche de la [bibliothèque de liens dynamiques](dynamic-link-library-search-order.md).

Si le système ne parvient pas à localiser une DLL requise, il met fin au processus et affiche une boîte de dialogue qui signale l’erreur à l’utilisateur. Dans le cas contraire, le système mappe la DLL dans l’espace d’adressage virtuel du processus et incrémente le nombre de références de DLL.

Le système appelle la fonction de point d’entrée. La fonction reçoit un code indiquant que le processus est en train de charger la DLL. Si la fonction de point d’entrée ne retourne pas la valeur TRUE, le système met fin au processus et signale l’erreur. Pour plus d’informations sur la fonction de point d’entrée, consultez [bibliothèque de liens dynamiques Entry-Point fonction](dynamic-link-library-entry-point-function.md).

Enfin, le système modifie la table d’adresses des fonctions avec les adresses de départ des fonctions DLL importées.

La DLL est mappée dans l’espace d’adressage virtuel du processus lors de son initialisation et est chargée dans la mémoire physique uniquement lorsque cela est nécessaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la liaison dynamique Load-Time](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



