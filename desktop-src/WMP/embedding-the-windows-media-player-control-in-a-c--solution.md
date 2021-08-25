---
title: incorporation du contrôle Lecteur Windows Media dans une Solution C
description: incorporation du contrôle Lecteur Windows Media dans une Solution C \
ms.assetid: 0889cfd8-ed1f-4d0c-aff8-bff2f55ffccb
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- contrôle de ActiveX, incorporation
- Lecteur Windows Media, C
- modèle objet Lecteur Windows Media, C
- modèle objet, C
- Lecteur Windows Media Mobile, C
- Lecteur Windows Media ActiveX contrôle, C
- Lecteur Windows Media contrôle Mobile ActiveX, C
- contrôle ActiveX, C
- incorporation, programmes C
- Incorporation de programme C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a067a407fccdd78d71d9e60bc00d1eae6950e3fdaf204f886c5e96edf372eb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901979"
---
# <a name="embedding-the-windows-media-player-control-in-a-c-solution"></a>incorporation du contrôle Lecteur Windows Media dans une Solution C#

pour utiliser les fonctionnalités de Lecteur Windows Media dans une application C#, commencez par ajouter le composant à un formulaire, comme décrit dans [utilisation du contrôle Lecteur Windows Media avec Microsoft Visual Studio](using-the-windows-media-player-control-with-microsoft-visual-studio.md)

Les sections suivantes décrivent comment créer une application qui lit des vidéos et utilise des boutons de lecture et d’arrêt personnalisés.

## <a name="add-the-video-window"></a>Ajouter la fenêtre vidéo

ajoutez le contrôle Lecteur Windows Media ActiveX à un formulaire. Redimensionnez le contrôle, puis placez-le à l’emplacement où vous souhaitez que la fenêtre vidéo apparaisse.

sélectionnez le contrôle Lecteur Windows Media, puis remplacez la valeur de la propriété **uiMode** par « none ». Ce paramètre masque les contrôles d’interface utilisateur. Quand l’utilisateur lit une vidéo, elle s’affiche dans la fenêtre. Pour le contenu audio uniquement, une visualisation s’affiche.

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



dans l’exemple de code précédent, « axWindowsMediaPlayer1 » est le nom par défaut du contrôle Lecteur Windows Media et « c : \\ mediafile. wmv » est un espace réservé pour le nom de l’élément multimédia que vous souhaitez lire. Vous pouvez utiliser n’importe quel chemin d’accès de fichier valide. Le symbole @ indique au compilateur de ne pas interpréter les barres obliques inverses comme des caractères d’échappement.

si vous avez ajouté le contenu multimédia numérique du kit de développement logiciel (SDK) Lecteur Windows Media à la bibliothèque dans Lecteur Windows Media, vous pouvez utiliser ce code à la place :


```CSharp
axWindowsMediaPlayer1.currentPlaylist = axWindowsMediaPlayer1.mediaCollection.getByName("mediafile");

```



étant donné que la propriété **autostart** est définie sur true par défaut, Lecteur Windows Media commencera à s’exécuter lorsque vous définirez la propriété **currentPlaylist** ou **URL** .

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
> le wrapper de code managé pour le contrôle Lecteur Windows Media expose l’objet **controls** en tant que **Ctlcontrols** pour éviter toute collision avec la propriété **controls** héritée de **System. Windows. Forms. Control**.

 

## <a name="add-error-handling"></a>Ajouter la gestion des erreurs

le contrôle Lecteur Windows Media ne lève pas d’exception lorsqu’il rencontre une erreur telle qu’une URL non valide. Au lieu de cela, il signale un événement. Votre application doit gérer les événements d’erreur envoyés par le lecteur.

pour créer un gestionnaire d’événements, commencez par ouvrir le Fenêtre Propriétés pour le contrôle Lecteur Windows Media. Dans la liste des événements, double-cliquez sur **MediaError**. Le code suivant s’affiche :


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

[**incorporation du contrôle Lecteur Windows Media dans une Solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




