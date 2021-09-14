---
title: Erreurs MCI générales
description: Erreurs MCI générales
ms.assetid: be9c4a2b-44bc-410c-be74-ba55bb4e785b
keywords:
- MCIERR les valeurs de retour, erreurs générales
- Référence multimédia, erreurs MCI
- référence pour les erreurs multimédias, MCI
- MCI (Media Control Interface), erreurs générales
- MCI (interface de contrôle multimédia), erreurs générales
- informations de référence sur MCI, erreurs générales
- Informations de référence sur MCI, erreurs générales
- MCI (Media Control Interface), Erreurs
- MCI (interface de contrôle multimédia), Erreurs
- informations de référence sur MCI, Erreurs
- Informations de référence sur MCI, Erreurs
- mciSendCommand fonction)
- mciSendString fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44538937be73c2ccfb1d30de1f1a1c729cc05095
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021192"
---
# <a name="general-mci-errors"></a>Erreurs MCI générales

Les valeurs d’erreur suivantes peuvent être retournées par la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) ou [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :



| Valeur                            | Signification                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ \_ format d’heure incorrect \_        | La valeur spécifiée pour le format d’heure n’est pas valide.                                                                                                         |
| MCIERR \_ ne peut pas \_ charger le \_ pilote     | Le pilote de périphérique spécifié ne se chargera pas correctement.                                                                                                         |
| MCIERR \_ ne peut pas \_ utiliser \_ tout         | Le nom de l’appareil « All » n’est pas autorisé pour cette commande.                                                                                                      |
| MCIERR \_ CREATEWINDOW             | Impossible de créer ou d’utiliser la fenêtre.                                                                                                                             |
| longueur de l' \_ appareil MCIERR \_           | Le nom de l’appareil ou du pilote est trop long. Spécifiez un nom de périphérique ou de pilote inférieur à 79 caractères.                                                     |
| \_appareil MCIERR \_ verrouillé           | L’appareil est en cours de fermeture. Patientez quelques secondes, puis réessayez.                                                                                         |
| \_appareil MCIERR \_ non \_ installé   | L’appareil spécifié n’est pas installé sur le système. Utilisez l’option pilotes du panneau de configuration pour installer l’appareil.                                   |
| \_appareil MCIERR \_ non \_ prêt       | Le pilote de périphérique n’est pas prêt.                                                                                                                             |
| \_appareil MCIERR \_ ouvert             | Le nom de l’appareil est déjà utilisé en tant qu’alias par cette application. Utilisez un alias unique.                                                                        |
| longueur de la \_ CDE d’appareil MCIERR \_ \_      | Le nom de l’appareil ou du pilote est trop long. Spécifiez un nom de périphérique ou de pilote inférieur à 79 caractères.                                                     |
| \_type d’appareil MCIERR \_ \_ requis   | L’appareil spécifié est introuvable sur le système. Vérifiez que l’appareil est installé et que le nom de l’appareil est correctement orthographié.                            |
| \_pilote MCIERR                   | Le pilote de périphérique présente un problème. Contactez le fabricant de l’appareil pour obtenir un nouveau pilote.                                                      |
| \_pilote MCIERR \_ interne         | Le pilote de périphérique présente un problème. Contactez le fabricant de l’appareil pour obtenir un nouveau pilote.                                                      |
| \_alias DUPLIQUÉ \_ MCIERR         | L’alias spécifié est déjà utilisé dans cette application. Utilisez un alias unique.                                                                                |
| \_extension MCIERR \_ \_ introuvable    | L’extension spécifiée n’est associée à aucun type d’appareil. Spécifiez un type d’appareil.                                                                       |
| MCIERR \_ \_ caractères supplémentaires        | Vous devez placer une chaîne entre guillemets ; les caractères qui suivent les guillemets fermants ne sont pas valides.                                              |
| \_fichier MCIERR \_ \_ introuvable         | Le fichier demandé est introuvable. Vérifiez que le chemin d’accès et le nom de fichier sont corrects.                                                                             |
| \_fichier MCIERR \_ non \_ enregistré         | Le fichier n’a pas été enregistré. Vérifiez que votre système dispose de suffisamment d’espace disque ou d’une connexion réseau intacte.                                                |
| \_lecture du fichier MCIERR \_               | Une lecture à partir du fichier a échoué. Assurez-vous que le fichier est présent sur votre système ou que votre système dispose d’une connexion réseau intacte.                             |
| \_écriture du fichier MCIERR \_              | Une écriture dans le fichier a échoué. Vérifiez que votre système dispose de suffisamment d’espace disque ou d’une connexion réseau intacte.                                            |
| \_nom de fichier MCIERR \_ requis       | Le nom de fichier n’est pas valide. Assurez-vous que le nom de fichier ne dépasse pas huit caractères, suivis d’un point et d’une extension.                                  |
| \_indicateurs MCIERR \_ non \_ compatibles   | Les paramètres spécifiés ne peuvent pas être utilisés ensemble.                                                                                                           |
| MCIERR \_ Télécharger le \_ CD                  | Le fichier demandé ou le périphérique MCI est introuvable. Essayez de changer de répertoire ou de redémarrer votre système.                                                         |
| \_matériel MCIERR                 | L’appareil spécifié présente un problème. Vérifiez que l’appareil fonctionne correctement ou contactez le fabricant de l’appareil.                                     |
| MCIERR \_ non conforme \_ pour l' \_ \_ ouverture automatique | MCI n’exécutera pas la commande spécifiée sur un appareil automatiquement ouvert. Attendez que l’appareil soit fermé, puis essayez d’exécuter la commande.             |
| MCIERR \_ interne                 | Un problème s’est produit lors de l’initialisation de MCI. essayez de redémarrer le système d’exploitation Windows.                                                                        |
| MCIERR \_ \_ ID d’appareil non valide \_      | ID d’appareil non valide. Utilisez l’ID donné à l’appareil lorsque l’appareil a été ouvert.                                                                               |
| MCIERR \_ \_ nom de périphérique non valide \_    | L’appareil spécifié n’est pas ouvert ou n’est pas reconnu par MCI.                                                                                                     |
| MCIERR \_ fichier non valide \_            | Le fichier spécifié ne peut pas être lu sur l’appareil MCI spécifié. Le fichier est peut-être endommagé ou utilise un format de fichier incorrect.                               |
| \_paramètre manquant dans MCIERR \_       | La commande spécifiée requiert un paramètre, que vous devez fournir.                                                                                          |
| MCIERR \_ multiple                 | Des erreurs se sont produites sur plusieurs appareils. Spécifiez séparément chaque commande et chaque périphérique pour identifier les périphériques à l’origine des erreurs.                             |
| MCIERR \_ doit \_ utiliser \_ Shareable     | Le pilote de périphérique est déjà en cours d’utilisation. Vous devez spécifier le paramètre « partageable » avec chaque commande d’ouverture pour partager l’appareil.                                  |
| MCIERR \_ aucun \_ élément n’est \_ autorisé     | L’appareil spécifié n’utilise pas de nom de fichier.                                                                                                               |
| MCIERR \_ aucun \_ entier              | Le paramètre de cette commande MCI doit être une valeur entière.                                                                                                |
| MCIERR \_ aucune \_ fenêtre               | Il n’y a aucune fenêtre d’affichage.                                                                                                                                 |
| MCIERR \_ fonction INapplicable \_  | La séquence de commandes MCI spécifiée ne peut pas être exécutée dans l’ordre indiqué. Corriger la séquence de commandes ; Ensuite, réessayez.                                   |
| \_bloc de \_ paramètres \_ null MCIERR   | Un bloc de paramètres null (structure) a été passé à MCI.                                                                                                       |
| MCIERR \_ \_ de \_ mémoire insuffisante          | Votre système ne dispose pas de suffisamment de mémoire pour cette tâche. Quittez une ou plusieurs applications pour augmenter la mémoire disponible, puis réessayez d’effectuer la tâche. |
| MCIERR \_ OUTOFRANGE               | La valeur de paramètre spécifiée est hors limites pour la commande MCI spécifiée.                                                                                |
| MCIERR \_ définir le \_ CD                  | Le fichier ou l’appareil MCI spécifié est inaccessible car l’application ne peut pas changer de répertoire.                                                         |
| MCIERR \_ définir le \_ lecteur               | Le fichier ou l’appareil MCI spécifié est inaccessible car l’application ne peut pas modifier les lecteurs.                                                              |
| \_ressource sans nom MCIERR \_        | Vous ne pouvez pas stocker un fichier sans nom. Spécifiez un nom de fichier.                                                                                                       |
| \_commande MCIERR non reconnue \_    | Le pilote ne peut pas reconnaître la commande spécifiée.                                                                                                          |
| MCIERR \_ fonction non prise en charge \_    | Le pilote de périphérique MCI utilisé par le système ne prend pas en charge la commande spécifiée.                                                                           |



 

 

 