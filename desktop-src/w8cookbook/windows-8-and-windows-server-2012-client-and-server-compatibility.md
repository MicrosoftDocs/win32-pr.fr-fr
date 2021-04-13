---
title: Compatibilité du client et du serveur-Windows 8
description: Compatibilité entre le client et le serveur Windows 8 et Windows Server 2012
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104313969"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a>Compatibilité entre le client et le serveur Windows 8 et Windows Server 2012

Cette section décrit les modifications apportées au système d’exploitation dont vous devez prêter une attention particulière en raison des impacts potentiels sur les applications existantes et de la façon dont les nouvelles applications doivent être conçues sur les clients, sur les serveurs, ou sur les clients et les serveurs. Voici la liste des rubriques traitées dans cette section, regroupées par domaine de fonctionnalité :

**AppCompat**

-   Mise à jour des règles de détection des applications de sécurité
-   Détermination de l’état des shims
-   Les applications serveur doivent pouvoir s’exécuter sans l’interpréteur de commandes graphique de serveur
-   Les composants serveur RDS sont supprimés de Windows 8
-   Type de fichier et modèle d’association de protocole
-   Modérateur de l’activité du Bureau
-   .NET Framework 4,5 est la valeur par défaut et .NET Framework 3,5 est facultatif
-   Les applications de bureau peuvent ne pas être visibles après le lancement du navigateur Web par défaut
-   Mode de contraste élevé
-   Manifeste de l’application (exécutable)
-   Le modèle actuel mis en file d’attente est déconseillé
-   Scénarios de l’Assistant Compatibilité des programmes pour Windows 8
-   Gadgets du Bureau supprimés

**Stockage et système de fichiers**

-   Mise à jour de compatibilité des disques au format avancé (4K)
-   Allocation dynamique d’unités logiques
-   Le stockage étendu est désormais facultatif pour environnement de préinstallation Windows (WinPE) (WinPE) et référence de serveur
-   Le service de disque virtuel passe à l’API de gestion du stockage Windows basé sur le Windows Management Instrumentation (WMI)
-   Interface utilisateur des versions précédentes supprimées pour les volumes locaux
-   StorAHCI remplace MSAHCI
-   Sauvegarde et restauration de Windows 7 déconseillées
-   Transferts de données déchargées

**Autres**

-   Gestionnaire de fenêtrage est toujours activé
-   Direct2D ne prend pas en charge le rendu des sous-fichiers « enrichis » dans Internet Explorer 9
-   Modifications apportées à la prise en charge matérielle héritée virtuel DX9
-   MSAA n’est pas disponible pour les applications du Windows Store
-   Le port 3 est déconseillé pour les pilotes NDIS 6,30

 

 
