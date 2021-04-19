---
description: 'Toute opération de sauvegarde qui tente de copier une image complète et stable d’un système doit répondre aux préoccupations suivantes :'
ms.assetid: 8ccdba6d-1097-4c1c-982c-f3d9cbdf06cd
title: Problèmes de sauvegarde de volume courants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f10433e0a695c11f7e61a258c3256baa651dc27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532294"
---
# <a name="common-volume-backup-issues"></a>Problèmes de sauvegarde de volume courants

Toute opération de sauvegarde qui tente de copier une image complète et stable d’un système doit répondre aux préoccupations suivantes :

-   Fichiers inaccessibles pendant une sauvegarde. Les applications en cours d’exécution doivent souvent conserver les fichiers ouverts en mode exclusif pendant une sauvegarde, ce qui empêche les programmes de sauvegarde de les copier.
-   État incohérent des fichiers. Même si les fichiers d’une application ne sont pas ouverts en mode exclusif, cela est possible, en raison du temps limité nécessaire à l’ouverture, à la sauvegarde et à la fermeture d’un fichier, que les fichiers copiés sur le support de stockage ne reflètent pas tous le même état de l’application.
-   Nécessité de réduire les interruptions de service. Pour garantir l’accessibilité des fichiers et l’intégrité des données sauvegardées, vous pouvez exiger la suspension et/ou l’arrêt de tous les programmes en cours d’exécution pendant une sauvegarde de volume. Pour les systèmes de disques volumineux, il peut s’agir d’heures de durée.

    Récemment, certains fournisseurs de stockage ont tenté de résoudre ces problèmes en fournissant un mécanisme de capture de volume, qui permet de capturer une image des fichiers sur le disque à un instant donné, à l’aide d’un mécanisme de copie sur écriture ou de « miroir scindé ». Toutefois, ces solutions impliquent des difficultés :

    -   Implémentations de fournisseur d’une capture de volume incompatible. De nombreux fournisseurs d’appareils RAID offrent des mécanismes de capture de volume. Toutefois, chaque fournisseur possède sa propre interface et doit obtenir un support des fournisseurs de sauvegarde pour ses interfaces de capture de volume. Cela signifie que les fournisseurs d’applications de sauvegarde doivent prendre en charge plusieurs implémentations de capture de volume, ce qui n’est pas souhaitable.
    -   Manque de coordination des applications. De nombreux appareils qui prennent en charge une capture de volume ne prennent pas en charge la coordination des applications en cours d’exécution avec le gel des données sur le disque. Pour les périphériques qui, comme avec les applications de sauvegarde, chaque fournisseur a une interface différente.
    -   Prise en charge limitée des appareils non RAID. Quelques-uns des fournisseurs de disques conventionnels prennent en charge toute sorte de capture de volume dans leurs pilotes de périphérique. Cela signifie que les mécanismes de capture sont limités à certains systèmes de disque et ne peuvent généralement pas prendre en charge la sauvegarde des zones système.
    -   Vous devez gérer les mises à jour sur le disque lors de la capture du volume. Bien que les mécanismes de capture de volume fournis par le fournisseur de stockage puissent geler l’état des données sur le disque, ils n’interagissent pas toujours avec les applications en cours d’exécution. Cela signifie souvent que les données envoyées au volume pendant qu’un dispositif de stockage subit une capture de volume peuvent être perdues.
    -   Sauvegarde multivolume cohérente. Le dispositif de stockage exécute ces captures de volume, de sorte qu’il n’y a généralement pas de mécanisme permettant de coordonner la synchronisation des données. Cela est particulièrement vrai si les appareils proviennent de fournisseurs distincts. Par conséquent, si plusieurs volumes de stockage sont impliqués dans une sauvegarde avec une capture de volume, l’image de temps conservée pour chaque volume peut ne pas être cohérente.

 

 



