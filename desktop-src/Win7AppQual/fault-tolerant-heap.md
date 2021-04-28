---
description: Segment de mémoire à tolérance de panne
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Segment de mémoire à tolérance de panne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17ab2630e6dc28cb84604e48be1aa60bf208a97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088397"
---
# <a name="fault-tolerant-heap"></a>Segment de mémoire à tolérance de panne

## <a name="affected-platforms"></a>Plateformes affectées

**Clients-** Windows 7  

## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité-** Médias  
**Fréquence-** Entrée  


## <a name="description"></a>Description

Le segment de mémoire à tolérance de panne (FTH) est un sous-système de Windows 7 responsable de la surveillance des pannes d’application et de l’application de mesures d’atténuation de manière autonome afin d’éviter les pannes futures pour chaque application. Pour la grande majorité des utilisateurs, FTH ne nécessite aucune intervention ni modification de leur part. Toutefois, dans certains cas, les développeurs d’applications et les testeurs de logiciels peuvent avoir besoin de remplacer le comportement par défaut de ce système.

## <a name="solution"></a>Solution

**Affichage de l’activité du tas à tolérance de panne**

Le segment de mémoire à tolérance de panne enregistre les informations lorsque le service démarre, s’arrête ou commence à atténuer les problèmes pour une nouvelle application. Pour voir ces informations, effectuez les étapes suivantes :

1.  Cliquez sur le menu Démarrer.
2.  Cliquez avec le bouton droit sur **ordinateur** , puis cliquez sur **gérer**.
3.  Cliquez sur **Observateur d’événements**  >  **les journaux des applications et des services**  >  **Microsoft**  >  **Windows > avec tolérance de pannes**
4.  Affichez les événements FTH.

Les événements d’arrêt et de démarrage du service ne contiennent pas de données supplémentaires. L’événement FTH activé contient l’ID de processus (PID), le nom de l’image de processus et l’heure de début de l’instance de processus.

**Désactivation du tas à tolérance de panne**

**Attention** Des problèmes sérieux peuvent survenir si vous modifiez le registre de manière incorrecte à l’aide de l’éditeur du registre ou en utilisant une autre méthode. Ces problèmes peuvent nécessiter la réinstallation du système d’exploitation. Microsoft ne peut pas garantir que ces problèmes puissent être résolus. Toute modification du registre relève de votre propre responsabilité.  
 Pour désactiver entièrement le segment de mémoire à tolérance de panne sur un système, définissez la \_ valeur reg DWORD **HKLM \\ Software \\ Microsoft \\ FTH \\ Enabled** sur **0**.

Après avoir modifié cette valeur, redémarrez le système. FTH ne s’activera plus pour les nouvelles applications.

**Réinitialisation de la liste des applications suivies par FTH**

Le segment de mémoire à tolérance de panne est auto-géré et s’arrête de façon autonome dans le cas où les atténuations ne sont pas effectives pour une application donnée. Toutefois, si vous devez réinitialiser la liste des applications pour lesquelles FTH est en mesure d’atténuer les problèmes (par exemple, si vous testez une application et que vous devez reproduire un incident que FTH est en mesure d’atténuer), vous pouvez exécuter la commande suivante à partir d’une invite de commandes avec élévation de privilèges :  **Rundll32.exe fthsvc.dll, FthSysprepSpecialize**  
**Attention** L’exécution de cette commande entraîne la suppression de toutes les applications FTH, de sorte que les applications qui fonctionnent correctement peuvent commencer à se bloquer après l’exécution de cette commande.  

 

 



