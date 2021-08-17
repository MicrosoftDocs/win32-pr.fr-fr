---
title: Guide de programmation pour Windows 64 bits
description: Microsoft a publié des versions 64 bits du système d’exploitation Windows.
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- guide de programmation Windows 64 bits 64-bits Windows programmation
- 64-bit Windows guide de programmation 64 bits Windows programmation, page d’hébergement
- guide de programmation pour la programmation 64 bits Windows 64 bits Windows consultez 64-bit Windows guide de programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8af8c2cb6340bd7617dd7e712f89cb5d9485c65d3d56258850c1a885df1f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743466"
---
# <a name="programming-guide-for-64-bit-windows"></a>Guide de programmation pour Windows 64 bits

Microsoft a publié des versions 64 bits du système d’exploitation Windows. 64 bits Windows a été conçu en tenant compte de la compatibilité. les développeurs peuvent s’assurer que leurs applications 32 bits existantes s’exécutent correctement sous 64 bits Windows ou tirent parti des avantages de la Windows 64 bits en migrant leurs applications.

## <a name="benefits-of-64-bit-windows"></a>Avantages de l’Windows 64 bits

Un système d’exploitation 64 bits prend en charge beaucoup plus de mémoire physique qu’un système d’exploitation 32 bits. par exemple, la plupart des systèmes de Windows 32 bits prennent en charge un maximum de 4 gigaoctets de mémoire physique, avec jusqu’à 3 gigaoctets d’espace d’adressage pour chaque processus, tandis que 64 bits Windows prend en charge jusqu’à 2 téraoctets de mémoire physique avec 8 téraoctets d’espace d’adressage pour chaque processus. L’augmentation de la mémoire physique offre les avantages suivants pour les applications :

-   Chaque application peut prendre en charge davantage d’utilisateurs. La totalité ou une partie de chaque application doit être répliquée pour chaque utilisateur, ce qui nécessite de la mémoire supplémentaire.
-   Chaque application offre de meilleures performances. L’augmentation de la mémoire physique permet à un plus grand nombre d’applications de s’exécuter simultanément et de rester entièrement résident dans la mémoire principale du système. Cela réduit ou élimine la baisse des performances de la permutation des pages vers et à partir du disque.
-   Chaque application dispose de davantage de mémoire pour le stockage et la manipulation des données. Les bases de données peuvent stocker davantage de données dans la mémoire physique du système. L’accès aux données est plus rapide, car les lectures de disque ne sont pas nécessaires.
-   Les applications peuvent manipuler de grandes quantités de données facilement et de manière plus fiable. la composition vidéo du travail image motion requiert une Windows 64 bits pour cette raison. La modélisation des applications scientifiques et financières présente des avantages considérables par rapport aux structures de données résidant en mémoire qui ne sont pas possibles sur les Windows 32 bits.

Il existe également des avantages importants pour les entreprises :

-   Accroissement de la productivité. Les travailleurs du savoir peuvent consacrer leur temps à réfléchir et à produire, au lieu d’attendre que le logiciel achève ses tâches.
-   Réduction du coût de possession. Chaque serveur pouvant prendre en charge un grand nombre d’utilisateurs et d’applications, votre entreprise aura besoin de moins de serveurs. Cela se traduit directement par une surcharge de gestion moins importante, l’un des coûts les plus élevés dans tout environnement informatique.
-   Nouvelles opportunités d’application. De nouvelles applications peuvent être conçues sans les barrières imposées par la Windows 32 bits. Les nouvelles applications graphiques rendent le travail plus facile et plus agréable. Les tâches consommatrices de données qui ne sont pas réalisables aujourd’hui peuvent être effectuées à l’aide de la Windows 64 bits.

## <a name="in-this-section"></a>Dans cette section

-   [Préparation à la Windows 64 bits](getting-ready-for-64-bit-windows.md)
-   [Conception d’interfaces compatibles 64 bits](designing-64-bit-compatible-interfaces.md)
-   [Exécution d’applications 32 bits](running-32-bit-applications.md)
-   [Conseils de migration](migration-tips.md)

 

 




