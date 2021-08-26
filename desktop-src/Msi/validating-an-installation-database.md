---
description: Les auteurs des packages d’installation doivent toujours exécuter la validation sur leurs packages avant d’essayer d’installer le package pour la première fois et de réexécuter la validation chaque fois que vous apportez des modifications au package.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Validation d’une base de données d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28d4d1937b5946d6c1df85a4c6c21ec8113ef6463b5aaad0e181f4bdc711e70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995819"
---
# <a name="validating-an-installation-database"></a>Validation d’une base de données d’installation

Les auteurs des packages d’installation doivent toujours exécuter la validation sur leurs packages avant d’essayer d’installer le package pour la première fois et de réexécuter la validation chaque fois que vous apportez des modifications au package. La validation analyse la base de données à la recherche d’erreurs qui peuvent sembler valides individuellement, mais qui entraînent un comportement incorrect dans le contexte de la base de données entière. Toute tentative d’installation d’un package dont la validation échoue peut endommager le système de l’utilisateur. Consultez les sections [validation de package](package-validation.md) et [évaluateur de cohérence interne-ICEs-v](internal-consistency-evaluators-ices.md).

Vous pouvez valider l’exemple de package à l’aide de [Orca.exe](orca-exe.md) ou [Msival2.exe](msival2-exe.md). Pour afficher l’aide de Msival2.exe modifier les répertoires et entrez sur la ligne de commande.

Msival2 -?

Le fichier. CUB Darice. CUB contient les actions personnalisées ICE requises par Msival2.exe pour effectuer la validation. Pour valider le MNP2000.msi entrée

MSIVal2 MNP2000.msi Darice. CUB

Pour obtenir une description des messages d’erreur et d’avertissement retournés par la validation, consultez la [référence Ice](ice-reference.md). Corrigez toutes les erreurs dans le package et réexécutez la validation si nécessaire, jusqu’à ce que le package ait réussi la validation sans erreurs.

Une fois que le package a réussi la validation, vous pouvez installer l’exemple de package en cliquant sur l’icône MNP2000.msi ou sur la ligne de commande à l’aide des [options de ligne de commande](command-line-options.md).

Cela termine l’installation de l’exemple.

## <a name="next-example"></a>Exemple suivant

[Exemple de mise à niveau](an-upgrade-example.md)

 

 



