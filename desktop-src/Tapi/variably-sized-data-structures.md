---
description: Lorsque les structures de données de taille variable sont utilisées pour transmettre des informations entre l’interface TAPI et l’application, l’application est chargée d’allouer la mémoire nécessaire.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Structures de données de taille variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182e349079abbce93f533b1b6cd299ab7e0e883d71e9b845dfdaf52bf0275ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760194"
---
# <a name="variably-sized-data-structures"></a>Structures de données de taille variable

Lorsque les structures de données de taille variable sont utilisées pour transmettre des informations entre l’interface TAPI et l’application, l’application est chargée d’allouer la mémoire nécessaire. La quantité de mémoire allouée doit être au moins suffisamment grande pour la partie fixe de la structure de données, et est définie par l’application dans le membre **dwTotalSize** de la structure de données. Les membres **dwUsedSize** et **dwNeededSize** sont renseignés par TAPI. Si **dwTotalSize** est inférieur à la taille de la partie fixe, LINEERR/PHONEERR \_ STRUCTURETOOSMALL est retourné. Si une fonction retourne Success, tous les champs de la partie fixe ont été remplis. Les membres **dwUsedSize** et **dwNeededSize** peuvent être comparés pour déterminer si toutes les parties variables ont été remplies, ainsi que la quantité d’espace nécessaire pour les remplir.

Si **dwNeededSize** est égal à **dwUsedSize**, toutes les parties fixes et variables ont été remplies. Si **dwNeededSize** est supérieur à **dwUsedSize**, certaines parties variables peuvent avoir été remplies, mais les champs de taille variable exactement qui ont été remplis ne sont pas définis. Aucune partie variable n’est jamais tronquée et les parties variables qui auraient été tronquées en raison d’un espace insuffisant sont indiquées en faisant en sorte que les deux parties « décalage » et « taille » correspondantes soient définies sur zéro. S’il ne s’agit pas de zéro (et qu’aucune erreur n’a été retournée), elles indiquent le décalage et la taille des données de partie variable valides et non tronquées.

Une application peut toujours garantir que toutes les parties variables sont remplies en allouant et en indiquant les octets **dwNeededSize** pour la structure et en appelant à nouveau la fonction « obtenir » jusqu’à ce que la fonction retourne Success et **DwNeededSize** égal à **dwUsedSize**. Cela doit se produire à la deuxième tentative, à l’exception des conditions de concurrence qui entraînent des modifications de la taille des parties variables entre les appels, ce qui doit être une occurrence rare.

> [!Note]  
> Toutes les chaînes de texte, quel que soit l’encodage, dans les structures à taille variable doivent se terminer par un caractère **null** conformément aux conventions normales de gestion des chaînes C.

 

 

 



