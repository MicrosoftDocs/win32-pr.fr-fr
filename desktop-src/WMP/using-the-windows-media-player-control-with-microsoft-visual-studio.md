---
title: utilisation du contrôle Lecteur Windows Media avec Microsoft Visual Studio
description: utilisation du contrôle Lecteur Windows Media avec Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- contrôle de ActiveX, incorporation
- Lecteur Windows Media, .NET Framework
- Lecteur Windows Media modèle objet, .NET Framework
- modèle objet, .NET Framework
- Lecteur Windows Media Mobile, .NET Framework
- Lecteur Windows Media contrôle ActiveX, .NET Framework
- Lecteur Windows Media contrôle de ActiveX Mobile, .NET Framework
- contrôle ActiveX, .NET Framework
- Lecteur Windows Media contrôle ActiveX, Visual Studio
- Lecteur Windows Media contrôle de ActiveX Mobile, Visual Studio
- contrôle ActiveX, Visual Studio
- .NET Framework, Visual Studio incorporation de programme
- incorporation, Visual Studio des programmes
- Visual Studio, incorporation de programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293759"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>utilisation du contrôle Lecteur Windows Media avec Microsoft Visual Studio

vous pouvez ajouter le contrôle de la série Lecteur Windows Media 9 ou version ultérieure ActiveX à une application .NET Framework par le biais de la boîte à outils dans Visual Studio.

## <a name="adding-the-windows-media-player-control"></a>ajout du contrôle Lecteur Windows Media

avant de créer un nouveau projet, assurez-vous que la version la plus récente de Lecteur Windows Media et le kit de développement logiciel (SDK) Lecteur Windows Media sont installés sur votre ordinateur.

démarrez Visual Studio, puis créez un nouveau projet.

dans Visual Studio, ouvrez la boîte à outils.

si Lecteur Windows Media n’apparaît pas dans la partie **composants** de la boîte à outils, procédez comme suit :

1.  Cliquez avec le bouton droit dans la boîte à outils, puis sélectionnez **choisir les éléments**. La boîte de dialogue Personnaliser la boîte **à outils** s’ouvre.
2.  sous l’onglet **composants COM** , sélectionnez Lecteur Windows Media.

    si Lecteur Windows Media n’apparaît pas dans la liste, cliquez sur **parcourir**, puis ouvrez Wmp.dll, qui doit se trouver dans le \\ dossier Windows System32.

3.  Cliquez sur **OK**. le contrôle Lecteur Windows Media sera placé dans l’onglet boîte à outils actif.

vous pouvez maintenant sélectionner Lecteur Windows Media dans la boîte à outils et l’ajouter à un formulaire.

Visual Studio donne au contrôle Lecteur Windows Media un nom par défaut tel que « axWindowsMediaPlayer1 ». Vous pouvez choisir un nom plus facile à mémoriser, tel que « Player ».

l’ajout du contrôle Lecteur Windows Media à partir de la boîte à outils ajoute également des références à deux bibliothèques créées par Visual Studio, AxWMPLib et WMPLib. Vous pouvez les trouver dans le Explorateur de solutions sous **références**.

Pour faciliter l’utilisation des objets dans l’espace de noms Player, vous devez inclure l’espace de noms dans les directives using ou Imports de vos fichiers, comme suit :


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



La directive garantit que vous pouvez faire référence aux objets **Player** sans qualifier complètement leurs noms.

> [!Note]  
> le contrôle Lecteur Windows Media est un objet **AxWindowsMediaPlayer** de l’espace de noms **AxWMPLib** . Toutefois, la classe **AxWindowsMediaPlayer** utilise des types de données, des interfaces et d’autres éléments de l’espace de noms **wmplib** .

 

## <a name="configuring-visibility-of-the-control"></a>Configuration de la visibilité du contrôle

lorsque vous ajoutez pour la première fois le contrôle Lecteur Windows Media à un formulaire, il est visible. Si vous ne souhaitez pas utiliser l’image visible du lecteur dans votre application, masquez le lecteur par défaut en définissant l’une des propriétés suivantes :



| Propriété        | Valeur                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | « invisible » (consultez [Player. UIMODE](player-uimode.md).) |
| **Visible**     | "false"                                               |
| **Size. Width**  | 0                                                     |
| **Size. Height** | 0                                                     |



 

vous pouvez définir ces propriétés dans le code ou dans la fenêtre **propriétés** lorsque le contrôle Lecteur Windows Media est sélectionné dans le concepteur de formulaires.

## <a name="object-model-compatibility-of-the-control"></a>Compatibilité du modèle objet du contrôle

le modèle objet du contrôle Lecteur Windows Media est fondamentalement le même dans la .NET Framework que dans le code et le script non managés. Toutefois, il existe des différences dans la façon dont les éléments sont exposés :

-   La plupart des objets sont exposés sous le nom de leur interface COM sous-jacente. Par exemple, l’objet **playlist** est exposé en tant que **IWMPPlaylist**.
-   Certaines interfaces ont des versions ultérieures. Par exemple, **IWMPMedia** a reçu des fonctionnalités supplémentaires dans **IWMPMedia2** et **IWMPMedia3**. Si vous déclarez un objet en tant que **IWMPMedia**, vous avez généralement accès aux fonctionnalités de toutes les versions de l’interface. toutefois, IntelliSense® ne reconnaît pas les méthodes ou les propriétés des interfaces ultérieures, et l’éditeur Visual Basic .net ne corrige pas automatiquement la casse. pour tirer pleinement parti d’IntelliSense et d’autres fonctionnalités de Visual Studio, déclarez l’objet à l’aide de la version la plus récente de l’interface, par exemple **IWMPMedia3**.
-   il n’existe pas de propriétés indexées (C#) ou de propriétés par défaut (Visual Basic .net). par exemple, pour récupérer un **élément Playlist. item**, vous devez appeler la méthode d’accesseur **\_ item IWMPlaylist. get** en C# ou récupérer la propriété **IWMPlayist. item** dans Visual Basic .net.
-   en raison d’un conflit de noms entre la propriété de **contrôles** Lecteur Windows Media et la propriété **controls** exposée par chaque contrôle, la version Player de cette propriété est appelée **CtlControls** dans le contexte du contrôle ActiveX. (toutefois, ce n’est pas le cas lorsque vous créez le joueur par programme plutôt qu’en tant que contrôle de ActiveX.)

utilisez l’explorateur d’objets de Visual Studio pour localiser les noms d’API corrects pour les méthodes et les objets dans les espaces de noms **AxWMPLib** et **WMPLib** .

## <a name="distributing-your-application"></a>Distribution de votre application

Lorsque vous distribuez votre application, veillez à installer AxInterop.WMPLib.dll et Interop.WMPLib.dll dans le dossier de l’application. vous devrez également vous assurer que la version de Lecteur Windows Media requise est installée sur l’ordinateur de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**création du contrôle Lecteur Windows Media par programmation**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**incorporation du contrôle Lecteur Windows Media dans une Solution C#**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**incorporation du contrôle Lecteur Windows Media dans une Solution Visual Basic .net**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




