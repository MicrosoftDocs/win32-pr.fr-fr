---
description: ces sections décrivent la mise à jour corrective d’une installation Windows Installer.
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: Application de correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb90436c2a33495aaa818d0796c5d749e5d76286db4dbdc247ec4ee58c7ea6ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926235"
---
# <a name="patching"></a>Application de correctifs

une application installée à l’aide de l’Microsoft Windows Installer peut être mise à niveau en réinstallant un package d’installation mis à jour (fichier .msi), ou en appliquant un correctif Windows Installer (un fichier. msp) à l’application.

un correctif Windows Installer (fichier. msp) est un package autonome qui contient les mises à jour apportées à l’application et décrit les versions de l’application qui peuvent recevoir le correctif. Les correctifs contiennent au minimum deux transformations de base de données et peuvent contenir des fichiers correctifs stockés dans le flux du fichier CAB du package correctif. pour plus d’informations sur les parties d’un package de correctifs Windows Installer, consultez [Packages de correctifs](patch-packages.md).

la maintenance des applications en livrant un correctif Windows Installer, plutôt qu’un package d’installation complet pour le produit mis à jour, peut avoir des avantages. Un correctif peut contenir un fichier entier ou uniquement les bits de fichier nécessaires à la mise à jour d’une partie du fichier. Cela peut permettre à l’utilisateur de télécharger un correctif de mise à niveau qui est plus petit que le package d’installation pour l’ensemble du produit. Une mise à jour à l’aide d’un correctif peut préserver la personnalisation de l’application par le biais de la mise à niveau.

* * Windows Installer 4,5 et versions ultérieures : * *

à partir de Windows Installer 4,5, les développeurs peuvent marquer des composants dans un correctif avec la valeur **msidbComponentAttributesUninstallOnSupersedence** dans la [table des composants](component-table.md). si un patch suivant est installé, marqué avec la valeur **msidbPatchSequenceSupersedeEarlier** dans sa [table MsiPatchSequence](msipatchsequence-table.md) pour remplacer le premier correctif, Windows Installer 4,5 et versions ultérieures peuvent annuler l’inscription et désinstaller des composants marqués **msidbComponentAttributesUninstallOnSupersedence** pour empêcher la conservation des composants inutilisés sur l’ordinateur. Si le composant n’est pas marqué avec ce bit, l’installation du correctif logiciel de remplacement peut rendre un composant inutilisé sur l’ordinateur. La définition de la propriété **MSIUNINSTALLSUPERSEDEDCOMPONENTS** a le même effet que la définition de ce bit pour tous les composants.

* * Windows Installer 3,0 et versions ultérieures : * *

les développeurs qui utilisent Windows Installer 3,0 et créent des packages de correctifs qui ont la [table MsiPatchSequence](msipatchsequence-table.md) peuvent créer des packages de correctifs qui effectuent les opérations suivantes :

-   Utilisez la ligne de base du produit mise en cache par le programme d’installation pour faciliter la maintenance des applications avec des correctifs Delta plus petits. Pour plus d’informations sur l’utilisation de la ligne de base du produit, consultez réduction de la [taille des correctifs](reducing-patch-size.md).
-   Ignorez les actions associées à des tables spécifiques qui ne sont pas modifiées par le correctif. Cela peut réduire considérablement le temps nécessaire à l’installation du correctif. Pour plus d’informations sur les tables qui peuvent être ignorées, consultez [optimisation des correctifs](patch-optimization.md).
-   Créez et installez des correctifs qui peuvent être désinstallés séparément, et dans n’importe quel ordre, sans avoir à désinstaller et réinstaller l’application entière, ainsi que d’autres correctifs. Pour plus d’informations sur la désinstallation des correctifs, consultez [suppression des correctifs](removing-patches.md).
-   Appliquez les correctifs dans un ordre constant, quelle que soit l’ordre dans lequel les correctifs sont fournis au système. pour plus d’informations sur la façon dont le Windows Installer détermine la séquence utilisée pour appliquer les correctifs, consultez [séquencement des correctifs](sequencing-patches.md).
-   Appliquez les correctifs à une application qui a été installée dans un contexte géré par l’utilisateur. Pour plus d’informations, consultez Mise à [jour corrective des Applications Per-User gérées](patching-per-user-managed-applications.md).

* * Windows Installer 2,0 : * *

La [table MsiPatchSequence](msipatchsequence-table.md) n’est pas prise en charge. à partir de Windows Installer 3,0, les packages de correctifs peuvent contenir des informations qui décrivent la séquence de mise à jour corrective du correctif par rapport à d’autres mises à jour et des informations descriptives supplémentaires.

La méthode recommandée pour créer un package de correctif consiste à utiliser des outils de création de correctifs tels que [Msimsp.exe](msimsp-exe.md) et [Patchwiz.dll](patchwiz-dll.md). Les développeurs peuvent générer un fichier de création de correctifs comme décrit dans la section [création d’un package de correctifs](creating-a-patch-package.md). La création d’un correctif logiciel de petite mise à jour est décrite dans la section : [un exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md).

Microsoft Windows Installer accepte une Uniform Resource Locator (URL) comme source valide d’un correctif. Pour plus d’informations sur l’installation d’un correctif situé sur un serveur Web, consultez [téléchargement et installation d’un correctif à partir d’Internet](downloading-and-installing-a-patch-from-the-internet.md).

un seul correctif de Windows Installer (fichier. msp) peut être appliqué au package d’installation lors de l’installation d’une application pour la première fois. Pour plus d’informations, consultez Mise à [jour corrective des installations initiales](patching-initial-installations.md).

Il n’est pas possible d’éliminer toutes les circonstances lorsque l’application d’un correctif peut nécessiter l’accès à la source d’installation d’origine. Toutefois, pour réduire la possibilité que votre correctif nécessite l’accès à la source d’origine, adhérez aux points énumérés dans la section suivante : [empêcher un correctif d’avoir accès à la source d’installation d’origine](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

Pour réduire la possibilité que votre correctif ne soit pas interrompu par une transformation de personnalisation ultérieure, en général, le correctif est installé en premier, suivi de la personnalisation. L’installation préalable des transformations de personnalisation, puis du correctif, risque de perturber la personnalisation. Pour plus d’informations sur la mise à jour corrective des applications personnalisées, consultez Mise à [jour corrective des applications personnalisées](patching-customized-applications.md).

 

 



