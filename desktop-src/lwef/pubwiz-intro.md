---
title: Présentation des assistants de publication
description: Windows XP présente l’Assistant Publication de sites Web et l’Assistant commande d’impression en ligne.
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- assistants de publication, à propos de
- Assistant Publication de sites Web, à propos de
- Assistant commande d’impression en ligne, à propos de
- assistants de publication, Assistant Publication de sites Web
- assistants de publication, Assistant commande d’impression en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b4e6d3c515edae23d0e74f550e000bdfdfacf03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118182"
---
# <a name="publishing-wizards-introduction"></a>Présentation des assistants de publication

Windows XP présente l’Assistant Publication de sites Web et l’Assistant commande d’impression en ligne. À partir du même Framework, ces assistants fournissent à l’utilisateur un mécanisme simple pour publier du contenu sur un site Web ou pour commander des impressions effectuées à partir de fichiers image numériques. L’avantage de ces assistants réside dans leur capacité à héberger du contenu HTML à partir de différents fournisseurs dans leurs pages d’Assistant afin que l’apparence, la procédure et les options utilisateur disponibles soient entièrement contrôlées par le fournisseur et qu’elles puissent être modifiées à tout moment sans affecter l’Assistant client qui les héberge. Bien que ces assistants existants aient été créés avec la création d’images numériques à l’esprit, l’infrastructure et les concepts peuvent être utilisés à de nombreuses fins, par exemple un service d’impression de documents ou une méthode de partage d’images avec des amis et de la famille.

-   [Comment cela fonctionne-t-il ?](#how-does-it-work)
-   [Documentation de l’Assistant Publication](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a>Comment cela fonctionne-t-il ?

L’expérience utilisateur de l’Assistant Publication de sites Web et de l’Assistant commande d’impression en ligne est similaire, mais le point d’entrée de chaque Assistant diffère. Pour l’Assistant Publication de sites Web, une tâche intitulée **publier ce dossier sur le Web** est disponible dans la liste **tâches de fichiers et de dossiers** à gauche de la plupart des affichages de dossiers. Le texte de la tâche varie selon le contenu sélectionné. Par exemple, si un fichier est sélectionné, la tâche lit **publier ce fichier sur le Web** comme indiqué dans l’exemple suivant.

![tâches de fichiers et de dossiers](images/shell-pubwiz-tasks.png)

L’utilisateur clique sur la tâche pour lancer l’Assistant. En cours dans l’Assistant, une liste de fournisseurs est présentée à l’utilisateur, comme illustré dans l’exemple suivant. Les fournisseurs de services Internet (ISP) peuvent développer et enregistrer leurs propres pages de fournisseur à afficher dans cette liste.

![Liste des fournisseurs de l’Assistant Publication](images/shell-pubwiz-provs.png)

Une fois qu’un fournisseur est choisi, l’Assistant se connecte à ce site et la première page HTML est téléchargée pour s’afficher dans l’Assistant. Si les utilisateurs ne disposent pas d’un compte avec le fournisseur sélectionné, ils ont la possibilité d’en définir un.

Plusieurs pages HTML sont contenues dans une seule page de l’Assistant. en d’autres termes, le descripteur de la page de l’Assistant hébergeant ce procession de pages HTML reste constant. Les pages HTML sont exposées dans le volet central comme avec n’importe quelle page standard de l’Assistant. Le site du fournisseur fournit des méthodes pour contrôler à quel moment les boutons précédent, **suivant** et **Annuler** de l’Assistant se **déplacent** alors que les pages HTML sont affichées. Au sein de ces pages HTML, les utilisateurs peuvent être invités à spécifier un dossier dans lequel ils peuvent copier des fichiers ou enregistrer le nom d’un site Web qu’ils souhaitent créer. Une fois que l’utilisateur a terminé toutes les étapes requises, le site appelle une méthode pour commencer le chargement, en retournant le contrôle à l’Assistant. L’Assistant lui-même gère le téléchargement et les graphiques de surveillance tels qu’un indicateur de progression. Une fois le téléchargement terminé, le site du fournisseur peut spécifier une URL où l’utilisateur peut accéder une fois l’Assistant fermé.

Dans l’Assistant commande d’impression en ligne, l’affichage **en ligne** de l’ordre des tâches s’affiche uniquement dans les dossiers d’images tels que mes images, comme dans l’exemple suivant. Toutefois, le processus est très similaire à l’Assistant Publication de sites Web. Le site du fournisseur invite les utilisateurs à fournir des options telles que la sélection d’images, les tailles d’impression, le nombre de copies et les informations de paiement.

![tâches de l’image](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a>Documentation de l’Assistant Publication

L’Assistant Publication de sites Web et l’Assistant commande d’impression en ligne sont présentés en détail dans les documents suivants. Vous trouverez également des instructions pour le développement d’applications qui doivent être hébergées par ces derniers.

-   [Conception côté client](pubwiz-client.md)
-   [Conception côté serveur](pubwiz-server.md)
-   [Inscription d’un service](pubwiz-reg.md)
-   [Utilisation du manifeste de transfert](pubwiz-manifest.md)
-   [Schéma de manifeste de transfert](/windows/desktop/shell/interfaces)

 

 