---
title: Utilisation du contrôle du lecteur Windows Media avec Microsoft Visual Studio
description: Utilisation du contrôle du lecteur Windows Media avec Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Lecteur Windows Media,. NET Framework
- Windows Media Player Object Model, .NET Framework
- modèle objet, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Contrôle ActiveX du lecteur Windows Media, .NET Framework
- Contrôle ActiveX mobile du lecteur Windows Media, .NET Framework
- Contrôle ActiveX, .NET Framework
- Contrôle ActiveX du lecteur Windows Media, Visual Studio
- Contrôle ActiveX Windows Media Player Mobile, Visual Studio
- Contrôle ActiveX, Visual Studio
- .NET Framework, incorporation de programme Visual Studio
- incorporation, programmes Visual Studio
- Visual Studio, incorporation de programmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104029913"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>Utilisation du contrôle du lecteur Windows Media avec Microsoft Visual Studio

Vous pouvez ajouter le contrôle ActiveX Windows Media Player 9 ou une version ultérieure à une application .NET Framework par le biais de la boîte à outils de Visual Studio.

## <a name="adding-the-windows-media-player-control"></a>Ajout du contrôle du lecteur Windows Media

Avant de créer un nouveau projet, assurez-vous que la dernière version du lecteur Windows Media et du kit de développement logiciel (SDK) Windows Media Player est installée sur votre ordinateur.

Démarrez Visual Studio, puis créez un nouveau projet.

Dans Visual Studio, ouvrez la boîte à outils.

Si le lecteur Windows Media n’apparaît pas dans la partie **composants** de la boîte à outils, procédez comme suit :

1.  Cliquez avec le bouton droit dans la boîte à outils, puis sélectionnez **choisir les éléments**. La boîte de dialogue Personnaliser la boîte **à outils** s’ouvre.
2.  Sous l’onglet **composants com** , sélectionnez lecteur Windows Media.

    Si le lecteur Windows Media n’apparaît pas dans la liste, cliquez sur **Parcourir**, puis ouvrez Wmp.dll, qui doit se trouver dans le \\ dossier Windows system32.

3.  Cliquez sur **OK**. Le contrôle du lecteur Windows Media est placé dans l’onglet Boîte à outils actif.

Vous pouvez maintenant sélectionner Windows Media Player dans la boîte à outils et l’ajouter à un formulaire.

Visual Studio donne au contrôle du lecteur Windows Media un nom par défaut tel que « axWindowsMediaPlayer1 ». Vous pouvez choisir un nom plus facile à mémoriser, tel que « Player ».

L’ajout du contrôle du lecteur Windows Media à partir de la boîte à outils ajoute également des références à deux bibliothèques créées par Visual Studio, AxWMPLib et WMPLib. Vous pouvez les trouver dans le Explorateur de solutions sous **références**.

Pour faciliter l’utilisation des objets dans l’espace de noms Player, vous devez inclure l’espace de noms dans les directives using ou Imports de vos fichiers, comme suit :


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



La directive garantit que vous pouvez faire référence aux objets **Player** sans qualifier complètement leurs noms.

> [!Note]  
> Le contrôle du lecteur Windows Media est un objet **AxWindowsMediaPlayer** de l’espace de noms **AxWMPLib** . Toutefois, la classe **AxWindowsMediaPlayer** utilise des types de données, des interfaces et d’autres éléments de l’espace de noms **wmplib** .

 

## <a name="configuring-visibility-of-the-control"></a>Configuration de la visibilité du contrôle

Lorsque vous ajoutez pour la première fois le contrôle du lecteur Windows Media à un formulaire, il est visible. Si vous ne souhaitez pas utiliser l’image visible du lecteur dans votre application, masquez le lecteur par défaut en définissant l’une des propriétés suivantes :



| Propriété        | Valeur                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | « invisible » (consultez [Player. UIMODE](player-uimode.md).) |
| **Visible**     | "false"                                               |
| **Size. Width**  | 0                                                     |
| **Size. Height** | 0                                                     |



 

Vous pouvez définir ces propriétés dans le code ou dans la fenêtre **Propriétés** lorsque le contrôle du lecteur Windows Media est sélectionné dans le concepteur de formulaires.

## <a name="object-model-compatibility-of-the-control"></a>Compatibilité du modèle objet du contrôle

Le modèle objet pour le contrôle du lecteur Windows Media est fondamentalement le même dans le .NET Framework que dans le code et le script non managés. Toutefois, il existe des différences dans la façon dont les éléments sont exposés :

-   La plupart des objets sont exposés sous le nom de leur interface COM sous-jacente. Par exemple, l’objet **playlist** est exposé en tant que **IWMPPlaylist**.
-   Certaines interfaces ont des versions ultérieures. Par exemple, **IWMPMedia** a reçu des fonctionnalités supplémentaires dans **IWMPMedia2** et **IWMPMedia3**. Si vous déclarez un objet en tant que **IWMPMedia**, vous avez généralement accès aux fonctionnalités de toutes les versions de l’interface. Toutefois, IntelliSense® ne reconnaît pas les méthodes ou les propriétés des interfaces ultérieures, et l’éditeur Visual Basic .NET ne corrige pas automatiquement la casse. Pour tirer le meilleur parti d’IntelliSense et d’autres fonctionnalités de Visual Studio, déclarez l’objet à l’aide de la version la plus récente de l’interface, par exemple **IWMPMedia3**.
-   Il n’existe pas de propriétés indexées (C#) ou de propriétés par défaut (Visual Basic .NET). Par exemple, pour récupérer un **élément playlist. Item**, vous devez appeler la méthode d’accesseur **\_ Item IWMPlaylist. Get** en C# ou récupérer la propriété **IWMPlayist. Item** dans Visual Basic .net.
-   En raison d’un conflit de noms entre la propriété **contrôles** du lecteur Windows Media et la propriété **contrôles** exposée par chaque contrôle, la version Player de cette propriété est appelée **CtlControls** dans le contexte du contrôle ActiveX. (Toutefois, ce n’est pas le cas lorsque vous créez le joueur par programmation plutôt qu’en tant que contrôle ActiveX.)

Utilisez l’Explorateur d’objets de Visual Studio pour rechercher les noms d’API corrects pour les méthodes et les objets dans les espaces de noms **AxWMPLib** et **wmplib** .

## <a name="distributing-your-application"></a>Distribution de votre application

Lorsque vous distribuez votre application, veillez à installer AxInterop.WMPLib.dll et Interop.WMPLib.dll dans le dossier de l’application. Vous devrez également vous assurer que la version requise du lecteur Windows Media est installée sur l’ordinateur de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du contrôle du lecteur Windows Media par programmation**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**Incorporation du contrôle du lecteur Windows Media dans une solution C#**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**Intégration du contrôle du lecteur Windows Media dans une solution Visual Basic .NET**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




