---
description: dans chaque version majeure de Windows, des polices sont ajoutées pour prendre en charge les langues et les scripts internationaux.
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: Énumération et sélection des polices internationales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b28e2dca3937f3513a930f157a364d466f761ed54a53d09c3e2b8b1c89bb30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146882"
---
# <a name="international-font-enumeration-and-selection"></a>Énumération et sélection des polices internationales

dans chaque version majeure de Windows, des polices sont ajoutées pour prendre en charge les langues et les scripts internationaux. pour plus d’informations sur la [prise en charge des scripts et des polices dans Windows](https://msdn.microsoft.com/globalization/mt791278) , consultez les polices ajoutées dans chaque version Windows depuis Windows 2000, ainsi que les scripts, les régions et les langues pris en charge.

## <a name="enumfontfamiliesex"></a>EnumFontFamiliesEx

Pour énumérer les polices internationales dans votre application, vous pouvez utiliser la fonction [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) . **EnumFontFamiliesEx** vous permet d’énumérer des polices en fonction du nom de la police et du jeu de caractères en passant un pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qui contient le nom de la police et les informations du jeu de caractères. Pour appeler **EnumFontFamiliesEx**, vous pouvez spécifier un nom de police ou un jeu de caractères, ou vous pouvez demander ce qui est disponible. La définition du nom de police de **LOGFONT** sur **null** permet d’énumérer tous les noms de police. La définition du champ charset **sur \_ charset par défaut** énumère tous les jeux de caractères.

Notez que les jeux de caractères sont une notion héritée correspondant aux jeux de caractères pré-Unicode. À l’heure actuelle, il n’existe aucun mécanisme pour énumérer les polices prenant en charge les scripts arbitraires ou les plages de caractères en Unicode. La structure [**NEWTEXTMETRICEX**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa) transmise par [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85)) comprend la structure [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) , qui comprend des déclarations plus détaillées fournies par le développeur de polices en ce qui concerne les pages de codes et les plages Unicode prises en charge par la police. Pour déterminer plus précisément les plages de caractères prises en charge par une police donnée, sélectionnez la police dans un contexte de périphérique et appelez [**GetFontUnicodeRanges**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges). Notez que cette API ne prend pas en charge les plans supplémentaires Unicode.

## <a name="choosefont"></a>ChooseFont

Vous pouvez utiliser la fonction [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) pour afficher une boîte de dialogue commune qui permet à l’utilisateur de sélectionner des polices internationales basées sur CharSet. Vous pouvez spécifier l’un des trois indicateurs pour déterminer, en fonction du jeu de caractères, les polices qui sont affichées dans la boîte de dialogue ChooseFont : **CF \_ SCRIPTSONLY**, **CF \_ SELECTSCRIPT** ou **CF \_ NOSCRIPTSEL**.

L’indicateur **CF \_ SCRIPTSONLY** indique à l’API de répertorier les polices pour tous les jeux de caractères qui ne sont pas des symboles ou des OEM.

Si vous souhaitez afficher uniquement les polices qui couvrent un jeu de caractères particulier, vous devez spécifier l’indicateur **CF \_ SELECTSCRIPT**. Avant d’appeler [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)), initialisez le champ *lfCharSet* de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Si vous souhaitez spécifier uniquement le jeu de caractères, affectez aux autres champs de la structure **LOGFONT** la **valeur null**. Pour que **ChooseFont** examine la structure **LOGFONT** , vous devez également spécifier l’indicateur **CF \_ INITTOLOGFONTSTRUCT** .

Enfin, comme pour tout autre champ de la boîte de dialogue police, vous pouvez choisir d’afficher une zone de liste de scripts vide. Cette fonctionnalité est utile si l’utilisateur a mis en surbrillance plusieurs polices différentes couvrant plusieurs jeux de caractères. Dans ce cas, vous devez appeler [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) avec l’indicateur **CF \_ NOSCRIPTSEL** .

à partir de Windows 7, [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) implémente la prise en charge du masquage des polices dans les listes de sélection de polices. **ChooseFont** répertorie uniquement les polices affichées et filtre les polices masquées lors de l’affichage des polices dans la zone de liste. l’indicateur supplémentaire (**CF \_ INACTIVEFONTS**) du membre flags de la structure [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) est ajouté pour vous permettre d’afficher toutes les polices installées dans la liste de polices, le même que **ChooseFont** se comporter avant Windows 7. pour plus d’informations sur les différences de comportement dans Windows 7 pour la fonction **ChooseFont** , consultez la [**boîte de dialogue commune de ChooseFont () Win32**](../win7appqual/choosefont-win32-common-dialog.md) dans le guide de [qualité des applications Windows 7](../win7appqual/windows-7-application-quality-cookbook.md). reportez-vous à la fonction **ChooseFont** et à la structure **ChooseFont** pour les différences d’expérience de l’utilisateur final dans Windows 7.

Notez que les jeux de caractères sont une notion héritée correspondant aux jeux de caractères pré-Unicode. À l’heure actuelle, il n’existe aucun mécanisme pour filtrer les polices en fonction des scripts Unicode ou des plages de caractères.

## <a name="font-controls-in-windows-scenic-ribbon"></a>contrôles de police dans Windows Scenic ruban

Windows 7 présente le ruban Windows Scenic qui est fourni avec un ensemble de contrôles ciblant la sélection des polices. ces contrôles de police prennent en charge le nouveau comportement de masquage de police Windows 7. Vous pouvez utiliser ces contrôles de police pour répertorier uniquement les polices affichées et autoriser l’utilisateur à sélectionner la police.

> [!Note]  
> la prise en charge du masquage des polices n’est pas disponible lorsque le ruban Windows Scenic s’exécute sur une plateforme antérieure à Windows 7.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**CHOOSEFONT, structure**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**contrôles de police dans Windows Scenic ruban**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**ChooseFont () boîte de dialogue commune Win32**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
