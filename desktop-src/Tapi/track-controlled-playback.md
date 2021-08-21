---
description: Les étapes suivantes sont effectuées pour la lecture contrôlée par suivi.
ms.assetid: 9069fb32-3978-491b-bb22-f6e736af23d7
title: Lecture Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc26cd1448c712b99a0e61bf94520531c1c592a289d273257c8bc907b266eea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002617"
---
# <a name="track-controlled-playback"></a>Lecture Track-Controlled

Pour effectuer une lecture contrôlée par suivi, procédez comme suit :

-   Sélectionnez le suivi des terminaux sur les flux.
-   Créez le terminal de lecture de fichier.
-   Définir les propriétés : le nom et le type de stockage du fichier.
-   À l’aide d’une méthode sur le terminal de lecture de fichier, énumérez les terminaux de suivi de fichier.
-   Énumérer les flux sur l’appel TAPI.
-   Sélectionnez le terminal file Track dans le flux.
-   Appelez la méthode [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sur le terminal de lecture de fichier pour démarrer la lecture des données enregistrées dans les flux TAPI.

 

 



