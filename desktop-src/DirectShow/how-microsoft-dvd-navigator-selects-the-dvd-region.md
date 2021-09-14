---
description: Comment le navigateur de DVD Microsoft sélectionne la région du DVD
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Comment le navigateur de DVD Microsoft sélectionne la région du DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119862"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a>Comment le navigateur de DVD Microsoft sélectionne la région du DVD

Le navigateur DVD Microsoft utilise l’algorithme suivant pour déterminer la correspondance de la région tout en lisant des disques DVD sur un PC :

1.  Le navigateur DVD obtient la région du disque, la région du lecteur et la région du décodeur.
2.  Si la région du disque est « toutes les régions », le navigateur DVD lit le disque.
3.  Si le disque n’est pas marqué pour toutes les régions, le navigateur DVD vérifie si le décodeur a une région prédéfinie.
4.  Si le décodeur a une région prédéfinie et qu’il ne correspond pas à la région du disque, le navigateur DVD renvoie une erreur indiquant qu’il ne peut pas lire le disque sur la configuration actuelle du DVD. Terminer
5.  Si la région du décodeur n’est pas définie ou est identique à la région du disque, le navigateur DVD vérifie si la région du lecteur est la même que la région du disque.
6.  Si la région du lecteur correspond à la région du disque, le navigateur DVD lit le titre.
7.  Dans le cas contraire, si la région du pilote ne correspond pas à la région du disque, le navigateur DVD appelle le code pour modifier la région du lecteur. Si le nombre autorisé de modifications de région est épuisé, la tentative de modification de la région échoue et le titre ne peut pas être lu sur ce système.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge du changement de région des DVD dans Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



