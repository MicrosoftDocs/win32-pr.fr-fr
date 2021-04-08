---
title: Utilisation de la récupération et du redémarrage de l’application
description: Une application peut utiliser la récupération et le redémarrage de l’application (ARR) pour enregistrer les données et les informations d’État avant la fermeture de l’application en raison d’une exception non gérée ou lorsque l’application cesse de répondre. L’application est également redémarrée, si nécessaire.
ms.assetid: 28cbb4c0-a287-4302-b3a9-daddc69adb40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5bf0b9bd0e0f6cc257ee785ab5df6febc8fef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842365"
---
# <a name="using-application-recovery-and-restart"></a>Utilisation de la récupération et du redémarrage de l’application

Une application peut utiliser la récupération et le redémarrage de l’application (ARR) pour enregistrer les données et les informations d’État avant la fermeture de l’application en raison d’une exception non gérée ou lorsque l’application cesse de répondre. L’application est également redémarrée, si nécessaire.

Lorsque vous vous inscrivez pour la récupération ou le redémarrage, les informations d’inscription sont ajoutées au processus. [Rapport d’erreurs Windows (WER)](/windows/desktop/wer/windows-error-reporting) utilise les informations d’inscription pour appeler votre rappel de récupération et redémarrer votre application. Par exemple, si vous vous inscrivez pour la récupération et que votre application rencontre une exception non gérée, WER affiche une boîte de dialogue à l’utilisateur qui donne à l’utilisateur la possibilité de rechercher une solution en ligne, de fermer le programme ou de déboguer le programme. Si l’utilisateur choisit de rechercher une solution ou de fermer le programme, WER appelle le rappel inscrit et donne à l’application la possibilité d’enregistrer des données et des informations d’État. Une fois la récupération terminée, l’application est arrêtée.

Si vous vous inscrivez au redémarrage et que votre application rencontre une exception non gérée, WER affiche la même boîte de dialogue à l’utilisateur, mais donne la possibilité de redémarrer le programme au lieu de fermer le programme. Si vous vous inscrivez pour la récupération et le redémarrage, la récupération se produit en premier ; l’application est ensuite arrêtée et redémarrée.

Une application qui ne répond pas est traitée de la même façon. Une application est considérée comme ne répondant pas si elle ne répond pas aux messages Windows pendant cinq secondes et que l’utilisateur tente ensuite d’interagir avec l’application. l’utilisateur verra (ne répond pas) dans la barre de titre. WER est activé quand l’utilisateur clique sur le bouton Fermer du système.

Vous devez vous inscrire pour la récupération ou le redémarrage, ou supprimer l’inscription, avant que l’application ne réponde ou qu’elle rencontre une exception non gérée. Toutefois, dans votre rappel de récupération, vous pouvez modifier la ligne de commande de redémarrage.

Pour plus d’informations sur l’inscription pour la récupération ou le redémarrage, consultez les rubriques suivantes :

-   [Inscription pour la récupération d’application](registering-for-application-recovery.md)
-   [Inscription au redémarrage de l’application](registering-for-application-restart.md)

Pour obtenir des exemples qui implémentent les fonctionnalités de récupération et de redémarrage, consultez les exemples AppRecovery et AppRestart dans le SDK Windows situé dans le \\ dossier WinBase WindowsErrorReporting.

 

 