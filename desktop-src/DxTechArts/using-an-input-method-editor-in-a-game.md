---
title: Utilisation d’un éditeur de méthode d’entrée dans un jeu
description: Cet article explique comment vous pouvez implémenter un contrôle d’édition IME de base dans une application Microsoft DirectX en mode plein écran.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8cb5869579da97aeea465b572082a23a963e9db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471965"
---
# <a name="using-an-input-method-editor-in-a-game"></a>Utilisation d’un éditeur de méthode d’entrée dans un jeu

> [!Note]  
> cet article détaille l’utilisation de l’éditeur de méthode d’entrée (IME) Windows XP. les modifications apportées à l’IME pour Windows Vista ne sont pas entièrement détaillées dans cet article. pour plus d’informations sur les modifications apportées à l’ime pour Windows vista, consultez [éditeurs de méthode d’entrée (ime)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) dans [Windows vista-une vue d’ensemble de Ever-Expanding de l’internationalisation](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) sur le portail informatique et de développement Global Microsoft.

 

Un éditeur de méthode d’entrée (IME) est un programme qui permet d’entrer facilement du texte à l’aide d’un clavier standard pour les langues asiatiques telles que le chinois, le japonais, le coréen et d’autres langages avec des caractères complexes. Par exemple, avec les éditeurs IME, un utilisateur peut taper des caractères complexes dans un traitement de texte, ou un joueur d’un jeu en ligne multijoueur massive peut discuter avec des amis dans des caractères complexes.

Cet article explique comment vous pouvez implémenter un contrôle d’édition IME de base dans une application Microsoft DirectX en mode plein écran. Les applications qui tirent parti de DXUT bénéficient automatiquement des fonctionnalités IME. Pour les applications qui n’utilisent pas le Framework, cet article explique comment ajouter la prise en charge de l’IME à un contrôle d’édition.

Contenu :

-   [Comportement IME par défaut](#default-ime-behavior)
-   [Utilisation des IME avec DXUT](#using-imes-with-dxut)
-   [Substitution du comportement IME par défaut](#overriding-the-default-ime-behavior)
-   [Fonctions](#functions)
-   [Messages](#ime-messages)
-   [Exemples](#examples)
    -   [Version de l’IME CHT 4,2, 4,3 et 4,4](#cht-ime-version-42-43-and-44)
    -   [Version de l’IME CHT 5,0](#cht-ime-version-50)
    -   [Version de l’IME CHT 5,1, 5,2 et CHS (IME) 5,3](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [Version d’IME CHS 4,1](#chs-ime-version-41)
    -   [Version d’IME CHS 4,2](#chs-ime-version-42)
-   [Messages IME](#ime-messages)
    -   [\_INPUTLANGCHANGE WM](#wm_inputlangchange)
    -   [STARTCOMPOSITION de l' \_ IME WM \_](/windows)
    -   [COMPOSITION de l' \_ IME WM \_](/windows)
    -   [ENDCOMPOSITION de l' \_ IME WM \_](/windows)
    -   [notification de l' \_ IME WM \_](/windows)
-   [Rendu](#rendering)
    -   [Indicateur de paramètres régionaux d’entrée](#input-locale-indicator)
    -   [Fenêtre de composition](#composition-window)
    -   [Lecture et Windows candidat](#reading-and-candidate-windows)
-   [Limitations](#limitations)
-   [Informations de Registre](#registry-information)
-   [Annexe A : versions CHT par système d’exploitation](#appendix-a-cht-versions-per-operating-system)
-   [Informations complémentaires](#further-information)
-   [GetReadingString](#getreadingstring)
-   [ShowReadingWindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>Comportement IME par défaut

Les IME mappent l’entrée au clavier aux composants phonétiques ou à d’autres éléments de langage spécifiques à une langue sélectionnée. Dans un scénario classique, l’utilisateur tape des clés qui représentent la prononciation d’un caractère complexe. Si l’IME reconnaît la prononciation comme étant valide, elle présente à l’utilisateur une liste de mots et d’expressions candidats à partir desquels l’utilisateur peut sélectionner un choix final. le mot choisi est ensuite envoyé à l’application par le biais d’une série de messages Microsoft Windows [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) . Étant donné que l’IME fonctionne à un niveau inférieur à l’application en interceptant l’entrée au clavier, la présence d’un IME est transparente pour l’application. presque toutes les applications Windows peuvent facilement tirer parti des éditeurs de logiciels sans avoir conscience de leur existence et sans nécessiter un codage spécial.

Un IME standard affiche plusieurs fenêtres pour guider l’utilisateur à travers l’entrée de caractères, comme illustré dans les exemples suivants.

![l’éditeur IME affiche plusieurs fenêtres](images/ime-elements.png)

| Type de fenêtre                                       | Description                                                                                                                                                                                                                                                                                                                 | Sortie IME                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| R. Fenêtre de lecture                                 | Contient les séquences de touches du clavier ; change généralement après chaque séquence de touches.                                                                                                                                                                                                                                              | chaîne de lecture                               |
| B. Fenêtre de composition                             | Contient la collection de caractères que l’utilisateur a composés avec l’IME. Ces caractères sont dessinés par l’IME en haut de l’application. Lorsque l’utilisateur notifie l’IME que la chaîne de composition est satisfaisante, l’IME envoie ensuite la chaîne de composition à l’application via une série de \_ messages WM char. | chaîne de composition                           |
| C. Fenêtre candidate                               | Lorsque l’utilisateur a entré une prononciation valide, l’IME affiche une liste des caractères candidats qui correspondent tous à la prononciation donnée. L’utilisateur sélectionne ensuite le caractère prévu dans cette liste, et l’IME ajoute ce caractère à l’affichage de la fenêtre de composition.                                                    | caractère suivant dans la chaîne de composition |
| D. Indicateur de [paramètres régionaux d’entrée](/windows/desktop/Intl/nls-terminology) | Affiche la langue sélectionnée par l’utilisateur pour l’entrée au clavier. cet indicateur est incorporé dans la barre des tâches Windows. La langue d’entrée peut être sélectionnée en ouvrant les options régionales et linguistiques du panneau de configuration, puis en cliquant sur détails dans l’onglet langues.                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>Utilisation des IME avec DXUT

Dans DXUT, la classe CDXUTIMEEditBox implémente la fonctionnalité IME. Cette classe est dérivée de la classe CDXUTEditBox, le contrôle d’édition de base fourni par le Framework. CDXUTIMEEditBox étend ce contrôle d’édition pour prendre en charge les IME en remplaçant les méthodes CDXUTIMEEditBox. Les classes sont conçues pour aider les développeurs à apprendre ce qu’ils doivent effectuer à partir de l’infrastructure pour implémenter la prise en charge de l’éditeur IME dans leurs propres contrôles d’édition. Le reste de cette rubrique explique comment l’infrastructure, et CDXUTIMEEditBox en particulier, substitue un contrôle d’édition de base pour implémenter les fonctionnalités IME.

La plupart des variables spécifiques à l’IME dans CDXUTIMEEditBox sont déclarées comme statiques, car de nombreux tampons et États IME sont spécifiques au processus. Par exemple, un processus ne possède qu’un seul tampon pour la chaîne de composition. Même si le processus comporte dix contrôles d’édition, ils partagent tous la même mémoire tampon de la chaîne de composition. La mémoire tampon de la chaîne de composition pour CDXUTIMEEditBox est donc statique, ce qui empêche l’application d’occuper de l’espace mémoire inutile.

CDXUTIMEEditBox est implémenté dans le code DXUT suivant :

(Racine SDK) \\ Exemples \\ \\ Common \\ DXUTgui. cpp du C++

## <a name="overriding-the-default-ime-behavior"></a>Substitution du comportement IME par défaut

normalement, un IME utilise des procédures de Windows standard pour créer une fenêtre (consultez [utilisation de Windows](/windows/desktop/winmsg/using-windows)). Dans des circonstances normales, cela produit des résultats satisfaisants. Toutefois, lorsque l’application s’affiche en mode plein écran, comme c’est souvent le cas pour les jeux, les fenêtres standard ne fonctionnent plus et peuvent ne pas s’afficher en plus de l’application. pour surmonter ce problème, l’application doit dessiner les fenêtres IME lui-même au lieu de s’appuyer sur Windows pour effectuer cette tâche.

Lorsque le comportement de création de la fenêtre IME par défaut ne fournit pas ce qu’une application requiert, l’application peut remplacer la gestion de la fenêtre IME. Une application peut y parvenir en traitant les messages liés à l’IME et en appelant l’API du [Gestionnaire de méthode d’entrée](/windows/desktop/Intl/input-method-manager) (IMM).

Lorsqu’un utilisateur interagit avec un IME pour entrer des caractères complexes, le IMM envoie des messages à l’application pour l’informer des événements importants, tels que le démarrage d’une composition ou l’indication de la fenêtre candidate. En général, une application ignore ces messages et les transmet au gestionnaire de messages par défaut, ce qui amène l’IME à les gérer. Lorsque l’application, au lieu du gestionnaire par défaut, gère les messages, elle contrôle exactement ce qui se produit à chacun des événements IME. Souvent, le gestionnaire de messages récupère le contenu des différentes fenêtres IME en appelant l’API IMM. Une fois que l’application dispose de ces informations, elle peut dessiner correctement les fenêtres IME lorsqu’elle doit effectuer un rendu à l’affichage.

## <a name="functions"></a>Fonctions

Un IME doit recevoir la chaîne de lecture, masquer la fenêtre de lecture et afficher l’orientation de la fenêtre de lecture. Ce tableau indique les fonctionnalités par version de l’IME :



|                    | Obtenir la chaîne de lecture                                                | Masquer la fenêtre de lecture                       | Orientation de la fenêtre de lecture                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| **Avant la version 6,0** | R. Lecture directe des données privées de l’IME d’accès à la fenêtre. Voir « structure 4 » | Interceptez les messages privés de l’IME. Voir « 3 messages » | Examinez les informations du Registre. Voir « 5 informations de Registre » |
| **Après la version 6,0**  | [GetReadingString](#getreadingstring)                                 | [ShowReadingWindow](#showreadingwindow)     | [GetReadingString](#getreadingstring)                      |



 

## <a name="messages"></a>Messages

Les messages suivants n’ont pas besoin d’être traités pour un IME plus récent qui implémente [ShowReadingWindow](#showreadingwindow)().

Les messages suivants sont interceptés par le gestionnaire de messages d’application (autrement dit, ils ne sont pas transmis à DefWindowProc) pour empêcher la fenêtre de lecture de s’affiche.

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>Exemples

Les exemples suivants montrent comment obtenir des informations de chaîne d’un IME antérieur qui n’a pas de GetReadingString (). Le code génère les sorties suivantes :



| Output              | Description                                                                                      |
|--------------|---------------------------------------------------------------------------------------|
| DWORD dwlen  | Longueur de la chaîne de lecture.                                                          |
| DWORD dwerr  | Index du caractère d’erreur.                                                                   |
| LPWSTR WSTR  | Pointeur désignant la chaîne de lecture.                                                         |
| BOOL Unicode | Si la valeur est true, la chaîne de lecture est au format Unicode. Dans le cas contraire, il est au format multioctet. |



 

### <a name="cht-ime-version-42-43-and-44"></a>Version de l’IME CHT 4,2, 4,3 et 4,4

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a>Version de l’IME CHT 5,0

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a>Version de l’IME CHT 5,1, 5,2 et CHS (IME) 5,3

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a>Version d’IME CHS 4,1

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a>Version d’IME CHS 4,2

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a>Messages IME

Une application en plein écran doit gérer correctement les messages liés à l’IME suivants :

### <a name="wm_inputlangchange"></a>\_INPUTLANGCHANGE WM

Le IMM envoie un \_ message WM INPUTLANGCHANGE à la fenêtre active d’une application une fois que les paramètres régionaux d’entrée ont été modifiés par l’utilisateur avec une combinaison de touches (généralement Alt + Maj) ou avec l’indicateur de paramètres régionaux d’entrée sur la barre des tâches ou la barre de langue. La barre de langue est un contrôle à l’écran avec lequel l’utilisateur peut configurer un service de texte. (Voir [comment afficher la barre de langue](/windows/desktop/TSF/how-to-set-up-tsf).) La capture d’écran suivante montre une liste de sélection de la langue qui s’affiche lorsque l’utilisateur clique sur l’indicateur de paramètres régionaux.

![liste de sélection de la langue qui s’affiche lorsque l’utilisateur clique sur l’indicateur de paramètres régionaux](images/ime-langselection.png)

Lorsque le IMM envoie un \_ message WM INPUTLANGCHANGE, CDXUTIMEEditBox doit effectuer plusieurs tâches importantes :

1.  La méthode GetKeyboardLayout est appelée pour retourner l’identificateur de paramètres régionaux (ID) d’entrée pour le thread d’application. La classe CDXUTIMEEditBox enregistre cet ID dans sa variable membre statique s \_ hklCurrent pour une utilisation ultérieure. Il est important pour l’application de connaître les paramètres régionaux d’entrée actuels, car l’IME pour chaque langue a son propre comportement distinct. Le développeur peut avoir besoin de fournir un code différent pour différents paramètres régionaux d’entrée.
2.  CDXUTIMEEditBox Initialise une chaîne à afficher dans l’indicateur de langue de la zone d’édition. Cet indicateur peut afficher la langue d’entrée active lorsque l’application s’exécute en mode plein écran et que la barre des tâches ou la barre de langue n’est pas visible.
3.  La méthode ImmGetConversionStatus est appelée pour indiquer si les paramètres régionaux d’entrée sont en mode de conversion natif ou non natif. Le mode de conversion natif permet à l’utilisateur d’entrer du texte dans la langue choisie. Le mode de conversion non natif fait du clavier un comportement en anglais standard. Il est important de fournir à l’utilisateur un indice visuel sur le type de mode de conversion dans lequel se trouve l’IME, afin que l’utilisateur puisse facilement savoir quels caractères attendre quand il appuie sur une touche. CDXUTIMEEditBox fournit cette indication visuelle avec une couleur d’indicateur de langue. Lorsque les paramètres régionaux d’entrée utilisent un IME avec le mode de conversion natif, la classe CDXUTIMEEditBox dessine le texte de l’indicateur avec la couleur définie par le \_ paramètre m IndicatorImeColor. Lorsque l’IME est en mode de conversion non natif ou qu’aucun IME n’est utilisé, la classe dessine le texte de l’indicateur avec la couleur définie par le \_ paramètre m IndicatorEngColor.
4.  CDXUTIMEEditBox vérifie les paramètres régionaux d’entrée et définit la variable membre statique s \_ bInsertOnType sur true pour le coréen et false pour toutes les autres langues. Cet indicateur est requis en raison des différents comportements des IME coréens et de tous les autres IME. Lorsque vous entrez des caractères dans des langues autres que le coréen, le texte entré par l’utilisateur est affiché dans la fenêtre de composition, et l’utilisateur peut modifier librement le contenu de la chaîne de composition. L’utilisateur appuie sur la touche entrée lorsque la chaîne de composition est satisfaite, et la chaîne de composition est envoyée à l’application sous la forme d’une série de \_ messages WM char. Toutefois, dans les éditeurs IME coréens, quand un utilisateur appuie sur une touche pour entrer du texte, un caractère est immédiatement envoyé à l’application. Lorsque l’utilisateur appuie ensuite sur plus de touches pour modifier ce caractère initial, le caractère dans la zone d’édition change pour refléter une entrée supplémentaire de la part de l’utilisateur. Pour l’essentiel, l’utilisateur compose des caractères dans la zone d’édition. Ces deux comportements sont suffisamment différents pour que CDXUTIMEEditBox doive coder spécifiquement pour chacun d’eux.
5.  La méthode membre statique SetupImeApi est appelée pour récupérer les adresses de deux fonctions à partir du module IME : GetReadingString et ShowReadingWindow. Si ces fonctions existent, ShowReadingWindow est appelé pour masquer la fenêtre de lecture par défaut pour cet IME. Étant donné que l’application affiche la fenêtre de lecture elle-même, elle indique à l’IME de désactiver le dessin de la fenêtre de lecture par défaut afin qu’elle n’interfère pas avec le rendu plein écran.

Le IMM envoie un \_ message WM IME \_ SETCONTEXT lorsqu’une fenêtre de l’application est activée. Le paramètre lParam de ce message contient un indicateur qui indique à l’éditeur de l’éditeur que les fenêtres doivent être dessinées et celles qui ne le doivent pas. Étant donné que l’application gère tout le dessin, elle n’a pas besoin de l’éditeur IME pour dessiner les fenêtres IME. Par conséquent, le gestionnaire de messages de l’application affecte simplement à lParam la valeur 0 et retourne.

Pour que les applications prennent en charge l’IME, un traitement spécial est nécessaire pour le message IME WM \_ IME \_ SETCONTEXT. étant donné que Windows envoie généralement ce message à l’application avant d’appeler la méthode PanoramaInitialize (), le Panorama n’a pas la possibilité de traiter l’interface utilisateur pour afficher les fenêtres de liste de candidats.

l’extrait de code suivant indique à Windows applications de ne pas afficher l’interface utilisateur associée à la fenêtre liste des candidats, ce qui permet au Panorama de gérer spécifiquement cette interface utilisateur.

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>STARTCOMPOSITION de l' \_ IME WM \_

Le IMM envoie un \_ \_ message STARTCOMPOSITION WM à l’application lorsqu’une composition IME est sur le le début de la séquence de touches par l’utilisateur. Si l’IME utilise la fenêtre de composition, il affiche la chaîne de composition actuelle dans une fenêtre de composition. CDXUTIMEEditBox gère ce message en effectuant deux tâches :

1.  CDXUTIMEEditBox efface la mémoire tampon de la chaîne de composition et la mémoire tampon d’attribut. Ces mémoires tampons sont des membres statiques de CDXUTIMEEditBox.
2.  CDXUTIMEEditBox définit la \_ variable de membre statique bHideCaret sur true. Ce membre, défini dans la classe de base CDXUTEditBox, contrôle si le curseur dans la zone d’édition doit être dessiné lors du rendu de la zone d’édition. La fenêtre de composition fonctionne de la même manière qu’une zone d’édition avec du texte et un curseur. Pour éviter toute confusion lorsque la fenêtre de composition est visible, la zone d’édition masque son curseur afin qu’un seul curseur soit visible à la fois.

### <a name="wm_ime_composition"></a>COMPOSITION de l' \_ IME WM \_

Le IMM envoie un \_ message de composition WM IME \_ à l’application lorsque l’utilisateur entre une séquence de touches pour modifier la chaîne de composition. La valeur de lParam indique le type d’informations que l’application peut récupérer à partir du gestionnaire de méthode d’entrée. L’application doit récupérer les informations disponibles en appelant [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) , puis enregistrer les informations dans sa mémoire tampon privée afin de pouvoir restituer les éléments IME ultérieurement.

CDXUTIMEEditBox vérifie et récupère les données de chaîne de composition suivantes :



| [**WM \_ Valeur \_**](/windows/desktop/Intl/wm-ime-composition) de l’indicateur lParam de la composition IME | Données                           | Description                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| comfromateurs \_ gc                                                         | Attribut de composition          | Cet attribut contient des informations telles que l’état de chaque caractère dans la chaîne de composition (par exemple, converti ou non converti). Ces informations sont nécessaires, car CDXUTIMEEditBox colore les caractères de la chaîne de composition différemment en fonction de leurs attributs.                                                                                   |
| catalogues globaux \_ COMPCLAUSE                                                       | Informations sur la clause de composition | Ces informations de clause sont utilisées lorsque l’IME japonais est actif. Lorsqu’une chaîne de composition japonaise est convertie, les caractères peuvent être regroupés en une clause qui est convertie en une entité unique. Lorsque l’utilisateur déplace le curseur, CDXUTIMEEditBox utilise ces informations pour mettre en surbrillance la clause entière, plutôt qu’un seul caractère dans la clause. |
| catalogues globaux \_ COMPSTR                                                          | Chaîne de composition             | Cette chaîne est la chaîne à jour qui est composée par l’utilisateur. Il s’agit également de la chaîne affichée dans la fenêtre de composition.                                                                                                                                                                                                                                        |
| catalogues globaux \_ CURSORPOS                                                        | Position du curseur de la composition    | La fenêtre de composition implémente un curseur, similaire au curseur dans une zone d’édition. L’application peut récupérer la position du curseur lors du traitement du \_ message de composition de l’IME WM afin \_ de dessiner le curseur correctement.                                                                                                                                            |
| GC \_ RESULTSTR                                                        | Chaîne de résultat                  | La chaîne de résultat est disponible lorsque l’utilisateur est sur le paragraphe de terminer le processus de composition. Cette chaîne doit être récupérée et les caractères doivent être envoyés à la zone d’édition.                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>ENDCOMPOSITION de l' \_ IME WM \_

Le IMM envoie un \_ \_ message ENDCOMPOSITION WM à l’application lorsque l’opération de composition IME se termine. Cela peut se produire lorsque l’utilisateur appuie sur la touche entrée pour approuver la chaîne de composition, ou la touche ÉCHAP pour annuler la composition. CDXUTIMEEditBox gère ce message en définissant la mémoire tampon de la chaîne de composition sur vide. Il définit ensuite \_ bHideCaret sur false, car la fenêtre de composition est fermée et le curseur dans la zone d’édition doit à nouveau être visible.

Le gestionnaire de messages CDXUTIMEEditBox affecte également \_ à bShowReadingWindow la valeur false. Cet indicateur contrôle si la classe dessine la fenêtre de lecture lorsque la zone d’édition s’affiche elle-même. elle doit donc avoir la valeur FALSe lorsqu’une composition se termine.

### <a name="wm_ime_notify"></a>notification de l' \_ IME WM \_

Le IMM envoie un \_ \_ message de notification de l’IME WM à l’application chaque fois qu’une fenêtre IME change. Une application qui gère le dessin des fenêtres IME doit traiter ce message afin qu’il prenne en charge toute mise à jour du contenu de la fenêtre. WParam indique la commande ou la modification qui a lieu. CDXUTIMEEditBox gère les commandes suivantes :




| Commande IME | Description | 
|-------------|-------------|
| <a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a> | Cet attribut contient des informations telles que l’état de chaque caractère dans la chaîne de composition (par exemple, converti ou non converti). Ces informations sont nécessaires, car CDXUTIMEEditBox colore les caractères de la chaîne de composition différemment en fonction de leurs attributs. | 
| <a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a> | Envoyé à l’application lorsque la fenêtre candidate est sur le lieu d’être ouverte ou mise à jour, respectivement. La fenêtre candidate s’ouvre lorsqu’un utilisateur souhaite modifier le texte converti. La fenêtre est mise à jour lorsqu’un utilisateur déplace l’indicateur de sélection ou modifie la page. CDXUTIMEEditBox utilise un gestionnaire de messages pour ces deux commandes, car les tâches requises sont exactement les mêmes :<br /><ol><li>CDXUTIMEEditBox définit le membre bShowWindow de la structure candidat List s_CandList sur TRUE pour indiquer que la fenêtre candidate doit être dessinée lors du rendu de frame.</li><li>CDXUTIMEEditBox récupère la liste des candidats en appelant <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, d’abord pour obtenir la taille de mémoire tampon requise, puis de nouveau pour obtenir les données réelles.</li><li>La structure de liste de candidats privée s_CandList est initialisée avec les données candidates récupérées.</li><li>Les chaînes candidates sont stockées sous la forme d’un tableau de chaînes.</li><li>L’index de l’entrée sélectionnée, ainsi que l’index de la page, sont enregistrés.</li><li>CDXUTIMEEditBox vérifie si le style de la fenêtre candidate est vertical ou horizontal. Si le style de fenêtre est horizontal, une mémoire tampon de chaîne supplémentaire, le membre HoriCand de s_CandList, doivent être initialisées avec toutes les chaînes candidates, avec des espaces insérés entre toutes les chaînes adjacentes. Lors du rendu d’une fenêtre candidate verticale, les chaînes de candidats individuelles sont dessinées l’une après l’autre, avec les coordonnées y incrémentées pour chaque chaîne. Toutefois, cette chaîne HoriCand doit être utilisée lors du rendu d’une fenêtre candidate horizontale, car le caractère espace est la meilleure façon de séparer deux chaînes adjacentes sur la même ligne.</li></ol> | 
| <a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a> | Envoyé à l’application lorsqu’une fenêtre candidate est sur le moment de se fermer. Cela se produit lorsqu’un utilisateur a effectué une sélection à partir de la liste de candidats. CDXUTIMEEditBox gère cette commande en affectant à l’indicateur visible de la fenêtre candidate la valeur FALSe, puis en effaçant la mémoire tampon de la chaîne candidate. | 
| IMN_PRIVATE | Envoyé à l’application lorsque l’IME a mis à jour sa chaîne de lecture suite à la saisie ou à la suppression de caractères par l’utilisateur. L’application doit récupérer la chaîne de lecture et l’enregistrer pour le rendu. CDXUTIMEEditBox a deux méthodes pour récupérer la chaîne de lecture, en fonction de la façon dont les chaînes de lecture sont prises en charge dans l’IME : <br /><ul><li>Si l’IME prend en charge la fonction GetReadingString, GetReadingString est appelé pour extraire la chaîne de lecture.</li><li>Si l’IME n’implémente pas GetReadingString, CDXUTIMEEditBox récupère la chaîne de lecture à partir du contenu du contexte d’entrée.</li></ul> | 




 

## <a name="rendering"></a>Rendu

Le rendu des éléments IME et Windows est simple. CDXUTIMEEditBox permet à la classe de base de s’afficher en premier, car les fenêtres IME doivent apparaître au-dessus du contrôle d’édition. Une fois la zone d’édition de base rendue, CDXUTIMEEditBox vérifie l’indicateur de visibilité de chaque fenêtre IME (indicateur, composition, candidat et fenêtre de lecture) et dessine la fenêtre si elle doit être visible. Pour obtenir une description des différents types de fenêtre IME, voir comportement IME par défaut.

### <a name="input-locale-indicator"></a>Indicateur de paramètres régionaux d’entrée

L’indicateur de paramètres régionaux d’entrée est restitué avant toute autre fenêtre IME, car il s’agit d’un élément qui est toujours affiché. Elle doit donc apparaître sous d’autres fenêtres IME. CDXUTIMEEditBox restitue l’indicateur en appelant la méthode RenderIndicator, dans laquelle la couleur de la police de l’indicateur est déterminée en examinant la variable statique imposed \_ qui reflète le mode de conversion IME actuel. Lorsque l’IME est activé et que la conversion native est active, la méthode utilise m \_ IndicatorImeColor comme couleur de l’indicateur. Si l’IME est désactivé ou est en mode de conversion non natif, m \_ IndicatorImeColor est utilisé pour dessiner le texte de l’indicateur. Par défaut, la fenêtre d’indicateur est dessinée à droite de la zone d’édition. Les applications peuvent modifier ce comportement en remplaçant la méthode RenderIndicator.

L’illustration suivante montre les différentes apparences d’un indicateur de paramètres régionaux d’entrée pour l’anglais, le japonais en mode de conversion alphanumérique et le japonais en mode de conversion natif :

![apparences différentes d’un indicateur de paramètres régionaux d’entrée pour l’anglais et le japonais](images/ime-indicator.png)

### <a name="composition-window"></a>Fenêtre de composition

Le dessin de la fenêtre de composition est géré dans la méthode RenderComposition de CDXUTIMEEditBox. La fenêtre de composition flotte au-dessus de la zone d’édition. Elle doit être dessinée à la position du curseur du contrôle d’édition sous-jacent. CDXUTIMEEditBox gère le rendu comme suit :

1.  La chaîne de composition entière est dessinée à l’aide des couleurs de la chaîne de composition par défaut.
2.  Les caractères avec certains attributs spéciaux doivent être dessinés dans des couleurs différentes. par conséquent, CDXUTIMEEditBox examine les caractères de la chaîne de composition et inspecte l’attribut de chaîne. Si l’attribut appelle des couleurs différentes, le caractère est à nouveau dessiné avec les couleurs appropriées.
3.  Le curseur de la fenêtre de composition est dessiné pour terminer le rendu.

Le curseur doit clignoter pour les IME coréens, mais il ne doit pas être destiné à d’autres éditeurs IME. RenderComposition détermine si le curseur doit être visible en fonction des valeurs du minuteur lorsque l’IME coréen est utilisé.

### <a name="reading-and-candidate-windows"></a>Lecture et Windows candidat

Les fenêtres de lecture et de candidat sont rendues par la même méthode CDXUTIMEEditBox, RenderCandidateReadingWindow. Les deux fenêtres contiennent un tableau de chaînes pour la disposition verticale, ou une chaîne unique dans le cas d’une disposition horizontale. La majeure partie du code de RenderCandidateReadingWindow est utilisée pour positionner la fenêtre afin qu’aucune partie de la fenêtre ne se situe en dehors de la fenêtre de l’application et qu’elle soit découpée.

## <a name="limitations"></a>Limites

Les éditeurs IME contiennent parfois des fonctionnalités avancées pour améliorer la facilité d’entrée de texte. Voici quelques-unes des fonctionnalités des IME les plus récents. Ces fonctionnalités avancées ne sont pas présentes dans DXUT. L’implémentation de la prise en charge de ces fonctionnalités avancées peut être difficile, car aucune interface n’est définie pour obtenir les informations nécessaires à partir des éditeurs IME.

IME chinois traditionnel avancé avec liste de candidats développée :

![IME chinois traditionnel avancé avec liste de candidats développée](images/ime-advanced1.png)

IME japonais avancé avec certaines entrées candidates qui contiennent du texte supplémentaire pour décrire leurs significations :

![IME japonais avancé avec certaines entrées candidates qui contiennent du texte supplémentaire pour décrire leurs significations](images/ime-advanced2.png)

IME coréen avancé qui comprend un système de reconnaissance de l’écriture manuscrite :

![IME coréen avancé qui comprend un système de reconnaissance de l’écriture manuscrite](images/ime-advanced3.png)

## <a name="registry-information"></a>Informations de Registre

Les informations de Registre suivantes sont vérifiées pour déterminer l’orientation de la fenêtre de lecture, lorsque l’IME actuel est ancien CHT New Phonetic qui n’implémente pas GetReadingString ().



| Clé                                                           | Valeur            |
|---------------------------------------------------------------|------------------|
| \\Logiciel HKCU \\ Microsoft \\ Windows \\ CurrentVersion \\ IME \_ Name | mappage du clavier |



 

Où : \_ le nom IME est MSTCIPH si la version du fichier IME est 5,1 ou ultérieure ; sinon, le nom de l’IME \_ est tintlgnt.

L’orientation de la fenêtre de lecture est horizontale dans les cas suivants :

-   L’IME est version 5,0 et la valeur de mappage du clavier est 0X22 ou 0x23
-   L’IME est version 5,1 ou version 5,2 et la valeur de mappage du clavier est 0X22, 0x23 ou 0x24.

Si aucune condition n’est remplie, la fenêtre de lecture est verticale.

## <a name="appendix-a-cht-versions-per-operating-system"></a>Annexe A : versions CHT par système d’exploitation



| Système d’exploitation           | Version de l’IME CHT |
|----------------------------|-----------------|
| Windows 98                 | 4,2             |
| Windows 2000               | 4.3             |
| unknown                    | 4.4             |
| Windows J'                 | 5.0             |
| Office XP                  | 5,1             |
| Windows XP                 | 5.2             |
| Downloadble Web autonome | 6.0             |



 

## <a name="further-information"></a>Informations complémentaires

Pour plus d'informations, reportez-vous aux procédures suivantes :

-   [Installation et utilisation des éditeurs de méthode d’entrée](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [Affichage de texte international](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [Le consortium Unicode](https://www.unicode.org/)
-   Développement de logiciels internationaux. Dr. international. 2e ed. Redmond, WA : Microsoft Press, 2003.

## <a name="getreadingstring"></a>GetReadingString

Obtient les informations de chaîne de lecture.

**Paramètres**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[dans le \] contexte d’entrée.

</dd> <dt>

<span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*
</dt> <dd>

\[dans la \] longueur de lpwReadingBuf, dans WCHAR. Si la valeur est zéro, cela signifie que la longueur de la mémoire tampon de lecture des requêtes.

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf* 
</dt> <dd>

\[sortie \] de la lecture de la chaîne de retour (pas de fin nulle).

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex* 
</dt> <dd>

\[out \] de retour de l’index du caractère d’erreur dans la chaîne de lecture.

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical* 
</dt> <dd>

\[\]si la valeur est true, la lecture de l’interface utilisateur est verticale. Sinon, puMaxReadingLen horizontal.

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen* 
</dt> <dd>

\[\]longueur de l’interface utilisateur de lecture. La longueur maximale de lecture n’est pas fixe ; Cela dépend non seulement de la disposition du clavier, mais également du mode d’entrée (par exemple, le code interne, l’entrée de substitution).

</dd> </dl>

**Valeurs retournées**

Longueur de la chaîne de lecture.

**Remarques**

Si la valeur de retour est supérieure à la valeur de uReadingBufLen, tous les paramètres de sortie ne sont pas définis.

Cette fonction est implémentée dans l’IME CHT 6,0 ou version ultérieure et peut être acquise par GetProcAddress sur un handle de module IME. le descripteur du module IME peut être obtenu par ImmGetIMEFileName et LoadLibrary.

**Configuration requise**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Titre**
</dt> <dd>

Déclaré dans IMM. h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Importer la bibliothèque**
</dt> <dd>

Utilisez IMM. lib.

</dd> </dl>

## <a name="showreadingwindow"></a>ShowReadingWindow

Affichez (ou masquez) la fenêtre de lecture.

**Paramètres**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[dans le \] contexte d’entrée.

</dd> <dt>

<span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow* 
</dt> <dd>

\[dans \] la propriété définie sur true pour afficher la fenêtre de lecture (ou false pour la masquer).

</dd> </dl>

**Valeurs retournées**

**Remarques**

Retourne la valeur TRUE en cas de réussite ou FALSe dans le cas contraire.

**Configuration requise**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Titre**
</dt> <dd>

Déclaré dans IMM. h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Importer la bibliothèque**
</dt> <dd>

Utilisez IMM. lib.

</dd> </dl>
