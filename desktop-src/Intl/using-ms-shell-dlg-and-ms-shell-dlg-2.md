---
description: Utilisation de MS Shell Dlg et MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: Utilisation de MS Shell Dlg et MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad43f972e776151551fa312ce2bd8ed6d19be58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224017"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>Utilisation de MS Shell Dlg et MS Shell Dlg 2

Windows est disponible dans les versions localisées de plusieurs langues. Toutefois, l’édition en langue anglaise peut également être utilisée pour exécuter des applications écrites dans des langages autres que l’anglais. Cela est vrai même lorsque le script utilisé pour ces langages est différent, comme lorsque les applications sont écrites en grec ou en japonais. ces applications requièrent une interface utilisateur avec des boîtes de dialogue, des icônes et des utilitaires qui fournissent des informations dans la langue de l’application, qui peuvent être différentes de la langue utilisée dans l’interface utilisateur actuelle Windows.

Le problème de sélection de la police d’une interface utilisateur est évident. par exemple, la police de l’interpréteur de commandes, également appelée police système ou par défaut, pour l’anglais (États-Unis) Windows 98 est ms sans serif, tandis que la police de l’interpréteur de commandes pour le grec (grèce) Windows 98 est ms sans serif grec. pour le japonais (japon) Windows 98, la police de l’interpréteur de commandes est MS UI Gothic. Ces jeux de caractères ne peuvent pas être mappés directement entre eux. Remplacement de MS sans serif par MS sans serif grec lorsque les paramètres régionaux sont définis sur grec (Grèce), ne permet pas aux applications existantes de s’exécuter de manière adéquate ou d’afficher des caractères grecs dans les menus système, les boîtes de dialogue et les contrôles d’édition.

Windows résout ce problème en utilisant les polices logiques ms shell dlg et ms shell dlg 2 pour permettre la sélection de la police appropriée pour l’affichage du script. cette section aborde plusieurs considérations relatives à la programmation pour l’utilisation des polices logiques afin d’implémenter des boîtes de dialogue, des menus et d’autres éléments similaires pour les interfaces utilisateur flexibles qui s’affichent correctement sur tous les systèmes d’exploitation Windows pris en charge et dans toutes les langues. Pour plus d’informations, consultez [création et sélection de polices](../gdi/font-creation-and-selection.md). pour plus d’informations sur l’utilisation de la technologie de interface utilisateur multilingue (MUI) dans création d’interfaces utilisateur pour vos applications multilingues, consultez également [interface utilisateur multilingue](multilingual-user-interface.md) .

## <a name="about-the-logical-fonts"></a>À propos des polices logiques

les polices logiques ms shell dlg et ms shell dlg 2 sont essentiellement des noms de police utilisés pour le mappage afin d’activer la prise en charge des paramètres régionaux/cultures dont les caractères ne sont pas contenus dans la page de codes 1252, le jeu de caractères Windows pour les États-Unis et l’europe occidentale. MS Shell Dlg correspond à la police de Shell par défaut associée à la culture/aux paramètres régionaux actuels et prend en charge l’apparence du bureau Windows classique. le nom de la police MS Shell Dlg 2 a été introduit dans Windows 2000 pour prendre en charge l’apparence introduite avec Windows 2000.

Par exemple, si votre application utilise MS Shell Dlg ou MS Shell Dlg 2 pour ses boîtes de dialogue, une équipe de localisation qui crée des ressources en langue grecque pour votre application peut se concentrer sur la traduction du texte. Ils n’ont pas à se préoccuper des problèmes tels que la distinction entre MS sans serif et MS sans serif grec.

> [!Note]  
> les polices générées par ms shell dlg et ms shell dlg 2 sont différentes selon les versions de Windows. Par conséquent, vous devez vous assurer que les éléments de l’interface utilisateur s’affichent correctement sur toutes les plateformes.

 

## <a name="handle-hard-coded-font-names"></a>Gérer les noms de police Hard-Coded

L’utilisation d’Unicode permet aux applications de gérer des milliers de caractères différents, mais la plupart des polices ne couvrent pas tous les jeux de caractères Unicode. Vos applications ne doivent pas coder en dur des noms de police. L’une des raisons est que le codage en dur d’un nom de police qui affiche des caractères pour une langue et non des caractères pour une autre langue entraîne l’affichage incorrect de l’ensemble du texte localisé dans la deuxième langue. Une autre raison pour ne pas coder en dur les noms de police est que la police souhaitée ne peut pas être chargée sur le système d’exploitation qui affiche le texte de l’application.

La meilleure façon de traiter les noms de polices consiste à les considérer comme des ressources localisables. l’utilisation d’une police logique résout le problème lié à l’exécution de votre interface à l’aide de n’importe quel langage sur Windows NT ou Windows 2000, quelle que soit la langue utilisée. Si vous définissez un nom de police comme ressource localisable, votre localisateur peut modifier la police de l’interface utilisateur localisée.

## <a name="handle-hard-coded-font-sizes"></a>Gérer les tailles de police Hard-Coded

Certains scripts sont complexes et nécessitent un grand nombre de pixels pour s’afficher correctement. Par exemple, la plupart des caractères anglais s’affichent sur une grille 5x7, mais les caractères japonais nécessitent au moins une grille 16x16 pour être clairement visibles. Alors que le chinois a besoin d’une grille 24x24, le thaï a uniquement besoin de 8 pixels pour la largeur, mais au moins 22 pixels pour la hauteur. Il est facile de comprendre que certains caractères peuvent ne pas être lisibles à une petite taille de police.

L’interface utilisateur de votre application doit traiter les tailles de police comme des ressources localisables. l’utilisation d’une police logique résout le problème lié à l’exécution de votre interface à l’aide de n’importe quel langage sur Windows NT ou Windows 2000, quelle que soit la langue utilisée. La définition d’une taille de police comme ressource localisable permet à votre localisateur de modifier la police de l’interface utilisateur localisée.

## <a name="map-the-logical-fonts"></a>Mapper les polices logiques

Chacune des polices logiques est mappée par une entrée dans le registre à la police de Shell appropriée pour les paramètres régionaux actifs. lorsque l’une des polices logiques est utilisée, Windows bascule vers la police pour les paramètres régionaux actuellement sélectionnés au moment de l’exécution. cette opération permet d’afficher correctement l’interface utilisateur de l’anglais (États-Unis) Windows, ainsi que les caractères qui ne sont pas dans la page de codes 1252. par conséquent, l’expédition des applications localisées peut s’exécuter sur la version anglaise (États-Unis) de Windows sans modification.

chaque Windows ordinateur mappe ms shell dlg et ms shell dlg 2 à une police physique appropriée, en fonction de la langue définie pour les programmes non-Unicode, décrite dans [terminologie NLS](nls-terminology.md). les mappages réels sont stockés dans la clé de registre HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ Current Version \\ FontSubstitutes.

### <a name="font-mapping-on-windows-me9895"></a>mappage des polices sur Windows Me/98/95

MS Shell Dlg correspond généralement à une version propre à la page de codes de MS sans serif.

### <a name="font-mapping-on-windows-nt-40"></a>Mappage des polices sur Windows NT 4,0

MS Shell Dlg est mappé à MS sans serif pour les langues occidentales et de l’Europe centrale, grec, turc, balte et langues à l’aide d’un script cyrillique. MS UI Gothic pour le japonais ; Gulim pour le coréen ; SimSun pour le chinois simplifié ; PMinglu pour le chinois traditionnel ; suite.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>mappage des polices sur Windows 2000, Windows XP, Windows Server 2003, Windows Vista et Windows 7

Les deux polices logiques sont mappées à des polices TrueType Unicode. MS Shell Dlg utilise Microsoft sans serif (distinct de MS sans serif) si la langue d’installation n’est pas japonaise. MS Shell Dlg est mappé à MS UI Gothic si la langue d’installation est le japonais.

sur les systèmes MUI Windows XP, ms Shell Dlg est mappé à ms UI Gothic uniquement lorsque les paramètres régionaux système et la langue de l’interface utilisateur sont définis sur le japonais. Dans le cas contraire, MS Shell Dlg est mappé à Microsoft sans serif.

sur Windows Vista et Windows 7, ms Shell Dlg est mappé à ms UI Gothic si la langue de l’interface utilisateur par défaut de l’ordinateur est définie sur le japonais (quelle que soit la langue de l’installation). MS Shell Dlg est mappé à Microsoft sans serif si la langue de l’interface utilisateur par défaut de l’ordinateur est définie sur une langue autre que le japonais.

MS Shell Dlg 2 utilise simplement la police Tahoma, quelle que soit la langue. Le principal avantage de Tahoma sur Microsoft sans serif est que Tahoma a un visage de police gras natif. Son principal inconvénient est qu’il est possible que les systèmes d’exploitation plus anciens ne soient pas installés et qu’ils remplacent une police moins attrayante.

les caractères qui ne sont pas implémentés dans Tahoma ou Microsoft Sans Serif peuvent être implémentés dans d’autres Windows polices utilisées pour l’affichage de texte dans les interfaces utilisateur. Selon les contrôles ou les API utilisés pour afficher du texte, plusieurs mécanismes tels que la [liaison de polices](https://msdn.microsoft.com/globalization/mt662331) peuvent être utilisés par le système pour sélectionner automatiquement ces polices afin d’afficher ces caractères.

Les applications peuvent utiliser Microsoft sans serif ou Tahoma de manière explicite, et enregistrer le niveau d’indirection impliqué dans l’utilisation de MS Shell Dlg ou MS Shell Dlg 2. En raison de la liaison de polices, la spécification de Microsoft sans serif ou Tahoma fournit des glyphes appropriés pour tous les langages.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>utiliser MS Shell Dlg pour une Application Non anglaise sur Windows Me/98/95

sur Windows Me/98/95, MS Shell Dlg n’est pas destiné à être utilisé avec une application d’interface utilisateur statique et non anglaise qui s’exécute lorsque l’utilisateur a choisi des paramètres régionaux avec un autre jeu de caractères de base de Windows. Dans ce cas, la langue de l’interface utilisateur de l’application peut ne pas être prise en charge avec la police substituée à MS Shell Dlg.

par exemple, si l’utilisateur utilise une version en allemand de Windows et souhaite installer une application non-Unicode grec, l’utilisateur tente de modifier les paramètres régionaux en grec (grèce). Cette action réinitialise MS Shell Dlg à une police grecque, mais cette police ne contient pas tous les glyphes nécessaires à l’affichage en allemand. Par conséquent, les caractères non-ASCII de l’interface utilisateur en allemand ne s’afficheront pas correctement. Pour prendre en charge ce scénario, une application doit définir MS Shell Dlg sur une police qui contient à la fois les glyphes de l’Europe occidentale et du grec.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération et sélection des polices internationales](using-international-fonts-and-text.md)
</dt> <dt>

[Interface utilisateur multilingue](multilingual-user-interface.md)
</dt> </dl>

 

 
