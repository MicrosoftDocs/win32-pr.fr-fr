---
description: Windows GDI+ est le sous-système du système d’exploitation Windows XP ou Windows Server 2003 qui est responsable de l’affichage des informations sur les écrans et les imprimantes. GDI+ est une API exposée par le biais d’un ensemble de classes C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Vue d’ensemble de GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ca4eadf9eaf27cbe35103753a49c4bc25d2974ee1051481b0b52787a6602e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830759"
---
# <a name="overview-of-gdi"></a>Vue d’ensemble de GDI+

Windows GDI+ est le sous-système du système d’exploitation Windows XP ou Windows Server 2003 qui est responsable de l’affichage des informations sur les écrans et les imprimantes. GDI+ est une API exposée par le biais d’un ensemble de classes C++.

comme son nom l’indique, GDI+ est le successeur de Windows Graphics Device Interface (GDI), l’Interface de périphérique graphique incluse avec les versions antérieures de Windows. Windows XP ou Windows Server 2003 prend en charge GDI pour la compatibilité avec les applications existantes, mais les programmeurs de nouvelles applications doivent utiliser GDI+ pour tous leurs besoins graphiques, car GDI+ optimise la plupart des fonctionnalités de GDI et fournit également des fonctionnalités supplémentaires.

une interface de périphérique graphique, telle que GDI+, permet aux programmeurs d’applications d’afficher des informations sur un écran ou une imprimante sans se préoccuper des détails d’un périphérique d’affichage particulier. le programmeur d’applications effectue des appels aux méthodes fournies par les classes GDI+ et ces méthodes effectuent à leur tour les appels appropriés à des pilotes de périphérique spécifiques. GDI+ isole l’application du matériel graphique et c’est cette isolation qui permet aux développeurs de créer des applications indépendantes du périphérique.

 

 



