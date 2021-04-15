---
title: Initialisation de la bande
description: Une application doit utiliser la fonction CreateFile pour créer un handle de périphérique à bandes. Ce descripteur est utilisé dans les opérations suivantes sur la bande de l’appareil.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Sauvegarde d’initialisation de bande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463426"
---
# <a name="tape-initialization"></a>Initialisation de la bande

Une application doit utiliser la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour créer un handle de périphérique à bandes. Ce descripteur est utilisé dans les opérations suivantes sur la bande de l’appareil.

Avant qu’une application n’écrive sur une bande, la bande doit être mise en forme en fonction des besoins de l’application et des fonctionnalités du lecteur de bande utilisé. La fonction [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) reformate une bande, en créant un nombre donné de partitions d’une taille spécifiée.

La fonction [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prépare l’accès ou la suppression d’une bande. Cette fonction peut charger, décharger, verrouiller ou déverrouiller une bande. Cette fonction peut également mettre en marche la bande en la déplaçant à la fin de la bande et en la faisant revenir au début.

Pour récupérer et définir des informations sur une bande et un lecteur de bande, une application utilise les fonctions [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)et [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .

[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) récupère des informations qui décrivent une bande ou un lecteur de bande. Les informations sur la bande incluent le type, la densité et la taille de bloc de la bande ; le nombre de partitions sur la bande ; la quantité de bande restant ; et ainsi de suite. Les informations sur le lecteur de bande incluent la taille de bloc par défaut du lecteur, le nombre maximal de partitions et les fonctionnalités prises en charge.

[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) définit la taille de bloc de bande ou définit les indicateurs de lecteur de bande qui indiquent si le lecteur prend en charge la correction des erreurs matérielles, la compression des données, le remplissage des données ou une combinaison des trois.

[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indique si le lecteur de bande est prêt à traiter les commandes de bande.

 

 