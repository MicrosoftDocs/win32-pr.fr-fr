---
description: Cet événement de contrôle exécute un fichier spécifié. Si le fichier n’existe pas ou si l’événement échoue, Windows Installer journalise l’erreur dans le journal détaillé sans afficher de boîte de dialogue contenant un message d’erreur.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521470"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent,

Cet événement de contrôle exécute un fichier spécifié. Si le fichier n’existe pas ou si l’événement échoue, Windows Installer journalise l’erreur dans le journal détaillé sans afficher de boîte de dialogue contenant un message d’erreur.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. Ce ControlEvent, est disponible à partir de Windows Installer 5,0.

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Les champs de la valeur de l’argument sont délimités par des espaces. Le premier champ contient une valeur de chaîne qui spécifie le fichier à exécuter. Utilisez la valeur de chaîne \[ \# *filekey* \] pour identifier le fichier et remplacer *filekey* par l’identificateur du fichier figurant dans la colonne fichier de la table de [fichiers](file-table.md) . Les champs restants de l’argument peuvent contenir des paramètres utilisés par le fichier en cours d’exécution.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue aucune action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Pour permettre à un utilisateur de choisir d’exécuter un fichier à la fin d’une installation. Cet événement peut être conditionné sur une propriété définie par un contrôle de [case à cocher](checkbox-control.md) affiché dans la dernière boîte de dialogue de l’installation. Le contrôle de case à cocher ne doit pas être affiché pendant la suppression du package.

 

 



