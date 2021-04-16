---
description: Les développeurs de bases de données d’installation doivent être conscients de deux limitations sur la gestion des flux par l’implémentation de stockage structuré OLE Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitations OLE sur les flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201790"
---
# <a name="ole-limitations-on-streams"></a>Limitations OLE sur les flux

Les développeurs de bases de données d’installation doivent être conscients de deux limitations sur la gestion des flux par l’implémentation de stockage structuré OLE Win32. Ces limitations peuvent affecter les fonctions du programme d’installation indirectement par le biais de transformations et d’autres données qui peuvent être stockées dans la base de données sous forme de flux.

Deux limitations s’appliquent :

-   Les données binaires sont stockées avec un nom d’index créé en concaténant le nom de la table et les valeurs des clés primaires de l’enregistrement à l’aide d’un délimiteur de point. OLE limite les noms de flux à 32 caractères (31 + terminateur null). Windows Installer utilise un algorithme de compression qui peut étendre la limite à 62 caractères en fonction du caractère. Notez que les caractères codés sur deux octets comptent comme 2.
-   Même si plusieurs flux peuvent être ouverts en même temps, vous ne pouvez pas ouvrir un flux une deuxième fois jusqu’à la fermeture de la première référence. Cela signifie que vous ne pouvez pas sélectionner le même flux de données binaires à ouvrir simultanément dans plusieurs enregistrements. Les tentatives de lecture des données binaires à partir du deuxième enregistrement échouent. Vous ne pouvez pas non plus renommer les clés primaires d’un enregistrement lorsqu’un flux de données binaires de cet enregistrement est ouvert.

 

 



