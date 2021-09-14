---
description: Cette section décrit comment planifier, développer et tester les pages de référence des événements (vos solutions ERP) et comment les déployer dans un expert ou une analyse. Pour plus d’informations sur les vos solutions ERP et leur utilisation avec Moniteur réseau, consultez la page de référence des événements.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Création d’un expert et surveillance des pages de référence des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229715"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a>Création d’un expert et surveillance des pages de référence des événements

Cette section décrit comment planifier, développer et tester les pages de référence des événements (vos solutions ERP) et comment les déployer dans un expert ou une analyse. Pour plus d’informations sur les vos solutions ERP et leur utilisation avec Moniteur réseau, consultez la [page de référence des événements](event-reference-page.md).

Pour développer un nouvel ERP, la première étape consiste à déterminer les événements qui requièrent des vos solutions ERP individuels pour votre [expert](experts.md) ou votre [moniteur](monitors.md)personnalisé. Vous devez créer des vos solutions ERP distincts pour chaque événement que vous souhaitez afficher dans le observateur d’événements Moniteur réseau. Par exemple, supposons que :

-   Vous développez un moniteur nommé Game Monitor et stock Watcher.
-   Le moniteur se trouve dans un fichier appelé Gamemon.dll.
-   Le moniteur génère deux événements : le jeu est en cours d’exécution et mes raccourcis d’inventaire Internet.
-   Vous envisagez de développer deux vos solutions ERP, Gamemon1.htm et Gamemon2.htm.

> [!Note]  
> Il n’est pas nécessaire d’avoir une correspondance un-à-un entre les vos solutions ERP et les événements d’experts.

 

Une fois que vous avez établi une liste de vos solutions ERP uniques, procédez comme suit pour créer chaque ERP.

-   [Écrivez le document source HTML](writing-an-event-reference-page.md).
-   [Enregistrez et nommez](naming-an-event-reference-page.md) le fichier source HTML sous la forme d’un fichier de .htm.
-   [Testez l’ERP](testing-an-event-reference-page.md) avec l’expert ou l’analyse terminé.

 

 



