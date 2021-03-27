---
description: Il n’existe essentiellement aucune contrainte sur la façon d’écrire une application de démarrage de l’exécution automatique.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Comment implémenter des applications de démarrage AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951941"
---
# <a name="how-to-implement-autorun-startup-applications"></a>Comment implémenter des applications de démarrage AutoRun

Il n’existe essentiellement aucune contrainte sur la façon d’écrire une application de démarrage de l’exécution automatique. Vous pouvez implémenter l’application de démarrage pour effectuer toutes les tâches nécessaires à l’installation, à la désinstallation, à la configuration ou à l’exécution de votre application. Toutefois, les conseils suivants fournissent des instructions pour l’implémentation d’une application de démarrage automatique efficace.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Assurez-vous que les utilisateurs reçoivent des commentaires le plus rapidement possible après avoir inséré un disque d’exécution automatique dans le lecteur. Les applications de démarrage doivent être des petits programmes qui se chargent rapidement. Ils doivent identifier clairement l’application et fournir un moyen simple d’annuler l’opération.

### <a name="step-2"></a>Étape 2 :

Vérifiez si le programme est déjà installé. Si ce n’est pas le cas, l’étape suivante sera probablement la procédure d’installation. L’application de démarrage peut tirer parti du temps que l’utilisateur passe à lire la boîte de dialogue en démarrant un autre thread pour commencer le chargement du code d’installation. Au moment où l’utilisateur clique sur **OK**, votre programme d’installation sera déjà en partie s’il n’est pas entièrement chargé. Cette approche réduit considérablement la perception de l’utilisateur quant au temps nécessaire au chargement de votre application.

> [!Note]  
> En règle générale, la partie initiale de l’application de démarrage présente aux utilisateurs une interface utilisateur, telle qu’une boîte de dialogue, en leur demandant comment ils souhaitent continuer.

 

### <a name="step-3"></a>Étape 3 :

Démarrez un autre thread pour commencer à charger le code de l’application afin de réduire le temps d’attente pour l’utilisateur. Si l’application a déjà été installée, l’utilisateur a probablement inséré le disque pour exécuter l’application.

### <a name="step-4"></a>Étape 4 :

Utilisez les indications suivantes pour réduire l’utilisation du disque dur :

-   Conservez au minimum le nombre de fichiers qui doivent se trouver sur le disque dur. Ils doivent être limités aux fichiers essentiels pour exécuter le programme ou qui prennent un temps de lecture beaucoup plus important à partir du média.
-   Dans de nombreux cas, l’installation de fichiers non essentiels sur le disque dur n’est pas nécessaire, mais peut fournir des avantages tels que l’augmentation des performances. Donnez à l’utilisateur la possibilité de décider comment effectuer le compromis entre les coûts et les avantages du stockage sur disque dur.
-   Fournir un moyen de désinstaller tous les composants qui ont été placés sur le disque dur.
-   Si votre application met en cache des données, donnez-lui un contrôle de l’utilisateur. Incluez les options dans l’application de démarrage, telles que la définition d’une limite sur la quantité maximale de données mises en cache qui seront stockées sur le disque dur, ou la suppression des données mises en cache par l’application lorsqu’elle se termine.

### <a name="step-5"></a>Étape 5 :

Désactivez l’exécution automatique si nécessaire. L’exécution automatique peut être supprimée par programmation ou désactivée entièrement avec le registre, même si un support a un fichier autorun. inf. Pour plus d’informations [, consultez Activation et désactivation de l’exécution automatique](autoplay-reg.md) .

 

 



