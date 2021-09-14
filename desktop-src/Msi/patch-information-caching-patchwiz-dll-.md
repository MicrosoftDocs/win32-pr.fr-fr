---
description: La génération d’un correctif peut nécessiter beaucoup de temps.
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: Mise en cache des informations sur les correctifs (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7000efceea62e9eef122a34f7700622e1e6e2e60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218753"
---
# <a name="patch-information-caching-patchwizdll"></a>Mise en cache des informations sur les correctifs (Patchwiz.dll)

La génération d’un correctif peut nécessiter beaucoup de temps. Une fois que vous avez généré un correctif à l’aide de [Patchwiz.dll](patchwiz-dll.md), vous devrez peut-être modifier à nouveau l’image de mise à jour et générer un autre correctif. La mise en cache des informations sur les correctifs peut réduire le temps nécessaire à la génération des correctifs suivants en réutilisant les correctifs existants. Par exemple, le temps nécessaire pour créer des service packs peut être réduit à l’aide des correctifs binaires générés à partir des correctifs précédents. Patchwiz.dll pouvez utiliser \_ le répertoire du cache des correctifs \_ pour rechercher un correctif binaire existant et l’ajouter au fichier cab de Service Pack sans avoir à recréer le correctif binaire.

La mise en cache des informations sur les correctifs requiert l’utilisation de [Patchwiz.dll](patchwiz-dll.md). Pour activer la mise en cache des correctifs, définissez les propriétés cache des correctifs \_ \_ activé et \_ répertoire du cache des correctifs \_ dans la [table des propriétés (Patchwiz.dll)](properties-table-patchwiz-dll-.md) du fichier de propriétés de création de correctifs (fichier. PCP). Patchwiz stocke toutes les informations relatives à la création de correctifs dans le dossier identifié par la \_ propriété de répertoire du cache des correctifs \_ et crée ce dossier si nécessaire. Lors de la prochaine tentative de création d’un correctif, Patchwiz vérifie ce dossier pour déterminer si les fichiers à comparer correspondent aux fichiers du cache. Si les fichiers correspondent, Patchwiz utilise les informations mises en cache au lieu de régénérer le correctif binaire pour le fichier. Si les fichiers ne correspondent pas, ou si les informations sont manquantes dans le cache, Patchwiz génère le correctif pour le fichier.

Pour utiliser la mise en cache des informations sur les correctifs, le dossier spécifié par le \_ répertoire du cache des correctifs \_ doit être conservé après la création d’un fichier. msp. Si le dossier est supprimé, PatchWiz doit régénérer les correctifs binaires pour les fichiers. msp suivants. Pour plus d’informations sur la préservation des informations dans les régions sélectionnées d’un fichier cible, consultez Mise à [jour corrective des régions sélectionnées d’un fichier](patching-selected-regions-of-a-file.md).

 

 



