---
title: Ajout, suppression et remplacement de ressources
description: Cette rubrique explique comment ajouter, supprimer ou remplacer des ressources.
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c12a1531e422efe44cbd0b3deca9f89838698
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412864"
---
# <a name="adding-deleting-and-replacing-resources"></a>Ajout, suppression et remplacement de ressources

Les applications doivent souvent ajouter, supprimer ou remplacer des ressources dans des fichiers exécutables. Vous pouvez utiliser deux méthodes pour accomplir ces tâches. La première consiste à modifier le fichier de définition de ressource, à recompiler les ressources et à ajouter les ressources recompilées au fichier exécutable de l’application. La deuxième méthode consiste à copier les données de ressources directement dans le fichier exécutable de l’application.

Par exemple, pour localiser une application en langue anglaise en vue de son utilisation en Norvège, il peut être nécessaire de remplacer la boîte de dialogue en anglais par une autre à l’aide de norvégien. Un développeur crée une boîte de dialogue appropriée à l’aide d’un éditeur de boîtes de dialogue ou en écrivant un modèle dans le fichier de définition de ressource. Le développeur RECOMPILE ensuite les ressources et ajoute les nouvelles ressources au fichier exécutable de l’application.

Toutefois, si une boîte de dialogue appropriée existe sous forme binaire, le développeur peut copier les données directement dans le fichier exécutable localisé à l’aide des fonctions suivantes. La fonction [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) crée un descripteur de mise à jour du fichier exécutable dont les ressources doivent être modifiées. La fonction [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) utilise ce handle pour ajouter, supprimer ou remplacer une ressource dans le fichier exécutable. La fonction [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) ferme le handle.

Après la création d’un descripteur de mise à jour d’un fichier exécutable par [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea), une application peut utiliser [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) à plusieurs reprises pour apporter des modifications aux données de ressource. Chaque appel à **UpdateResource** contribue à une liste interne d’ajouts, de suppressions et de remplacements, mais n’écrit pas réellement les données dans le fichier exécutable. Juste avant de fermer le descripteur de mise à jour, [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) écrit les modifications accumulées dans le fichier exécutable.

Parfois, une application doit copier des ressources à partir d’un autre fichier. La [mise à jour des ressources](using-resources.md) montre un exemple d’obtention des données de ressources et de leur taille à partir d’un fichier.

 

 




