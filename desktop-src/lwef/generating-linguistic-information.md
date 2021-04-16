---
title: Génération d’informations linguistiques
description: Génération d’informations linguistiques
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23fb99a5139e287e07e353791ce776b8a04dd8d2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104567070"
---
# <a name="generating-linguistic-information"></a>Génération d’informations linguistiques

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Une fois que vous avez enregistré un nouveau fichier audio ou que vous avez chargé un fichier audio existant, vous pouvez générer des informations de phonétique et de césure en entrant du texte qui correspond à votre fichier audio dans la zone de **représentation de texte** . Choisissez ensuite la commande **générer des informations linguistiques** dans le menu **Edition** ou dans la barre d’outils. L’éditeur Sound affiche un message de progression et commence le traitement de votre fichier audio. Lorsqu’il a terminé de générer des informations linguistiques, il affiche un mappage des étiquettes Word et phonème pour le fichier audio dans des zones de la zone **représentation audio** . Notez que la commande **generate linguistique info** reste désactivée jusqu’à ce que vous entriez une représentation textuelle de votre fichier audio.

![Capture d’écran qui montre les volets « représentation textuelle » et « représentation audio » dans l’outil d’édition de sons de l’information linguistique Microsoft.](images/f3listlabel.gif)

Si l’éditeur ne produit pas un ensemble acceptable d’étiquettes Word ou phonème, choisissez à nouveau la commande **generate linguistique info** . Si l’éditeur ne génère pas d’informations linguistiques, vérifiez votre représentation textuelle pour vous assurer que tous les mots sont correctement triés et épelés, et que vous n’avez pas d’espaces superflus autour de la ponctuation. Ensuite, choisissez à nouveau la commande **générer les informations linguistiques** . Vous pouvez modifier la représentation textuelle en sélectionnant du texte dans la zone de texte **représentation textuelle** et en utilisant les commandes **couper**, **copier** et **coller** du menu **Edition** . Si vous n’êtes pas certain des mots inclus dans le fichier audio, vous pouvez lire le fichier audio en choisissant **lire** dans le menu **Edition** ou la barre d’outils de l’éditeur. Si l’éditeur ne parvient toujours pas à produire des étiquettes linguistiques, essayez à nouveau d’enregistrer votre fichier audio. Un enregistrement de qualité médiocre, surtout avec un bruit de fond excessif, est susceptible de réduire la probabilité de générer des informations linguistiques raisonnables.

Vous pouvez également créer manuellement vos propres informations linguistiques en sélectionnant une partie de la représentation audio et en choisissant **Insérer phonème** ou **Insérer un mot** dans le menu **Edition** . Ces commandes sont également disponibles si vous cliquez avec le bouton droit dans la sélection.

Pour voir comment les informations linguistiques peuvent être utilisées pour l’animation des caractères de synchronisation LIP avec Microsoft Agent, choisissez le bouton **lecture** dans la barre d’outils et l’éditeur lira votre fichier audio, en animant une image de la bouche en fonction des informations d’étiquette générées.

Vous pouvez modifier l’affichage des étiquettes de phonème pour afficher les attributions de l’alphabet de la loi internationale, en choisissant la commande d' **affichage des étiquettes de phonème** dans le menu **Edition** , puis la commande loi. Cela affiche la valeur d’octet pour le phonème. Pour revenir aux noms descriptifs, choisissez à nouveau la commande d' **affichage des étiquettes de phonème** , puis choisissez **nom**.

### <a name="playing-a-sound-file"></a>Exécution d’un fichier audio

Vous pouvez lire des fichiers audio Windows standard ou des fichiers audio linguistiquement améliorés en choisissant la commande **lire** dans le menu **audio** ou dans la barre d’outils de l’éditeur. Les commandes **suspendre** et **arrêter** vous permettent de suspendre ou d’arrêter la diffusion du fichier son. À mesure que vous lisez le fichier, l’exemple d’image de bouche s’anime pour montrer comment les informations de synchronisation de lèvre peuvent être utilisées par un caractère Microsoft Agent.

Vous pouvez également lire une partie sélectionnée d’un fichier son en faisant glisser une sélection dans la **représentation audio** ou en cliquant sur une étiquette de mot ou de phonème, puis en choisissant **lire**. Vous pouvez étendre une sélection existante en appuyant sur Maj et en cliquant, ou en appuyant sur Maj et en faisant glisser vers le nouvel emplacement dans la **représentation audio**.

### <a name="editing-linguistic-information"></a>Modification des informations linguistiques

Vous pouvez modifier les informations linguistiques d’un fichier de plusieurs façons. Par exemple, vous pouvez ajuster la limite d’un mot ou d’un contrôle de phonème en déplaçant le pointeur vers le bord de la zone qui définit la plage de l’étiquette. Lorsque le pointeur se transforme en pointeur de déplacement de la limite, faites glisser vers la gauche ou vers la droite. L’éditeur ajuste automatiquement la limite de mot ou de phonème adjacent.

![Capture d’écran qui montre les modifications apportées aux informations linguistiques d’un fichier.](images/f4listadj.gif)

L’ajustement de la limite d’une étiquette de phonème modifie le minutage d’un phonème lors de la lecture de l’audio. Pour les caractères développés pour une utilisation avec Microsoft Agent, la modification de la limite de l’étiquette de phonème peut modifier le minutage ou la durée d’une image de bouche mappée sur ce phonème. La modification de la limite d’une étiquette de mot modifie le minutage de l’apparence du mot dans la bulle de texte du caractère.

Vous pouvez également remplacer une assignation de phonème en sélectionnant l’étiquette de phonème et en sélectionnant **remplacer phonème** dans le menu **Edition** , ou en cliquant avec le bouton droit sur l’étiquette de phonème et en choisissant **remplacer phonème** dans le menu contextuel. L’éditeur affiche la boîte de dialogue **remplacer phonème** et met en surbrillance l’attribution de phonème actuelle de l’étiquette. Vous pouvez choisir un phonème de remplacement en le sélectionnant **dans la liste de la liste** de tarifs ou en choisissant une autre entrée dans la liste **nom** . Si plusieurs traductions de la Loi d’informations sont disponibles pour ce nom, choisissez un élément dans la **liste de disponibilité** . Pour entrer une désignation de la Loi d’un phonème qui ne peut pas être directement incluse dans la langue, tapez sa valeur hexadécimale ou plusieurs valeurs hexadécimales, concaténées avec un caractère plus (+). Une fois que vous avez sélectionné les informations de phonème de remplacement, choisissez **OK**, et l’éditeur remplace l’étiquette de phonème que vous avez sélectionnée.

![Capture d’écran montrant la boîte de dialogue « Replace phonème », avec « <SIL> » sélectionné comme étiquette descriptive.](images/f5listphone.gif)

De même, vous pouvez remplacer une étiquette de mot en cliquant sur la zone de l’étiquette et en choisissant **remplacer le mot**, ou en cliquant avec le bouton droit sur la zone de l’étiquette et en choisissant **remplacer Word** dans le menu contextuel. L’éditeur affiche la boîte de dialogue **remplacer le mot** . Entrez le mot de remplacement, puis choisissez **OK**.

![Capture d’écran montrant la boîte de dialogue « remplacer le mot » par « son » entré dans la zone de texte « texte du mot ».](images/f6listrep.gif)

Pour les caractères développés pour une utilisation avec Microsoft Agent, le remplacement d’une étiquette de phonème peut modifier l’image de bouche affichée lorsque le fichier audio est lu. Le remplacement d’un mot remplace le texte qui apparaît dans la bulle de texte du caractère lorsque la méthode [**Speak**](speak-method.md) est appelée.

Vous pouvez également insérer une nouvelle étiquette ou un nouveau mot de phonème en effectuant une sélection dans la **représentation audio** et en choisissant **Insérer phonème** ou **Insérer un mot** dans le menu **Edition** , ou en cliquant avec le bouton droit dans la sélection et en choisissant les commandes dans le menu contextuel. Ces commandes affichent des boîtes de dialogue similaires aux boîtes de dialogue **remplacer l’phonème** et **remplacer le mot** , sauf que l’éditeur insère le nouveau mot ou le phonème plutôt que de remplacer les informations existantes.

Enfin, vous pouvez supprimer un phonème ou un mot en sélectionnant son étiquette et en choisissant **supprimer phonème** ou **supprimer le mot**. Cela supprime les informations linguistiques du fichier.

 

 




