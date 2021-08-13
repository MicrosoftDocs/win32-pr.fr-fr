---
description: Cet événement de contrôle exécute un fichier spécifié. si le fichier n’existe pas ou si l’événement échoue, Windows Installer journalise l’erreur dans le journal détaillé sans afficher de boîte de dialogue contenant un message d’erreur.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982152d58748ba8b1b8f9d302766e1e9c55eb2ee3c9fa0ce7582507c017dc9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627787"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent,

Cet événement de contrôle exécute un fichier spécifié. si le fichier n’existe pas ou si l’événement échoue, Windows Installer journalise l’erreur dans le journal détaillé sans afficher de boîte de dialogue contenant un message d’erreur.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. ce controlevent, est disponible à partir de Windows Installer 5,0.

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Les champs de la valeur de l’argument sont délimités par des espaces. Le premier champ contient une valeur de chaîne qui spécifie le fichier à exécuter. Utilisez la valeur de chaîne \[ \# *filekey* \] pour identifier le fichier et remplacer *filekey* par l’identificateur du fichier figurant dans la colonne fichier de la table de [fichiers](file-table.md) . Les champs restants de l’argument peuvent contenir des paramètres utilisés par le fichier en cours d’exécution.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue aucune action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Pour permettre à un utilisateur de choisir d’exécuter un fichier à la fin d’une installation. Cet événement peut être conditionné sur une propriété définie par un contrôle de [case à cocher](checkbox-control.md) affiché dans la dernière boîte de dialogue de l’installation. Le contrôle de case à cocher ne doit pas être affiché pendant la suppression du package.

 

 



