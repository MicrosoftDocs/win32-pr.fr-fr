---
description: L’exemple de reconnaissance avancée illustre des fonctionnalités avancées de l’interface de programmation d’applications (API) d’automatisation de Microsoft Tablet PC utilisée pour la reconnaissance de l’écriture manuscrite.
ms.assetid: 4c9b9f31-c317-43fd-8404-35295b41d093
title: Exemple de reconnaissance avancée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e23a078ded9c6967f8e45780f8cb3a739b246f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749117"
---
# <a name="advanced-recognition-sample"></a>Exemple de reconnaissance avancée

L’exemple de reconnaissance avancée illustre des fonctionnalités avancées de l’interface de programmation d’applications (API) d’automatisation de Microsoft Tablet PC utilisée pour la reconnaissance de l’écriture manuscrite.

Microsoft System Center ASP.NET 2.0 2007 offre les fonctionnalités suivantes :

-   Énumération du module de reconnaissance installé
-   Création d’un contexte de module de reconnaissance avec un langage spécifique
-   Utilisation de l’objet Recognizer
-   Définition des Factoid de reconnaissance et des listes de mots
-   Utilisation de guides pour améliorer la qualité de la reconnaissance
-   Reconnaissance dynamique en arrière-plan
-   Reconnaissance de mouvement

Les interfaces utilisées sont les suivantes : [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer), **IInkRecoContext**, [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult), **IInkRecognitionGuide**, **IInkWordList**, [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture), **IInkCollector**, **IInkDisp**, **IInkRenderer**, **IInkDrawingAttributes**, **IInkStrokes** et **IInkStroke**.

## <a name="ink-and-project-headers"></a>En-têtes d’encre et de projet

Tout d’abord, incluez les en-têtes pour les interfaces d’automatisation Tablet PC. Celles-ci sont installées avec le kit de développement logiciel (SDK) de plateforme Tablet PC. Le fichier TpcError. h contient les définitions des codes d’erreur de l’API Tablet PC.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
#include <TpcError.h>
```



Le fichier EventSinks. h définit les interfaces **IInkEventsImpl** et **IInkRecognitionEventsImpl** , et configure les événements [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md), [**Stroke**](inkcollector-stroke.md)et [**geste**](inkcollector-gesture.md) .


```C++
#include "EventSinks.h"
```



Le fichier ChildWnds. h contient les définitions des classes **CInkInputWnd** et **CRecoOutputWnd**, qui sont dérivées de CWindowImpl d’ATL et utilisées pour créer les fenêtres enfants de l’exemple.


```C++
#include "ChildWnds.h"
```



Le fichier AdvReco. h déclare la classe **CAdvRecoApp** , qui est la classe de fenêtre d’application pour cet exemple.


```C++
#include "AdvReco.h"
```



## <a name="initializing-the-application-window"></a>Initialisation de la fenêtre d’application

La méthode de la fenêtre `Run` configure l’objet **CAdvRecoApp** , charge le menu et l’icône de la fenêtre, crée un objet [**InkRecognizerContext**](inkrecognizercontext-class.md) pour le module de reconnaissance par défaut et démarre la boucle de message de la fenêtre.

La méthode **OnCreate** de la fenêtre gère l’événement **WM \_ Create** et crée les fenêtres enfants. Un objet [**InkCollector**](inkcollector-class.md) se connecte à la source de l’événement du collecteur d’encre et active l’entrée d’encre dans la fenêtre d’entrée. Ensuite, il crée un objet [**InkRecognizerGuide**](inkrecognizerguide-class.md) et utilise la propriété [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer) du collecteur d’encre pour convertir les rectangles de la boîte du repère de reconnaissance en espace d’encre. Enfin, la méthode **OnCreate** crée un objet [**InkWordList**](inkwordlist-class.md) .

## <a name="handling-ink-collector-events"></a>Gestion des événements du collecteur d’encre

La méthode **OnStroke** de la fenêtre gère l’événement [**Stroke**](inkcollector-stroke.md) du collecteur d’encre. Le nouvel objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) est ajouté au [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) du collecteur Ink.

La méthode **OnGesture** de la fenêtre gère l’événement de [**mouvement**](inkcollector-gesture.md) du collecteur d’encre. La méthode **OnGesture** identifie le mouvement, en commençant par le geste de confiance le plus élevé, et vérifie si la fenêtre prend en charge ce geste particulier. Si le mouvement est pris en charge, la zone englobante du geste est invalidée, car le mouvement est supprimé de la collection de traits. Si le mouvement n’est pas pris en charge, l’événement de **mouvement** est annulé, ce qui amène le collecteur d’encre à déclencher un événement [**Stroke**](inkcollector-stroke.md) . Enfin, la fenêtre résultats est mise à jour.

## <a name="handling-recognizer-context-events"></a>Gestion des événements de contexte de reconnaissance

La méthode **OnRecognitionWithAlternates** de la fenêtre gère l’événement [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) du contexte du module de reconnaissance. La méthode **OnRecognitionWithAlternates** affiche les résultats de la reconnaissance dans la fenêtre résultats.

## <a name="handling-menu-commands"></a>Gestion des commandes de menu

La méthode **OnRecognizer** de la fenêtre gère les commandes dans le menu du module de reconnaissance. Si la commande **par défaut** a été sélectionnée, la méthode [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) de [InkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) est utilisée pour récupérer le module de reconnaissance par défaut ; dans le cas contraire, le module de reconnaissance sélectionné est récupéré. Ensuite, un contexte de module de reconnaissance est créé et utilisé, et le menu et la barre d’État sont mis à jour.

La méthode **OnFactoidWordlist** de la fenêtre gère la commande **use** de la personne dans le menu **Factoid** . La propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) du contexte du module de reconnaissance est définie sur **null** pour réinitialiser le contexte du module de reconnaissance. Si vous désactivez l’option **utiliser** la balise de [**la personne,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) la propriété texte du contexte du module de reconnaissance est définie sur **null**. Sinon, **la propriété de** la balise de contexte du module de reconnaissance est définie sur le [**InkWordList**](inkwordlist-class.md) qui a été créé dans la méthode **OnCreate** . Enfin, le [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) du collecteur d’encres est rattaché au contexte du module de reconnaissance, la méthode [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) du contexte du module de reconnaissance est appelée et le menu est mis à jour.

La méthode **OnFactoid** de la fenêtre gère les commandes Factoid dans le menu **Factoid** . Il définit d’abord la propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) du contexte du module de reconnaissance sur la **valeur null**, définit la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) du contexte du module de reconnaissance sur le Factoid sélectionné et réaffecte le [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) du collecteur d’encre au contexte du module de reconnaissance. Si l’objet [Factoid](factoid-constants.md) est pris en charge par le contexte du module de reconnaissance, la méthode [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) du contexte du module de reconnaissance est appelée ; dans le cas contraire, un message d’erreur s’affiche. Enfin, le menu et la barre d’État sont mis à jour.

La méthode **OnGuide** de la fenêtre gère les commandes dans le menu du **repère** . Si le contexte du [**module de reconnaissance**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) prend en charge les options du repère, la méthode **OnGuide** affecte la **valeur null** au contexte du contexte du module de reconnaissance, définit [**la propriété du repère du**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) contexte du module de reconnaissance sur le paramètre du repère sélectionné, réaffecte le [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) du collecteur d’encre au contexte du module de reconnaissance et appelle la méthode [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) du contexte du module de reconnaissance. Dans le cas contraire, un message d’erreur s’affiche. Enfin, la fenêtre d’entrée, le menu et la barre d’État sont mis à jour.

La méthode **OnMode** de la fenêtre gère les commandes du menu **mode** . Il désactive le collecteur d’encres, met à jour la propriété [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) du collecteur d’encre, met à jour le menu et affiche ou masque les listes de mouvements. Enfin, le collecteur d’encre est activé.

La méthode **OnRecognize** de la fenêtre gère la commande **Recognize** dans le menu Ink. Elle appelle la méthode [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) du contexte de reconnaissance pour empêcher l’ajout de l’encre au contexte du module de reconnaissance. Cela est parfois nécessaire, car tous les identifiants ne prennent pas en charge la reconnaissance partielle. Elle appelle ensuite la méthode [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) du contexte de reconnaissance et transmet les résultats à la méthode **OnRecognitionWithAlternates** de la fenêtre. Enfin, le [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) du collecteur d’encres est réaffecté au contexte du module de reconnaissance.

La méthode **OnClear** de la fenêtre gère la commande **Clear** dans le menu **Ink** . Elle supprime les traits de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) du collecteur d’encre, libère l’ancienne collection Strokes et en crée une pour la propriété **Ink** du collecteur d’encre, puis attache la nouvelle collection Strokes au contexte de module de reconnaissance.

La méthode **OnExit** de la fenêtre gère la commande **quitter** dans le menu **Ink** et déclenche l' \_ événement WM Close.

## <a name="helper-methods"></a>Méthodes d'assistance

La méthode **LoadMenu** de la fenêtre est appelée à partir de la méthode **Run** de la fenêtre et ajoute la liste des module de reconnaissance pris en charge et la liste des Factoids prises en charge au menu. Tout d’abord, elle récupère [InkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)). Il itère ensuite au sein des module de reconnaissance disponibles et sélectionne uniquement ceux qui ont une liste de langues dans la propriété **languages** , qu’il ajoute au menu du module de **reconnaissance** . Enfin, il remplit le menu **Factoid** avec la liste de Factoids définie en tant que constante globale.

La méthode **UseRecognizer** de la fenêtre est appelée à partir de la méthode **OnRecognizer** de la fenêtre lorsque l’utilisateur sélectionne un nouveau module de reconnaissance. Il crée un contexte de module de reconnaissance, détache l’ancien contexte du récepteur d’événements de reconnaissance, efface et libère l’ancien contexte et attache le nouveau contexte au récepteur d’événements de la reconnaissance.

Ensuite, la méthode **UseRecognizer** vérifie la propriété des [**capacités**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) du module de reconnaissance, qui retourne une valeur [**InkRecognizerCapabilities**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities) . Si le module de reconnaissance prend en charge l’entrée en ligne, la commande **lignes** du menu du **repère** est activée. Si le module de reconnaissance prend en charge les entrées boxed, la commande **cases** est activée. Si le module de reconnaissance ne prend pas en charge l’entrée libre, la commande **None** est désactivée. Si la sélection du repère en cours n’est pas prise en charge, la propriété [**Guide**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) du contexte de module de reconnaissance et le menu sont mis à jour.

Ensuite, la méthode **UseRecognizer** tente de définir les propriétés [**de la recherche et de**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) la [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) du contexte du module de reconnaissance. Si l’un des paramètres n’est pas pris en charge par le module de reconnaissance, la valeur par défaut est utilisée et le menu est mis à jour.

Enfin, la méthode **UseRecognizer** attache la propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) de l’objet [**InkDisp**](inkdisp-class.md) du collecteur Ink au contexte du module de reconnaissance, modifie la police de la fenêtre de sortie en une valeur prise en charge par la langue du module de reconnaissance, réinitialise la fenêtre de sortie et met à jour les résultats de la reconnaissance en appelant la méthode [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) du contexte de reconnaissance.

La méthode **GetGestureName** de la fenêtre est appelée à partir de la méthode **OnGesture** de la fenêtre. Elle recherche le mouvement et retourne un index au nom du geste, qui est stocké dans une table de chaînes du fichier AdvReco. rc.

 

 
