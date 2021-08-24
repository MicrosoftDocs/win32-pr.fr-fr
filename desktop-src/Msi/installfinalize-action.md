---
description: L’action InstallFinalize exécute un script qui contient toutes les opérations de la séquence d’action depuis le début de l’installation ou l’exécution des actions InstallExecute ou InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Action InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8bd3ac9473fab868e5f7d83e760b39ca4dd6136faec987b5a7d2a3777bdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787039"
---
# <a name="installfinalize-action"></a>Action InstallFinalize

L’action InstallFinalize exécute un script qui contient toutes les opérations de la séquence d’action depuis le début de l’installation ou l’exécution des actions [InstallExecute](installexecute-action.md) ou [InstallExecuteAgain](installexecuteagain-action.md) . Cette action marque la fin d’une transaction qui commence par l’action [InstallInitialize](installinitialize-action.md) .

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [InstallInitialize](installinitialize-action.md) doit précéder l’action InstallFinalize.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Remarques

S’il est détecté que le produit est marqué pour une suppression complète, les opérations sont automatiquement ajoutées au script pour supprimer l' **Ajout/suppression de programmes** dans les informations du **panneau de configuration** du produit, pour annuler l’inscription et annuler la publication du produit, et pour supprimer la base de données locale mise en cache de% Windows%, si elle existe.

Les modifications système effectuées avant l’action ne peuvent pas être restaurées après l’exécution de l’action InstallFinalize. L’action InstallFinalize met à jour le système avec toutes les opérations déterminées à ce point, puis met fin à la transaction.

 

 



