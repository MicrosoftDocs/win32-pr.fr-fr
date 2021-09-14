---
description: La création d’un dossier monté est un processus en deux étapes.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Création de dossiers montés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009905"
---
# <a name="creating-mounted-folders"></a>Création de dossiers montés

La création d’un dossier monté est un processus en deux étapes. Tout d’abord, appelez [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) avec le point de montage (lettre de lecteur, chemin d’accès du GUID du volume ou dossier monté) du volume à affecter au dossier monté. Utilisez ensuite la fonction [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) pour associer le chemin d’accès du GUID du volume retourné au répertoire souhaité sur un autre volume. Pour obtenir un exemple de code, consultez [création d’un dossier monté](mounting-a-volume-at-a-mount-point.md).

Votre application peut désigner n’importe quel répertoire vide sur un volume autre que la racine comme dossier monté. Lorsque vous appelez la fonction [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , ce répertoire devient le dossier monté. Vous pouvez attribuer le même volume à plusieurs dossiers montés.

Une fois le dossier monté établi, il est géré automatiquement par le redémarrage de l’ordinateur.

En cas de défaillance d’un volume, tous les volumes qui ont été affectés aux dossiers montés sur ce volume ne sont plus accessibles via ces dossiers montés. Supposons, par exemple, que vous ayez deux volumes, C : et D :, et que D : soit associé au dossier monté C : monté \\ \\ . Si le volume C : échoue, le volume D : n’est plus accessible via le chemin d’accès C : \\ monté \\ .

Seuls les volumes de système de fichiers NTFS peuvent avoir des dossiers montés, mais les volumes cibles pour les dossiers montés peuvent être des volumes non NTFS.

Les dossiers montés sont implémentés à l’aide de points d’analyse et sont soumis à leurs restrictions. Pour plus d’informations, consultez [points d’analyse](reparse-points.md). Il n’est pas nécessaire de manipuler des points d’analyse pour utiliser des dossiers montés. les fonctions telles que [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) gèrent tous les détails du point d’analyse pour vous.

Étant donné que les dossiers montés sont des répertoires, vous pouvez les renommer, les supprimer, les déplacer et les manipuler, comme vous le feriez pour d’autres annuaires.

(Remarque : la documentation TechNet utilise le terme *lecteurs montés* pour faire référence aux *dossiers montés*.)

 

 



