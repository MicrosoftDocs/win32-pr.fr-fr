---
description: Contient des informations sur l’interface de programmation pour le service de configuration sans fil de Zero sur Windows XP et Windows Server 2003.
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: Référence de configuration sans fil Zero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebe202e16aa38fef617f382559f124772d50a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202734"
---
# <a name="wireless-zero-configuration-reference"></a>Référence de configuration sans fil Zero

\[L’interface de programmation de configuration automatique sans fil n’est plus prise en charge à compter de Windows Vista et de Windows Server 2008. Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires. Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]

Cette section contient des informations sur l’interface de programmation pour le service de configuration sans fil de Zero sur Windows XP et Windows Server 2003. Les rubriques sont les suivantes :

-   [Fonctions de configuration sans fil Zero](wireless-zero-configuration-functions.md)
-   [Structures de configuration sans fil Zero](wireless-zero-configuration-structures.md)

La configuration sans fil Zero est un service Windows sur Windows XP et Windows Server 2003 qui est utilisé pour configurer et gérer les connexions de réseau sans fil sur une carte sans fil. Le nom du service pour la configuration sans fil Zero est WZCSVC. Sur Windows XP, le nom complet du service WZCSVC est la configuration sans fil de zéro. Sur Windows Server 2003, le nom complet du service WZCSVC est configuration sans fil.

Le service de configuration sans fil Zero est normalement démarré au moment du démarrage. L’interface de programmation du service de configuration automatique sans fil ne peut être utilisée que si le service de configuration sans fil Zero a été démarré. Si le service de configuration sans fil de zéro n’est pas démarré, les fonctions de configuration sans fil ne retournent pas d’erreur.

Pour activer le service de configuration automatique sans fil afin qu’il démarre automatiquement, accédez au bouton **Démarrer** . Sélectionnez l’option **paramètres** , puis sélectionnez **panneau** de configuration. Si vous utilisez l’affichage Windows XP, sélectionnez la catégorie **performances et maintenance** , puis **Outils d’administration**. Si vous utilisez l’affichage classique, sélectionnez **Outils d’administration**. Cliquez sur l’icône **services** dans le volet gauche. Cliquez sur l’icône Configuration sans fil Zero dans le volet droit, puis remplacez le **type de démarrage** Dropbox par **automatique**. Ce paramètre configure le service pour qu’il démarre automatiquement au moment du démarrage. Cliquez ensuite sur le bouton **Démarrer** pour démarrer le service de configuration sans fil Zero sans fil, puis cliquez sur le bouton **OK** .

La configuration sans fil Zero peut également être démarrée et arrêtée à partir d’une invite de commandes. Pour démarrer la configuration sans fil de zéro, exécutez la commande suivante :

**NET START wzcsvc**

Pour arrêter la configuration sans fil de zéro, exécutez la commande suivante :

**net stop wzcsvc**

 

 



