---
title: Compatibilité des clients et des serveurs-Windows 8
description: Windows 8 et Windows Server 2012 la compatibilité du client et du serveur
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bbe52486339906d260fe623533cfbb871e97c07f914798990a5d16c51e5bbf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593809"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a>Windows 8 et Windows Server 2012 la compatibilité du client et du serveur

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
-   le stockage étendu est désormais facultatif pour environnement de préinstallation Windows (WinPE) (WinPE) et référence de serveur
-   le Service de disque virtuel est en train de passer à l’API de gestion des Stockage Windows basée sur Windows Management Instrumentation (WMI)
-   Interface utilisateur des versions précédentes supprimées pour les volumes locaux
-   StorAHCI remplace MSAHCI
-   sauvegarde et restauration de Windows 7 déconseillées
-   Transferts de données déchargées

**Autres**

-   Gestionnaire de fenêtrage est toujours activé
-   Direct2D ne prend pas en charge le rendu des sous-fichiers « enrichis » dans Internet Explorer 9
-   Modifications apportées à la prise en charge matérielle héritée virtuel DX9
-   MSAA n’est pas disponible pour les applications de Windows store
-   Le port 3 est déconseillé pour les pilotes NDIS 6,30

 

 
