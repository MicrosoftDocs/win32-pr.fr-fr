---
description: Utilisez les tables de registre des modules de fusion en fonction du type d’informations de registre.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Création de tables de registre de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03726481905d4efee2405d0b383f53833d840090fea74e2d41fc6ae67a8e5bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066149"
---
# <a name="authoring-merge-module-registry-tables"></a>Création de tables de registre de module de fusion

Utilisez les tables de registre des modules de fusion en fonction du type d’informations de registre.

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a>TypeLib, Class, AppId, ProgId, extension, Verb ou MIME tables

Pour les bibliothèques de types, les classes, les extensions et les verbes, créez les informations du Registre dans la [TypeLib](typelib-table.md), la [classe](class-table.md), l' [AppID](appid-table.md), le [ProgID](progid-table.md), l' [extension](extension-table.md), le [verbe](verb-table.md)ou les tables [MIME](mime-table.md) du module de fusion. si vous utilisez la [table du registre](registry-table.md) pour ajouter ces informations, Windows 2000 ne peut pas fournir de publication à l’ensemble du système pour ces composants.

Les auteurs de modules de fusion peuvent décider de ne pas s’inscrire à l’aide de la table de classes pour les raisons suivantes :

-   Pour être inscrit par la table de classe, le fichier doit être le chemin d’accès du keyPath de son composant. Cela peut nécessiter une modification inacceptable de l’Organisation des composants.
-   Un appel COM peut déclencher une tentative de programme d’installation de réinstaller une classe publiée. Les auteurs peuvent décider de ne pas inscrire une classe à l’aide de la table de classes afin d’éviter de déclencher une réinstallation lorsque l’ordinateur client ne prend pas en charge une interface utilisateur.

## <a name="registry-table"></a>Table du Registre

Utilisez la table Registry pour ajouter des informations de Registre qui ne peuvent pas être créées dans les tables TypeLib, Class, AppId, ProgId, extension, Verb ou MIME. Windows 2000 ne peut pas fournir de publication à l’ensemble du système pour les composants qui utilisent la table du registre.

Lors de la création de la table du Registre, consultez chemins d’accès aux fichiers à l’aide du \[ \# fichier \] ou \[ ! \]Format de fichier plutôt qu’en tant que nom de fichier \[ \] du répertoire. Ce dernier format ne prend pas en charge l’installation à partir de la source. Le format précédent rend également les fichiers manquants et les composants défectueux plus faciles à détecter.

Une attention est nécessaire lors de l’utilisation du texte mis en forme dans la colonne clé de la table du Registre. étant donné que Windows Installer ne réinstalle pas les composants qui sont déjà installés, l’utilisation du texte mis en forme dans ce champ peut entraîner la suppression des clés de registre lors de la suppression de l’application.

## <a name="selfreg-table"></a>Table SelfReg

L’utilisation de la table SelfReg n’est pas recommandée. Pour obtenir la liste des raisons pour lesquelles vous n’utilisez pas l’inscription automatique, consultez la [table Selfreg](selfreg-table.md). Vous devez utiliser la TypeLib, la classe, l’AppId, le ProgId, l’extension, le verbe et les tables MIME dans la mesure du possible et la table du Registre dans tous les autres cas.

 

 



