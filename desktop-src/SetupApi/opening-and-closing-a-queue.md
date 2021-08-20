---
description: Avant de pouvoir faire des opérations de file d’attente, vous devez ouvrir une file d’attente de fichiers. L’appel de la fonction SetupOpenFileQueue retourne un handle vers un fichier de file d’attente. Ce descripteur est utilisé par les fonctions de file d’attente suivantes pour faire référence à la file d’attente ouverte et y ajouter des opérations ou l’analyser.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Ouverture et fermeture d’une file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8465446842521adbd320816a76d7f545819eebf68b55aee0c3a057fc0ca3ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965152"
---
# <a name="opening-and-closing-a-queue"></a>Ouverture et fermeture d’une file d’attente

Avant de pouvoir faire des opérations de file d’attente, vous devez ouvrir une file d’attente de fichiers. L’appel de la fonction [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) retourne un handle vers un fichier de file d’attente. Ce descripteur est utilisé par les fonctions de file d’attente suivantes pour faire référence à la file d’attente ouverte et y ajouter des opérations ou l’analyser.

Une fois que toutes les opérations de fichier spécifiées ont été mises en file d’attente et validées, vous devez appeler la fonction [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) pour libérer les ressources allouées pendant l’appel à [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).

> [!Note]  
> La fonction [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) ne valide pas la file d’attente de fichiers. Toutes les opérations qui ne sont pas validées quand **SetupCloseFileQueue** est appelé ne sont pas exécutées.

 

 

 



