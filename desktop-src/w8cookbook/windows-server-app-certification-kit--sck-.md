---
title: Outil de test de compatibilité avec la plateforme Microsoft (MPR, Microsoft Platform Ready)
description: Outil de test de compatibilité avec la plateforme Microsoft (MPR, Microsoft Platform Ready)
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730725"
---
# <a name="microsoft-platform-ready-test-tool"></a>Outil de test de compatibilité avec la plateforme Microsoft (MPR, Microsoft Platform Ready)

## <a name="platform"></a>Plateforme

 **Serveurs** – windows server 2012 \| Windows Server 2012 R2  

## <a name="description"></a>Description

L’outil de test MPR (Microsoft Platform Ready) est utilisé pour la préparation des applications de plateforme et pour valider la conformité avec les exigences de certification pour les applications Windows Server 2012 et Windows Server 2012 R2.

Microsoft encourage vivement à incorporer l’outil de test MPR dans les processus de génération et de test de logiciels, garantissant ainsi la préparation des plateformes avant la publication des applications sur le marché. L’outil de test MPR est également un outil recommandé pour tester la compatibilité des applications métier et pour évaluer les produits serveur pour la compatibilité de leurs plateformes avant de prendre des décisions d’achat.

## <a name="requirements"></a>Configuration requise

L’outil de test MPR comprend des tests automatisés pour :

-   Windows Installer
-   Configuration et fonctionnalités principales
-   Pilotes et sécurité
-   Bonnes pratiques

L’auto-test et la soumission des résultats pour la plupart des applications serveur doivent durer 2 heures au maximum ; les applications plus complexes peuvent durer environ 4 heures.

Tous les pilotes doivent passer séparément le test de certification matérielle Windows et être signés par Microsoft pour Windows Server 2012.

## <a name="usage"></a>Utilisation

Pour tester vos applications :

1.  Installez la dernière configuration minimale de Windows Server 2012 (interface utilisateur graphique complète, interface serveur minimale ou Server Core), selon les besoins de votre application.
2.  Passez en revue les conditions de certification.
3.  Sur un système propre, exécutez l’outil de test MPR en mode d’interface utilisateur complet ou en mode de ligne de commande.
4.  Terminez le processus de test auto-guidé.
5.  Passez en revue les résultats et corrigez votre application selon vos besoins.
6.  Connectez-vous et téléchargez les résultats réussis sur le portail Microsoft pour les plateformes prêtes à être répertoriés dans le catalogue Windows Server et l’utilisation du logo.

## <a name="resources"></a>Ressources

-   [Configuration requise pour le programme de certification des applications Windows Server](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Outil de test de compatibilité avec la plateforme Microsoft (MPR, Microsoft Platform Ready)](https://www.microsoft.com/download/details.aspx?id=37143)
-   [Programme de certification des applications Windows Server 2012](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [Commentaires sur le logo Windows Server](mailto:WSLogoFB@microsoft.com)

 

 