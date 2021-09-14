---
description: à partir de Windows Installer version 3,0, les rédacteurs de correctifs peuvent utiliser la référence de produit mise en cache par le programme d’installation pour faciliter le service des applications avec des correctifs delta plus petits.
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: Réduction de la taille des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa365e831ab8685073347dc254bac58269135f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009705"
---
# <a name="reducing-patch-size"></a>Réduction de la taille des correctifs

à partir de Windows Installer version 3,0, les rédacteurs de correctifs peuvent utiliser la référence de produit mise en cache par le programme d’installation pour faciliter le service des applications avec des correctifs delta plus petits. Dans de nombreux cas, un [*correctif Delta*](d-gly.md) qui fournit des informations de maintenance à une application peut être considérablement plus petit qu’un correctif de fichier complet ou un package d’installation qui fournit les mêmes informations.

**Windows Installer 2,0 :** Non pris en charge. à partir de Windows Installer 3,0, le programme d’installation enregistre de manière sélective les informations de référence sur les fichiers lorsqu’ils sont mis à jour.

Windows Le programme d’installation de propose trois méthodes de mise à jour et de maintenance des applications : [petites mises à jour](small-updates.md), mises à [niveau mineures](minor-upgrades.md)et [mises à niveau majeures](major-upgrades.md). Une petite mise à jour est également appelée mise à jour QFE (Quick Fix Engineering) et une mise à niveau mineure est également appelée mise à jour de Service Pack (SP). Une mise à niveau majeure classique supprime une application précédente et installe une nouvelle application. Windows Le programme d’installation peut fournir des informations de maintenance aux applications sous la forme d’un [package d’installation](installation-package.md) (fichier .msi) ou d’un [package correctif](patch-packages.md) (fichier. msp).

un package de correctifs Windows Installer qui fournit des informations de maintenance pour une petite mise à jour ou une mise à niveau mineure est généralement bien plus petit que le package d’installation équivalent qui fournit les mêmes informations de maintenance. Il est recommandé d’utiliser des packages de correctifs pour la distribution de petites et mineures mises à niveau. Il est recommandé d’utiliser un package d’installation pour la distribution d’une mise à niveau majeure.

Windows Les correctifs du programme d’installation (fichiers. msp) peuvent être générés soit à partir de fichiers complets, soit à partir de différences de fichiers (également appelées deltas de fichiers). un correctif Windows Installer généré à partir de deltas de fichiers peut être plus petit que le correctif de fichier complet équivalent. toutes les versions du Windows Installer peuvent utiliser des correctifs de fichiers complets ou des correctifs delta.

à partir de Windows Installer version 3,0, le programme d’installation enregistre de manière sélective les informations de référence sur les fichiers lorsqu’ils sont mis à jour. Les informations relatives à l’application de base d’origine (version RTM) et à la mise à niveau mineure la plus récente (Service Pack) sont enregistrées dans un emplacement privé lorsque l’application est installée ou reçoit une mise à niveau mineure.

Le programme d’installation effectue les opérations suivantes pour réduire la taille du cache de base :

-   Plus de deux lignes de base sont conservées pour chaque application : une ligne de base du fichier à l’origine (RTM) et une ligne de base du fichier au moment de la mise à niveau mineure la plus récente (Service Pack.)
-   Un fichier n’est pas ajouté au cache tant qu’il n’est pas corrigé. Le cache de base est copié en écriture.
-   Si l’application n’a jamais été mise à jour, il n’y a aucun fichier dans le cache de base.
-   Lorsque la dernière maintenance de l’application était une mise à niveau mineure (Service Pack), l’application se trouve au niveau de la ligne de base et au maximum deux copies d’un fichier peuvent être présentes sur l’ordinateur. Une copie du fichier se trouve dans le répertoire cible de l’installation. L’autre copie peut être dans le cache de base de la version RTM.
-   Lorsque la dernière maintenance de l’application était une petite mise à jour (QFE), l’application n’est pas au niveau de la ligne de base et au plus trois copies d’un fichier peuvent être présentes sur l’ordinateur. La première copie du fichier se trouve dans le répertoire cible de l’installation. La deuxième copie du fichier se trouve dans le cache de base de données RTM. La dernière copie du fichier se trouve dans le cache de base de référence le plus récent.
-   Le cache de base de l’application est supprimé lors de la désinstallation du produit.

à partir de Windows Installer version 3,0, le programme d’installation peut utiliser le cache de base lorsque des correctifs sont appliqués à l’application. Les informations de ligne de base peuvent être utilisées pour appliquer un correctif Delta ou pour rétablir une version antérieure d’un fichier pendant la désinstallation d’un correctif. Cela peut permettre aux auteurs de correctifs de bénéficier de plus petits correctifs Delta. Si le programme d’installation détecte que le correctif delta ne peut pas être appliqué au fichier cible, le programme d’installation peut tenter d’utiliser un fichier enregistré dans le cache de base comme point de départ. Le programme d’installation n’a besoin que de demander la source d’installation d’origine après avoir essayé toutes les possibilités du cache.

l’adhérence aux instructions suivantes peut aider les auteurs des correctifs à utiliser Windows Installer correctifs de la version 3,0 et le cache de base pour créer des correctifs delta plus petits :

-   Créez des correctifs qui incluent la [table MsiPatchSequence](msipatchsequence-table.md). cette table est requise pour utiliser le cache de base et est disponible à partir de Windows Installer version 3,0.
-   Ne définissez pas de stratégie qui empêche la mise en cache de base. La valeur de la stratégie [MaxPatchCacheSize](maxpatchcachesize.md) spécifie le pourcentage maximal d’espace disque qui peut être utilisé. Si la stratégie MaxPatchCacheSize est définie sur 0, aucun fichier supplémentaire n’est enregistré dans le cache de base. Si la stratégie n’est pas définie, la valeur par défaut est qu’un maximum de 10% de l’espace disque peut être utilisé. Si la taille totale du cache atteint le pourcentage maximal d’espace disque, aucun fichier supplémentaire n’est enregistré. La stratégie n’affecte pas les fichiers qui ont déjà été enregistrés. Même lorsque la mise en cache est désactivée, le programme d’installation peut utiliser les caches de référence de produit existants.
-   Si le premier correctif appliqué comprend la [table MsiPatchSequence](msipatchsequence-table.md), la mise en cache est activée pour l’application.
-   Si un correctif de la transaction de maintenance n’inclut pas la [table MsiPatchSequence](msipatchsequence-table.md), la mise en cache est activée pour l’application uniquement si un correctif de mise à niveau mineure (Service Pack) incluant la table MsiPatchSequence est appliqué avec succès au produit.
-   Générez le package de correctifs à l’aide d’outils de création de correctifs tels que [Msimsp.exe](msimsp-exe.md) et [PATCHWIZ.DLL](patchwiz-dll.md).
-   Toujours cibler les correctifs pour la version RTM de l’application ou une version de mise à niveau mineure (Service Pack) de l’application. Les cibles spécifiées dans la [table TargetImages](targetimages-table-patchwiz-dll-.md) du fichier de propriétés de création de correctif (PCP) doivent être des points de vérification de produit définis par les trois premiers champs de la propriété [**ProductVersion**](productversion.md) .
-   Ne ciblez jamais les correctifs de petites images de mise à jour. Les cibles pour la génération du correctif ne doivent pas inclure les images de mise à niveau de petite mise à jour précédentes.

 

 



