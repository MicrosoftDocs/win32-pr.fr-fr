---
description: .
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Meilleures pratiques pour l’efficacité énergétique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a9980d199e2d95c6dbd01c642a1f00f45e584c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525725"
---
# <a name="best-practices-for-energy-efficiency"></a>Meilleures pratiques pour l’efficacité énergétique

## <a name="platform"></a>Plateforme

 **Clients** – Windows XP Windows \| Vista Windows \| 7  

## <a name="description"></a>Description

Les ordinateurs portables Windows doivent satisfaire aux exigences réglementaires en matière d’efficacité énergétique, telles que celles du programme Energy Star de l’Agence de protection environnementale (EPA) États-Unis. En outre, les enquêtes montrent que la durée de vie de la batterie est plus longue que celle des ordinateurs portables. Pour répondre aux demandes des consommateurs, les ordinateurs portables Windows doivent continuellement avancer dans les domaines suivants :

-   Efficacité énergétique dans tous les scénarios d’utilisation, y compris les charges de travail inactives, la productivité des DVD et les supports, ainsi que les tests de performances du secteur
-   Autonomie de la batterie d’un ordinateur portable — pour les plateformes matérielles et pour Windows

La plate-forme Windows est très fiable et permet d’accélérer les performances. Toutefois, les extensions fournies avec les systèmes d’ordinateurs portables, telles que les services, les applets de barre d’état système, les pilotes et autres logiciels, peuvent affecter considérablement les performances, la fiabilité et l’efficacité énergétique.

L’efficacité énergétique est un problème complexe, avec les facteurs affectés par et affectant tous les éléments de l’écosystème du PC. Des améliorations mineures dans plusieurs scénarios peuvent améliorer l’efficacité énergétique, mais une application, un appareil ou une fonctionnalité système à performances médiocres peut augmenter considérablement la consommation d’énergie.

Le matériel et les périphériques constituent la base de l’efficacité énergétique. Toutefois, les logiciels d’application et de service doivent également être efficaces pour permettre au système d’atteindre une autonomie de batterie optimale. Chaque composant logiciel sur le système, y compris le système d’exploitation et les applications et services à valeur ajoutée, doit respecter les règles de performances de base. Une application ou un service à dysfonctionnement unique peut éliminer tout gain d’efficacité énergétique que le dernier processeur, les périphériques ou le matériel de la plateforme ont atteint. Pour plus d’informations sur la durée de vie de la batterie et l’efficacité énergétique, reportez-vous au [Guide des solutions de durée de vie des batteries](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#).

Les principaux problèmes et les composants qui affectent la durée de vie de la batterie sur un ordinateur portable sont les suivants :

**Caractéristiques de la batterie**

-   La taille, le type et la qualité de la capacité de la batterie affectent la durée de vie de la batterie
-   Plus la batterie est grande, plus l’alimentation est grande
-   Les batteries plus grandes sont plus chères et plus lourdes ; les utilisateurs préfèrent les systèmes plus légers

**Composants matériels**

-   Fréquence et profondeur auxquelles le matériel peut entrer dans des États d’alimentation inférieurs
-   Prise en charge matérielle des États de faible consommation d’énergie
-   Optimisation du pilote pour l’efficacité énergétique

**Système d’exploitation-gestion de l’alimentation dirigée**

-   Efficacité du code Windows en temps de chargement et en mode inactif
-   Niveau de coopération de tous les composants avec la gestion de l’alimentation dirigée vers Windows
-   Configuration appropriée du système d’exploitation pour optimiser la gestion de l’alimentation via les paramètres de stratégie d’alimentation

**Logiciels et services d’application**

-   Efficacité des applications, des pilotes et des services tout en étant sous une charge et en mode inactif
-   Niveau de coopération des applications avec Windows – gestion de l’alimentation dirigée
-   Remise des logiciels du système ou des appareils pour qu’ils soient en état d’inactivité faible

Une application ou un composant de service unique peut empêcher un système de réaliser une autonomie de batterie optimale. Bien que Windows fournisse de nombreuses options de configuration de l’alimentation, les logiciels préinstallés ou les paramètres de stratégie d’alimentation sur de nombreux systèmes ne sont pas optimisés pour la plateforme matérielle de l’ordinateur hôte.

Une méthode courante pour évaluer l’impact sur la durée de vie de la batterie des logiciels préinstallés consiste à comparer la consommation énergétique du système avec une installation propre de Windows et une installation Windows qui comprend des logiciels et des services à valeur ajoutée. Bien qu’une nouvelle installation ne représente pas la plateforme standard que les fabricants d’ordinateurs OEM livrent aux clients, la comparaison de la consommation d’énergie peut fournir un aperçu de l’efficacité énergétique des logiciels préinstallés.

## <a name="best-practices"></a>Bonnes pratiques

Pour vous assurer que votre application est optimisée sur les plateformes Windows, suivez ces meilleures pratiques quand vous concevez des applications ou des services :

-   **Évitez d’utiliser des minuteries périodiques à haute résolution**

<dl> Utilisation de minuteries périodiques haute résolution (<10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   **Investir dans des optimisations de performances**

<dl> Chaque optimisation des performances est une optimisation de la durée de vie de la batterie. Les réductions des ressources requises, telles que l’utilisation de temps processeur réduit ou de lectures de disque par lot/cluster, permettent au matériel système de devenir inactif et de passer en mode faible consommation d’énergie.  
</dl>

-   **Ajuster à la stratégie d’alimentation de l’utilisateur**

<dl> Windows Vista et les versions ultérieures permettent à l’utilisateur de choisir facilement les économies d’énergie globales ou le comportement des performances du système. Votre application doit répondre aux modifications apportées à la stratégie d’alimentation et réduire l’utilisation des ressources ou améliorer les performances en conséquence. Par exemple, une application doit désactiver l’activité en arrière-plan, telle que l’indexation ou l’analyse du système lorsque l’utilisateur a sélectionné un mode de gestion de l’alimentation.  
</dl>

-   **Réduire l’utilisation des ressources lorsque le système est alimenté par batterie**

<dl> Votre application doit réduire son utilisation des ressources (par exemple, la fréquence de mise à jour en arrière-plan) quand le système est alimenté par batterie.  
</dl>

-   **Ne pas afficher dans l’affichage lorsqu’il est désactivé**

<dl> L’affichage du système peut être désactivé pour les économies d’énergie. Votre application ne doit pas effectuer de rendu graphique inutile lorsque l’affichage est désactivé, car cela gaspille les ressources système et la puissance.  
</dl>

-   **Éviter l’interrogation et la rotation dans des boucles serrées**

<dl> Une utilisation intensive du processeur réduit l’efficacité des technologies de gestion de l’alimentation du processeur, telles que les États d’inactivité du processeur et les États des performances du processeur.  
</dl>

-   **N’empêchez pas le système de désactiver l’affichage ou le ralenti pour le mettre en veille**

<dl> Votre application doit faire des demandes d’alimentation judicieuses avec l’API SetThreadExecutionState. Le système doit effectuer ces requêtes uniquement lorsque les opérations critiques doivent retarder l’arrêt de l’affichage ou l’entrée automatique en mode veille.  
</dl>

-   **Répondre aux événements courants de gestion de l’alimentation**

<dl> Votre application doit s’inscrire aux événements de gestion de l’alimentation courants et y répondre, tels que les modifications de source d’alimentation du système et les notifications de mise sous tension et de mise hors tension pour l’affichage.  
</dl>

-   **N’activez pas la journalisation du débogage par défaut ; Utilisez à la place Suivi d’v nements pour Windows**

<dl> La journalisation de débogage périodique peut empêcher la rotation du disque.  
</dl>

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Guide des solutions de durée de vie de la batterie](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [Portail d’efficacité énergétique](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



