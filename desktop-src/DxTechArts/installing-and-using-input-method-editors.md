---
title: Installation et utilisation des éditeurs de méthode d’entrée
description: cet article propose un didacticiel sur l’installation et l’utilisation de l’éditeur de méthode d’entrée (IME) Windows standard.
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45a0da52d0e917186831de8c84f39ecee3d2583ac4a267fa2501c643e2f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153425"
---
# <a name="installing-and-using-input-method-editors"></a>Installation et utilisation des éditeurs de méthode d’entrée

cet article propose un didacticiel sur l’installation et l’utilisation de l’éditeur de méthode d’entrée (IME) Windows standard.

-   [Installation d’un éditeur de méthode d’entrée](#installing-an-input-method-editor)
-   [IME chinois simplifié](#simplified-chinese-ime)
-   [IME chinois traditionnel](#traditional-chinese-ime)
-   [IME japonais](#japanese-ime)
-   [IME coréen](#korean-ime)
-   [Requirements](#requirements)

## <a name="installing-an-input-method-editor"></a>Installation d’un éditeur de méthode d’entrée

Les sections suivantes décrivent comment installer et utiliser les éditeurs de méthode d’entrée (IME) pour entrer des caractères complexes dans quatre langues d’Asie orientale différentes. Les fonctionnalités propres à chaque langue sont présentées.

Pour implémenter les fonctionnalités de l’éditeur de méthode d’entrée (IME) dans une application, consultez [utilisation d’un éditeur de méthode d’entrée dans un jeu](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game).

par défaut, un IME n’est pas installé sur les systèmes Microsoft Windows XP. Pour installer, procédez comme suit.

**Pour installer un IME**

1.  Dans le panneau de configuration, ouvrez Options régionales et linguistiques.
2.  Dans l’onglet langues, activez la case à cocher installer les fichiers pour les langues d’Extrême-Orient.

    ![onglet langues des options régionales et linguistiques](images/ime-1.png)

    Une boîte de dialogue d’installation de la prise en charge de langue supplémentaire s’affiche pour vous informer des exigences de stockage pour les fichiers de langue.

    ![installer la prise en charge linguistique supplémentaire, boîte de dialogue](images/ime-install-lang-dialog.png)

3.  Cliquez sur OK pour fermer la boîte de dialogue.
4.  Cliquez sur OK sous l’onglet langues.
5.  une autre boîte de dialogue s’affiche pour demander un disque d’installation Windows XP ou un emplacement de partage réseau où se trouvent les fichiers de prise en charge linguistique. insérez un disque Windows XP compact ou accédez à l’emplacement réseau approprié, puis cliquez sur OK. Microsoft Windows installe les fichiers nécessaires et vous invite à redémarrer l’ordinateur.
6.  Cliquez sur Oui pour redémarrer l’ordinateur.
7.  Après le redémarrage, ouvrez une nouvelle fois les options régionales et linguistiques du panneau de configuration.
8.  Dans l’onglet langues, cliquez sur détails. La fenêtre services de texte et langues d’entrée s’affiche.

    ![services ext et fenêtre langues d’entrée](images/ime-2.png)

9.  sous l’onglet Paramètres, cliquez sur ajouter. La fenêtre Ajouter une langue d’entrée s’affiche.

    ![fenêtre Ajouter une langue d’entrée](images/ime-3.png)

10. Sélectionnez chinois (Taiwan) pour langue d’entrée et Microsoft New IME phonétique 2002a pour la disposition du clavier/IME.
11. Cliquez sur OK. Vous pouvez désormais ajouter des langages et des IME supplémentaires de la même manière.
12. Cliquez à nouveau sur Ajouter, sélectionnez chinois (RPC) pour langue d’entrée et chinois (simplifié)-Microsoft Pinyin IME 3,0 pour la disposition du clavier/IME, puis cliquez sur OK.
13. Cliquez à nouveau sur Ajouter, sélectionnez japonais pour la langue d’entrée et Microsoft IME standard 2002 ver. 8,1 pour la disposition de clavier/IME, puis cliquez sur OK.
14. Cliquez à nouveau sur Ajouter, sélectionnez coréen pour langue d’entrée et système d’entrée coréen (IME 2002) pour disposition du clavier/IME, puis cliquez sur OK. Dans la fenêtre services de texte et langues d’entrée, la zone de liste services installés doit maintenant contenir les quatre IME récemment ajoutés.

    ![zone de liste des services installés](images/ime-7.png)

15. Cliquez sur OK pour fermer la fenêtre services de texte et langues d’entrée.
16. Cliquez sur OK pour fermer le panneau de configuration Options régionales et linguistiques. la barre des tâches Windows doit maintenant contenir un indicateur de paramètres régionaux d’entrée entouré d’un cercle rouge. L’existence de l’indicateur signifie que plusieurs langues d’entrée ont été installées sur le système.

    ![indicateur qui signifie que plusieurs langues d’entrée ont été installées sur le système](images/ime-8.png)

## <a name="simplified-chinese-ime"></a>IME chinois simplifié

cette section explique comment utiliser l’IME (PinYin) simplifié avec Microsoft Bloc-notes pour entrer quelques caractères chinois.

1.  lancez Bloc-notes (disponible à partir du bouton démarrer, puis sélectionnez tous les programmes et accessoires). tapez des caractères dans Bloc-notes. Ces caractères vous aideront à visualiser la fenêtre IME plus tard.

    ![Capture qui affiche des caractères qui permettent de visualiser la fenêtre I M E plus tard pour le chinois simplifié.](images/ime-sc1.png)

2.  avec Bloc-notes comme application active, cliquez sur l’indicateur de paramètres régionaux d’entrée et sélectionnez chinois (rpc). L’affichage de l’indicateur devient CH pour indiquer que la nouvelle langue d’entrée est le chinois (RPC).

    ![Capture d’écran montrant l’indicateur de paramètres régionaux d’entrée pour sélectionner le chinois (P R C).](images/ime-sc2.png)

3.  placez le curseur dans Bloc-notes. Appuyez sur orig sur le clavier afin que le curseur se trouve au début de la ligne. Sur le type de clavier « N », puis « I ». L’illustration suivante montre l’apparence de l’affichage. Le petit rectangle horizontal est la fenêtre de lecture, qui affiche la chaîne de lecture actuelle. Actuellement, la chaîne de lecture est « ni » en raison de la saisie de « N » et « I ».

    ![Capture d’écran montrant une chaîne de lecture avec « n » et « i ».](images/ime-sc3.png)

4.  Tapez « 3 ». Bloc-notes a désormais l’affichage suivant. Étant donné que N + I + 3 est une prononciation complète en pinyin chinois simplifié, l’IME dispose de suffisamment d’informations pour anticiper le caractère que l’utilisateur peut avoir prévu d’entrer. La fenêtre de lecture disparaît, car vous avez entré une prononciation complète. un caractère est affiché en haut du curseur Bloc-notes. ce caractère ne fait pas partie de Bloc-notes, mais il est affiché dans une autre fenêtre en plus de Bloc-notes et masque les caractères existants dans Bloc-notes qui se trouvent sous. Cette nouvelle fenêtre est appelée la fenêtre de composition, et la chaîne qu’elle contient est appelée chaîne de composition. La chaîne de composition est soulignée dans l’affichage.

    ![Capture d’écran montrant une fenêtre de composition avec une chaîne de composition d’un caractère.](images/ime-sc4.png)

5.  Tapez maintenant "H", "A", "O", "3" pour entrer un autre caractère. Notez que la fenêtre de lecture s’affiche lorsque « H » est tapé et disparaît lorsque « 3 » est tapé. Comme indiqué ci-dessous, la chaîne de composition contient maintenant deux caractères.

    ![Capture d’écran montrant une fenêtre de composition avec une chaîne de composition de deux caractères.](images/ime-sc5.png)

6.  Appuyez une fois sur la flèche gauche du clavier. Le curseur de composition déplace un caractère vers la gauche, au deuxième caractère que vous avez tapé. une fenêtre s’affiche au-dessus de Bloc-notes comme indiqué ci-dessous. Cette fenêtre s’appelle la fenêtre candidate. Elle affiche une liste de caractères ou d’expressions qui correspondent à la prononciation que vous avez tapée. Vous pouvez sélectionner le mot souhaité parmi les entrées de la liste candidat. Dans cet exemple, deux caractères candidats sont disponibles avec la même prononciation.

    ![deux caractères candidats disponibles avec la même prononciation](images/ime-sc6.png)

7.  Tapez « 2 » pour sélectionner la deuxième entrée. La fenêtre candidate se ferme maintenant, et la chaîne de composition est mise à jour avec le caractère sélectionné.

    ![Capture d’écran montrant une chaîne de composition mise à jour avec le caractère sélectionné.](images/ime-sc7.png)

8.  Appuyez sur Entrée. cela indique à l’IME que la composition est terminée et la chaîne doit être envoyée à l’application-Bloc-notes dans cet exemple. la fenêtre de composition se ferme et les deux caractères sont envoyés à Bloc-notes via WM \_ CHAR. le soulignement est passé dans la figure suivante, car les deux caractères indiqués font partie du texte de Bloc-notes. le texte existant « ABCDEFG » dans Bloc-notes est déplacé vers la droite, car deux caractères supplémentaires ont été insérés. Vous avez maintenant entré avec succès deux caractères en chinois simplifié à l’aide d’un IME.

    ![deux caractères chinois simplifiés sont entrés avec succès à l’aide d’un IME](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a>IME chinois traditionnel

cette section explique comment utiliser l’éditeur IME chinois traditionnel (nouveau phonétique) avec Bloc-notes pour entrer quelques caractères chinois.

1.  Lancez le Bloc-notes. tapez des caractères dans Bloc-notes. Ces caractères vous aideront à visualiser la fenêtre IME plus tard.

    ![Capture d’écran montrant des caractères permettant de visualiser la fenêtre I M E plus tard pour le chinois traditionnel.](images/ime-tc1.png)

2.  cliquez sur l’indicateur paramètres régionaux d’entrée dans la barre des tâches Windows, puis sélectionnez chinois (taïwan). L’affichage de l’indicateur devient CH pour indiquer que la nouvelle langue d’entrée est le chinois (Taïwan).

    ![indicateur de paramètres régionaux d’entrée pour sélectionner le chinois (Taïwan)](images/ime-tc2.png)

3.  placez le curseur dans Bloc-notes. Appuyez sur orig sur le clavier afin que le curseur se trouve au début de la ligne. Sur le type de clavier « S », puis sur « U ». L’illustration suivante montre l’apparence de l’affichage. Le petit rectangle vertical est la fenêtre de lecture, qui affiche la chaîne de lecture actuelle. Comme indiqué dans l’illustration suivante, la chaîne de lecture comporte deux caractères suite à la saisie de « S » et de « U ».

    ![Capture d’écran montrant une chaîne de lecture avec deux caractères.](images/ime-tc3.png)

4.  Tapez « 3 ». Bloc-notes a désormais l’affichage suivant. Étant donné que S + U + 3 est une prononciation complète en chinois traditionnel, l’IME dispose de suffisamment d’informations pour anticiper le caractère que l’utilisateur peut avoir prévu d’entrer. La fenêtre de lecture disparaît, car vous avez entré une prononciation complète. un caractère est affiché en haut du curseur Bloc-notes. ce caractère ne fait pas partie de Bloc-notes, mais il est affiché dans une autre fenêtre en plus de Bloc-notes et masque les caractères existants dans Bloc-notes qui se trouvent sous. Cette nouvelle fenêtre est appelée la fenêtre de composition, et la chaîne qu’elle contient est appelée chaîne de composition. La chaîne de composition est soulignée dans l’affichage.

    ![Capture d’écran montrant une fenêtre de composition avec une chaîne de composition soulignée.](images/ime-tc4.png)

5.  Tapez maintenant « C », « L » et « 3 » pour entrer un autre caractère. Notez que la fenêtre de lecture s’affiche lorsque « C » est tapé et disparaît lorsque « 3 » est tapé. Comme indiqué ci-dessous, la chaîne de composition contient maintenant deux caractères.

    ![Capture d’écran montrant une fenêtre de composition avec une chaîne de composition et deux caractères soulignés.](images/ime-tc5.png)

6.  Tapez la flèche vers le bas sur le clavier une fois. une fenêtre s’affiche au-dessus de Bloc-notes comme indiqué ci-dessous. Cette fenêtre s’appelle la fenêtre candidate. Elle affiche une liste de caractères ou d’expressions qui correspondent à la prononciation que vous avez tapée. Vous pouvez sélectionner le mot souhaité parmi les entrées de la liste candidat. Dans cet exemple, trois caractères candidats sont disponibles avec la même prononciation.

    ![trois caractères candidats disponibles avec la même prononciation](images/ime-tc6.png)

7.  Tapez « 2 » pour sélectionner la deuxième entrée. La fenêtre candidate se ferme maintenant, et la chaîne de composition est mise à jour avec le caractère sélectionné.

    ![Capture d’écran montrant une chaîne de composition mise à jour avec un caractère sélectionné.](images/ime-tc7.png)

8.  Appuyez sur Entrée. cela indique à l’IME que la composition est terminée et la chaîne doit être envoyée à l’application-Bloc-notes dans cet exemple. la fenêtre de composition se ferme et les deux caractères sont envoyés à Bloc-notes via [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char). le soulignement est passé dans la figure suivante, car les deux caractères indiqués font partie du texte de Bloc-notes. le texte existant « ABCDEFG » dans Bloc-notes est déplacé vers la droite, car deux caractères supplémentaires ont été insérés. Vous avez maintenant entré avec succès deux caractères en chinois traditionnel à l’aide d’un IME.

    ![deux caractères chinois traditionnel ont été entrés à l’aide d’un IME](images/ime-tc8.png)

## <a name="japanese-ime"></a>IME japonais

cette section est une procédure pas à pas d’utilisation de l’IME japonais avec Bloc-notes pour entrer quelques caractères japonais.

1.  Lancez le Bloc-notes. tapez des caractères dans Bloc-notes. Ces caractères vous aideront à visualiser la fenêtre IME plus tard.

    ![Capture d’écran montrant les caractères qui permettent de visualiser la fenêtre I M E plus tard pour le japonais.](images/ime-j1.png)

2.  avec Bloc-notes comme application active, cliquez sur l’indicateur de paramètres régionaux d’entrée, puis sélectionnez japonais. L’indicateur affiche la modification de JP pour refléter le fait que la nouvelle langue d’entrée est le japonais.

    ![indicateur de paramètres régionaux d’entrée pour sélectionner le japonais](images/ime-j2.png)

3.  placez le curseur dans Bloc-notes. Appuyez sur orig sur le clavier afin que le curseur se trouve au début de la ligne. Sur le type de clavier « N », puis « I ». L’illustration suivante montre l’apparence de l’affichage. Étant donné que N + I est une prononciation complète en japonais, l’IME dispose de suffisamment d’informations pour anticiper le caractère que l’utilisateur peut avoir prévu d’entrer. un caractère est affiché en haut du curseur Bloc-notes. ce caractère ne fait pas partie de Bloc-notes, mais il est affiché dans une autre fenêtre en plus de Bloc-notes et masque les caractères existants dans Bloc-notes qui se trouvent sous. Cette nouvelle fenêtre est appelée la fenêtre de composition, et la chaîne qu’elle contient est appelée chaîne de composition. La chaîne de composition est soulignée dans l’affichage.

    ![Capture d’écran montrant une chaîne de composition avec un caractère japonais souligné.](images/ime-j3.png)

4.  À présent, tapez « H », « O », « N », « G » et « O » pour entrer deux autres caractères. La chaîne de composition contient maintenant quatre caractères, comme indiqué ci-dessous.

    ![Capture d’écran montrant une chaîne de composition avec quatre caractères japonais soulignés.](images/ime-j4.png)

5.  Appuyez sur la barre d’espace. Cela indique à l’IME de convertir le texte entré en clauses. Dans la figure ci-dessous, l’IME convertit la prononciation « Nihongo » en une clause écrite en kanji qui signifie « langue japonaise ».

    ![IME convertit la prononciation japonaise](images/ime-j5.png)

6.  Appuyez une fois sur la flèche bas du clavier. une fenêtre s’affiche au-dessus de Bloc-notes comme indiqué ci-dessous. Cette fenêtre s’appelle la fenêtre candidate. Elle affiche une liste de clauses qui correspondent à la prononciation que vous avez tapée. Vous pouvez sélectionner le mot prévu dans la liste des candidats. Dans cet exemple, trois caractères candidats sont disponibles avec la même prononciation. Notez que la deuxième entrée est mise en surbrillance et que la chaîne de composition change. Cela est dû à la saisie d’une flèche orientée vers le bas, qui indique à l’IME de sélectionner l’entrée après celle qui a été précédemment affichée.

    ![Capture d’écran montrant la fenêtre candidate.](images/ime-j6.png)

7.  Tapez « 2 » pour sélectionner la deuxième entrée. La fenêtre candidate se ferme maintenant, et la chaîne de composition est mise à jour avec le caractère sélectionné.

    ![Capture d’écran montrant la chaîne de composition mise à jour avec le caractère japonais sélectionné.](images/ime-j7.png)

8.  Appuyez sur Entrée. cela indique à l’IME que la composition est terminée et la chaîne doit être envoyée à l’application-Bloc-notes dans cet exemple. la fenêtre de composition se ferme et les deux caractères sont envoyés à Bloc-notes via [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char). le soulignement est passé dans la figure suivante, car les deux caractères indiqués font partie du texte de Bloc-notes. le texte existant « ABCDEFG » dans Bloc-notes est déplacé vers la droite, car deux caractères supplémentaires ont été insérés. Vous avez maintenant entré avec succès quelques caractères japonais à l’aide d’un IME.

    ![saisie réussie de quelques caractères japonais à l’aide d’un IME](images/ime-j8.png)

## <a name="korean-ime"></a>IME coréen

cette section décrit comment utiliser l’éditeur IME coréen avec Bloc-notes pour entrer quelques caractères coréens.

1.  Lancez le Bloc-notes. tapez des caractères dans Bloc-notes. Ces caractères vous aideront à visualiser la fenêtre IME plus tard.

    ![caractères qui permettent de visualiser la fenêtre IME plus tard](images/ime-k1.png)

2.  avec Bloc-notes comme application active, cliquez sur l’indicateur de paramètres régionaux d’entrée, puis sélectionnez coréen. L’affichage de l’indicateur devient KO pour indiquer que la nouvelle langue d’entrée est le coréen.

    ![indicateur de paramètres régionaux d’entrée pour sélectionner le coréen](images/ime-k2.png)

3.  placez le curseur dans Bloc-notes. Appuyez sur orig sur le clavier pour que le curseur se trouve au début de la ligne, puis tapez « G ». L’illustration suivante montre l’apparence de l’affichage. l’élément phonetic correspondant à « G » s’affiche sur Bloc-notes et est mis en surbrillance avec un curseur de bloc. Ce caractère en surbrillance est appelé la chaîne de composition. notez que contrairement à l’IME pour d’autres langages, la chaîne de composition est envoyée à Bloc-notes et insérée à gauche du texte existant dès que l’utilisateur entre un seul élément phonétique.

    ![Capture d’écran montrant une chaîne de composition avec un caractère inséré à gauche du texte existant.](images/ime-k3.png)

4.  À ce stade, la chaîne de composition se compose d’un caractère intermédiaire, car tous les éléments phonétiques supplémentaires entrés par l’utilisateur modifient la chaîne de composition sur place. À présent, tapez « K », puis « S ». Notez que le caractère intermédiaire change avec chaque séquence de touches.

    ![chaîne de composition](images/ime-k4.png)

5.  Appuyez maintenant sur la touche CTRL de droite. Une fenêtre candidate s’affiche et répertorie les caractères hanja que vous pouvez sélectionner pour la prononciation entrée, G + K + S.

    ![Capture d’écran montrant une fenêtre candidate avec une liste de caractères hanja que vous pouvez sélectionner en bas de la fenêtre.](images/ime-k5.png)

6.  Tapez le chiffre « 1 » pour sélectionner la première entrée de la liste. La fenêtre candidate se ferme et la chaîne de composition est mise à jour avec le caractère sélectionné.

    ![chaîne de composition mise à jour avec le caractère sélectionné](images/ime-k6.png)

7.  Tapez « R », « N » et « R ». Appuyez ensuite sur la touche CTRL de droite pour entrer un autre caractère.

    ![fenêtre candidate](images/ime-k7.png)

8.  Tapez « 1 » pour sélectionner la première entrée. Vous avez maintenant entré avec succès deux caractères coréens à l’aide d’un IME. les caractères coréens font déjà partie de la chaîne de texte dans Bloc-notes.

    ![deux caractères coréens ont été entrés à l’aide d’un IME](images/ime-k8.png)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Système d’exploitation**                | Windows XP                                                                                                 |
| **Espace disque disponible**       | Au moins 230 Mo                                                                                            |
| **Emplacements des fichiers de langue étrangère** | Windows installation xp disque compact ou emplacement réseau avec les fichiers d’installation Windows XP                |
| **Time**                            | Environ dix minutes pour installer les fichiers de langue étrangère ; environ dix minutes, chacune d’entre elles examine quatre IME différents. |



 

 

 
