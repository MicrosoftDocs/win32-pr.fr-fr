---
description: L’action InstallFinalize exécute un script qui contient toutes les opérations de la séquence d’action depuis le début de l’installation ou l’exécution des actions InstallExecute ou InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Action InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753517"
---
# <a name="installfinalize-action"></a>Action InstallFinalize

L’action InstallFinalize exécute un script qui contient toutes les opérations de la séquence d’action depuis le début de l’installation ou l’exécution des actions [InstallExecute](installexecute-action.md) ou [InstallExecuteAgain](installexecuteagain-action.md) . Cette action marque la fin d’une transaction qui commence par l’action [InstallInitialize](installinitialize-action.md) .

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [InstallInitialize](installinitialize-action.md) doit précéder l’action InstallFinalize.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

S’il est détecté que le produit est marqué pour une suppression complète, les opérations sont automatiquement ajoutées au script pour supprimer l' **Ajout/suppression de programmes** dans les informations du **panneau de configuration** du produit, pour annuler l’inscription et annuler la publication du produit, et pour supprimer la base de données locale mise en cache de% Windows%, si elle existe.

Les modifications système effectuées avant l’action ne peuvent pas être restaurées après l’exécution de l’action InstallFinalize. L’action InstallFinalize met à jour le système avec toutes les opérations déterminées à ce point, puis met fin à la transaction.

 

 



