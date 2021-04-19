---
title: Intégration du contrôle du lecteur Windows Media dans une solution C
description: Incorporation du contrôle du lecteur Windows Media dans une solution C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Lecteur Windows Media, C
- Windows Media Player Object Model, C
- modèle objet, C
- Lecteur Windows Media Mobile, C
- Contrôle ActiveX du lecteur Windows Media, C
- Contrôle ActiveX mobile pour Windows Media Player, C
- Contrôle ActiveX, C
- incorporation, programmes C
- Incorporation de programme C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c950bed9812cea0aa6ce28995fd6998bb8417ac
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "106511462"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>Incorporation du contrôle du lecteur Windows Media dans une solution C#

Pour utiliser la fonctionnalité du lecteur Windows Media dans une application C#, commencez par ajouter le composant à un formulaire, comme décrit dans [utilisation du contrôle du lecteur Windows Media avec Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

Les sections suivantes décrivent comment créer une application qui lit des vidéos et utilise des boutons de lecture et d’arrêt personnalisés.

## <a name="add-the-video-window"></a>Ajouter la fenêtre vidéo

Ajoutez le contrôle ActiveX du lecteur Windows Media à un formulaire. Redimensionnez le contrôle, puis placez-le à l’emplacement où vous souhaitez que la fenêtre vidéo apparaisse.

Sélectionnez le contrôle du lecteur Windows Media, puis modifiez la propriété **UIMODE** en « None ». Ce paramètre masque les contrôles d’interface utilisateur. Quand l’utilisateur lit une vidéo, elle s’affiche dans la fenêtre. Pour le contenu audio uniquement, une visualisation s’affiche.

## <a name="add-two-buttons-and-adjust-the-form"></a>Ajouter deux boutons et ajuster le formulaire

À présent, ajoutez deux boutons au formulaire. Sélectionnez le premier bouton et affectez à la propriété **Text** la valeur « Play ». Sélectionnez le deuxième bouton et définissez sa propriété **Text** sur « STOP ».

## <a name="add-the-play-code"></a>Ajouter le code de lecture

Double-cliquez sur le bouton **lecture** pour afficher la fenêtre de code. En C#, le code suivant s’affiche :


```CSharp
private void button1_Click(object sender, System.EventArgs e)
{

}

```



Ajoutez cette ligne entre les deux accolades :


```CSharp
axWindowsMediaPlayer1.URL = @"c:\mediafile.wmv";

```



Dans l’exemple de code précédent, « axWindowsMediaPlayer1 » est le nom par défaut du contrôle du lecteur Windows Media et « c : \\ mediafile. wmv » est un espace réservé pour le nom de l’élément multimédia que vous souhaitez lire. Vous pouvez utiliser n’importe quel chemin d’accès de fichier valide. Le symbole @ indique au compilateur de ne pas interpréter les barres obliques inverses comme des caractères d’échappement.

Si vous avez ajouté le contenu multimédia numérique du kit de développement logiciel (SDK) du lecteur Windows Media à la bibliothèque dans le lecteur Windows Media, vous pouvez utiliser ce code à la place :


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



Étant donné que la propriété **AutoStart** est définie sur true par défaut, le lecteur Windows Media démarre la lecture lorsque vous définissez la propriété **currentPlaylist** ou **URL** .

## <a name="add-the-stop-code"></a>Ajouter le code d’arrêt

Double-cliquez sur le bouton **arrêter** pour afficher la fenêtre de code. En C#, le code suivant s’affiche :


```CSharp
private void button2_Click(object sender, System.EventArgs e)
{

}

```



Ajoutez cette ligne entre les deux accolades :


```CSharp
axWindowsMediaPlayer1.Ctlcontrols.stop();

```



> [!Note]  
> Le wrapper de code managé pour le contrôle du lecteur Windows Media expose l’objet **contrôles** en tant que **Ctlcontrols** pour éviter toute collision avec la propriété **Controls** héritée de **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Ajouter la gestion des erreurs

Le contrôle du lecteur Windows Media ne lève pas d’exception lorsqu’il rencontre une erreur telle qu’une URL non valide. Au lieu de cela, il signale un événement. Votre application doit gérer les événements d’erreur envoyés par le lecteur.

Pour créer un gestionnaire d’événements, commencez par ouvrir le Fenêtre Propriétés pour le contrôle du lecteur Windows Media. Dans la liste des événements, double-cliquez sur **MediaError**. Le code suivant s’affiche :


```CSharp
private void Player_MediaError(object sender, _WMPOCXEvents_MediaErrorEvent e)
{
}

```



Le code suivant peut être inséré dans la méthode pour fournir une fonctionnalité de gestion des erreurs minimale. Notez que les informations sur l’erreur peuvent être récupérées à partir de l’argument **\_ WMPOCXEvents \_ MediaErrorEvent** .


```CSharp
try
// If the Player encounters a corrupt or missing file, 
// show the hexadecimal error code and URL.
{
    IWMPMedia2 errSource = e.pMediaObject as IWMPMedia2;
    IWMPErrorItem errorItem = errSource.Error;
    MessageBox.Show("Error " + errorItem.errorCode.ToString("X") 
                    + " in " + errSource.sourceURL);
}
catch(InvalidCastException)
// In case pMediaObject is not an IWMPMedia item.
{
    MessageBox.Show("Error.");
} 

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Intégration du contrôle du lecteur Windows Media dans une solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




