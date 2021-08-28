---
title: Boîte de dialogue Couleur
description: Affiche une boîte de dialogue modale qui permet à l’utilisateur de choisir une valeur de couleur spécifique.
ms.assetid: 248586b5-5068-4021-8407-56eb79243789
keywords:
- entrée utilisateur, bibliothèque de boîtes de dialogue communes
- capture de l’entrée utilisateur, bibliothèque de boîtes de dialogue communes
- Bibliothèque de boîtes de dialogue communes
- boîtes de dialogue communes
- Couleur, boîte de dialogue
- Couleur partielle, boîte de dialogue
- boîte de dialogue couleur complète
- boîte de dialogue Personnaliser la couleur
- Modèle de couleurs RVB
- TSL, modèle de couleurs
- teinte saturation luminosité (TSL)
- TSL (luminosité de saturation de la teinte)
- RVB (rouge vert bleu)
- rouge vert bleu (RVB)
- raccordements, boîte de dialogue couleur
- boîtes de dialogue prédéfinies
- boîtes de dialogue, couleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bdfb1543de80ac105d4a6012a0c95ff46cd8da1fef204ed573d14d05a6dfe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726393"
---
# <a name="color-dialog-box"></a>Boîte de dialogue Couleur

Affiche une boîte de dialogue modale qui permet à l’utilisateur de choisir une valeur de couleur spécifique. L’utilisateur peut choisir une couleur à partir d’un ensemble de palettes de couleurs de base ou personnalisées. L’utilisateur peut également générer une valeur de couleur en modifiant les valeurs de couleur RVB ou teinte, saturation, luminosité (TSL) de l’interface utilisateur de la boîte de dialogue. La boîte de dialogue **couleur** retourne la valeur RVB de la couleur sélectionnée par l’utilisateur.

Vous créez et affichez une boîte de dialogue de **couleur** en initialisant une structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) et en transmettant la structure à la fonction [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) . En définissant des valeurs de paramètre différentes pour la structure **les ChooseColor.** , vous pouvez affecter la manière dont la boîte de dialogue couleur s’affiche. Par exemple, vous pouvez afficher une version d’interface utilisateur complète ou partielle de la boîte de dialogue. L’illustration suivante montre la version complète de l’interface utilisateur de la boîte de dialogue **couleur** .

![boîte de dialogue des couleurs](images/colordialogboxxp.png)

Si l’utilisateur clique sur le bouton **OK** , [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) retourne **true**. Le membre **rgbResult** de la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) contient la valeur de couleur RVB de la couleur sélectionnée par l’utilisateur. La valeur de couleur RVB spécifie les intensités des couleurs rouges, vertes et bleues individuelles qui composent la couleur sélectionnée. Les valeurs individuelles sont comprises entre 0 et 255. Utilisez les macros [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue)et [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue) pour extraire des couleurs individuelles d’une valeur de couleur RVB.

Si l’utilisateur annule la boîte de dialogue **couleur** ou si une erreur se produit, [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) retourne la **valeur false** et le membre **rgbResult** n’est pas défini. Pour déterminer la cause de l’erreur, appelez la fonction [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) pour récupérer la valeur d’erreur étendue.

Les sujets suivants sont traités dans cette section.

-   [Boîtes de dialogue couleur partielle et complète](#full-and-partial-color-dialog-boxes)
-   [Personnalisation de la boîte de dialogue couleur](#customizing-the-color-dialog-box)
    -   [Pour fournir un modèle personnalisé pour la boîte de dialogue couleur](#to-provide-a-custom-template-for-the-color-dialog-box)
    -   [Pour activer une procédure de Hook pour la boîte de dialogue couleur](#to-enable-a-hook-procedure-for-the-color-dialog-box)
-   [Modèles de couleurs utilisés par la boîte de dialogue couleur](#color-models-used-by-the-color-dialog-box)
    -   [Modèle de couleurs RVB](#rgb-color-model)
    -   [TSL, modèle de couleurs](#hsl-color-model)
    -   [Conversion de valeurs TSL en valeurs RVB](#converting-hsl-values-to-rgb-values)

## <a name="full-and-partial-color-dialog-boxes"></a>Boîtes de dialogue couleur partielle et complète

La boîte de dialogue couleur contient une version complète et une version partielle de l’interface utilisateur. La version complète inclut les contrôles de base et contient des contrôles supplémentaires qui permettent à l’utilisateur de créer des couleurs personnalisées. La version partielle contient des contrôles qui affichent les palettes de couleurs de base et personnalisées à partir desquelles l’utilisateur peut sélectionner une valeur de couleur.

La version partielle de la boîte de dialogue couleur comprend un bouton **définir des couleurs personnalisées** . L’utilisateur peut cliquer sur ce bouton pour afficher la version complète. Vous pouvez indiquer à la boîte de dialogue couleur d’afficher toujours la version complète en définissant l’indicateur **\_ FULLOPEN** dans le membre **Flags** de la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Pour empêcher l’utilisateur de créer des couleurs personnalisées, vous pouvez définir l’indicateur **\_ PREVENTFULLOPEN CC** pour désactiver le bouton **définir des couleurs personnalisées** .

Les couleurs de base représentent une sélection des couleurs disponibles sur l’appareil spécifié. Le nombre réel de couleurs affichées est déterminé par le pilote d’affichage. Par exemple, un pilote VGA affiche 48 couleurs et un pilote d’affichage monochrome affiche uniquement 16.

Les couleurs personnalisées sont celles que vous spécifiez ou que l’utilisateur crée. Lorsque vous créez une boîte de dialogue de couleur, vous devez utiliser le membre **lpCustColors** de la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) pour spécifier les valeurs initiales des 16 couleurs personnalisées. Si la version complète de la boîte de dialogue couleur est ouverte, l’utilisateur peut créer une couleur personnalisée selon l’une des méthodes suivantes :

-   Déplacement du curseur dans le contrôle de spectre de couleurs et le contrôle de diapositive de luminosité
-   Saisie de valeurs RVB dans les contrôles d’édition **rouge**, **vert** et **bleu**
-   Saisie de valeurs TSL dans les contrôles d’édition **Hue**, **SAT** et **Lum**

Pour ajouter une nouvelle couleur personnalisée à l’affichage des couleurs personnalisées, l’utilisateur peut cliquer sur le bouton **Ajouter aux couleurs personnalisées** . Par ailleurs, la boîte de dialogue copie la valeur RVB de la nouvelle couleur sur l’élément correspondant dans le tableau pointé par le membre **lpCustColors** . Pour conserver les nouvelles couleurs personnalisées entre les appels à [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)), vous devez allouer de la mémoire statique pour le tableau. Pour plus d’informations sur les modèles de couleurs RVB et TSL, consultez [modèles de couleurs utilisés par la boîte de dialogue couleur](#color-models-used-by-the-color-dialog-box).

## <a name="customizing-the-color-dialog-box"></a>Personnalisation de la boîte de dialogue couleur

Pour personnaliser une boîte de dialogue de couleur, vous pouvez utiliser l’une des méthodes suivantes :

-   Spécifier des valeurs dans la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) quand vous créez la boîte de dialogue
-   Fournir un modèle personnalisé
-   Fournir une procédure de raccordement

Vous pouvez modifier l’apparence et le comportement de la boîte de dialogue couleur en définissant des indicateurs dans le membre **Flags** de la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Par exemple, vous pouvez définir l’indicateur **cc \_ SOLIDCOLOR** pour indiquer à la boîte de dialogue d’afficher uniquement les couleurs unies. Pour faire en sorte que la boîte de dialogue sélectionne initialement une couleur autre que le noir, définissez l’indicateur **\_ RGBINIT CC** et spécifiez une couleur dans le membre **rgbResult** .

Vous pouvez fournir un modèle personnalisé pour la boîte de dialogue couleur, par exemple, si vous souhaitez inclure des contrôles supplémentaires propres à votre application. La fonction [**les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) utilise votre modèle personnalisé à la place du modèle par défaut.

### <a name="to-provide-a-custom-template-for-the-color-dialog-box"></a>Pour fournir un modèle personnalisé pour la boîte de dialogue couleur

1.  Créez le modèle personnalisé en modifiant le modèle par défaut spécifié dans le fichier Color. dlg. Les identificateurs de contrôle utilisés dans le modèle de boîte de dialogue couleur par défaut sont définis dans le fichier Color. dlg.
2.  Utilisez la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) pour activer le modèle comme suit :
    -   Si votre modèle personnalisé est une ressource d’une application ou d’une bibliothèque de liens dynamiques, définissez l’indicateur **cc \_ ENABLETEMPLATE** dans le membre **Flags** . Utilisez les membres **HINSTANCE** et **lpTemplateName** de la structure pour identifier le nom du module et de la ressource.

        Ou

    -   Si votre modèle personnalisé est déjà en mémoire, définissez l' **indicateur \_ ENABLETEMPLATEHANDLE CC** . Utilisez le membre **HINSTANCE** pour identifier l’objet mémoire qui contient le modèle.

Vous pouvez fournir une procédure de hook [**CCHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc) pour la boîte de dialogue couleur. La procédure de raccordement peut traiter les messages envoyés à la boîte de dialogue. Il peut également utiliser des messages inscrits pour contrôler le comportement de la boîte de dialogue. Si vous utilisez un modèle personnalisé pour définir des contrôles supplémentaires, vous devez fournir une procédure de raccordement pour traiter l’entrée de vos contrôles.

### <a name="to-enable-a-hook-procedure-for-the-color-dialog-box"></a>Pour activer une procédure de Hook pour la boîte de dialogue couleur

1.  Définissez l' **indicateur \_ ENABLEHOOK CC** dans le membre **Flags** de la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) .
2.  Spécifiez l’adresse de la procédure de raccordement dans le membre **lpfnHook** .

Après le traitement du message [**WM \_ INITDIALOG**](wm-initdialog.md) , la procédure de la boîte de dialogue envoie un message **WM \_ INITDIALOG** à la procédure de Hook. Le paramètre *lParam* de ce message est un pointeur vers la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) utilisée pour initialiser la boîte de dialogue.

La boîte de dialogue envoie le message [**COLOROKSTRING**](colorokstring.md) Registered à la procédure de hook lorsque l’utilisateur clique sur le bouton **OK** . La procédure de raccordement peut rejeter la couleur sélectionnée et forcer la boîte de dialogue à rester ouverte en retournant zéro lorsqu’elle reçoit ce message. La procédure de raccordement peut forcer la boîte de dialogue à sélectionner une couleur particulière en envoyant le message [**SETRGBSTRING**](setrgbstring.md) Registered à la boîte de dialogue. Pour utiliser ces messages enregistrés, vous devez passer les constantes **COLOROKSTRING** et **SETRGBSTRING** à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir un identificateur de message. Vous pouvez ensuite utiliser l’identificateur pour détecter et traiter les messages envoyés à partir de la boîte de dialogue, ou pour envoyer des messages à la boîte de dialogue.

## <a name="color-models-used-by-the-color-dialog-box"></a>Modèles de couleurs utilisés par la boîte de dialogue couleur

L’extension couleurs personnalisées de la boîte de dialogue couleur permet à l’utilisateur de spécifier une couleur à l’aide des valeurs RVB ou TSL. Toutefois, la structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) utilise uniquement des valeurs RVB pour signaler les couleurs créées ou sélectionnées par l’utilisateur.

-   [Modèle de couleurs RVB](#rgb-color-model)
-   [TSL, modèle de couleurs](#hsl-color-model)
-   [Conversion de valeurs TSL en valeurs RVB](#converting-hsl-values-to-rgb-values)

### <a name="rgb-color-model"></a>Modèle de couleurs RVB

Le modèle RGB est utilisé pour désigner des couleurs pour les affichages et d’autres appareils qui émettent de la lumière. Les valeurs valides pour le rouge, le vert et le bleu sont comprises entre 0 et 255, 0 indiquant une intensité minimale et une valeur de 255 indiquant une intensité maximale. L’illustration suivante montre comment les couleurs primaires rouge, vert et bleu peuvent être combinées pour produire quatre couleurs supplémentaires. (Pour les périphériques d’affichage, la couleur noire se produit lorsque les valeurs rouge, vert et bleu sont définies sur 0. Dans la technologie d’affichage, le noir est l’absence de toutes les couleurs.)

![cercles rouge, vert et bleu se chevauchant](images/rgbcolormodel.png)

Le tableau suivant répertorie les huit couleurs du modèle RGB et leurs valeurs RVB associées.



| Couleur   | Valeurs RVB    |
|---------|---------------|
| Rouge     | 255, 0,0     |
| Vert   | 0, 255, 0     |
| Bleu    | 0, 0, 255     |
| Cyan    | 0, 255, 255   |
| Magenta | 255, 0, 255   |
| Yellow  | 255, 255, 0   |
| Blancs   | 255, 255, 255 |
| Noir   | 0, 0, 0       |



 

Le système stocke les couleurs internes en tant que valeurs RVB de 32 bits qui ont la forme hexadécimale suivante : 0x00bbggrr.

L’octet de poids faible contient une valeur pour l’intensité relative du rouge ; le deuxième octet contient une valeur pour le vert ; et le troisième octet contient une valeur pour le bleu. L’octet de poids fort doit être égal à zéro.

Vous pouvez utiliser la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) pour obtenir une valeur RVB en fonction des intensités spécifiées pour les composants rouge, vert et bleu. Utilisez les macros [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue)et [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue) pour extraire des couleurs individuelles d’une valeur de couleur RVB.

### <a name="hsl-color-model"></a>TSL, modèle de couleurs

La boîte de dialogue couleur fournit des contrôles pour la spécification des valeurs TSL. L’illustration suivante montre le contrôle spectre des couleurs et le contrôle de la luminosité qui s’affichent dans la boîte de dialogue couleur. L’illustration montre également les plages de valeurs que l’utilisateur peut spécifier avec ces contrôles.

![échelle de couleurs et de luminosité](images/colordialogranges.png)

Dans la boîte de dialogue couleur, les valeurs de saturation et de luminosité doivent être comprises entre 0 et 240, et la valeur de teinte doit être comprise entre 0 et 239.

### <a name="converting-hsl-values-to-rgb-values"></a>Conversion de valeurs TSL en valeurs RVB

La procédure de boîte de dialogue fournie dans Comdlg32.dll de la boîte de dialogue couleur contient le code qui convertit les valeurs TSL en valeurs RVB correspondantes. Le tableau suivant répertorie les huit couleurs du modèle RGB et leurs valeurs TSL et RVB associées.



| Couleur   | valeurs HSL      | Valeurs RVB      |
|---------|-----------------|-----------------|
| Rouge     | (0, 240, 120)   | (255, 0, 0)     |
| Yellow  | (40, 240, 120)  | (255, 255, 0)   |
| Vert   | (80, 240, 120)  | (0, 255, 0)     |
| Cyan    | (120, 240, 120) | (0, 255, 255)   |
| Bleu    | (160, 240, 120) | (0, 0, 255)     |
| Magenta | (200, 240, 120) | (255, 0, 255)   |
| Blancs   | (0, 0, 240)     | (255, 255, 255) |
| Noir   | (0, 0, 0)       | (0, 0, 0)       |



 

 

 
