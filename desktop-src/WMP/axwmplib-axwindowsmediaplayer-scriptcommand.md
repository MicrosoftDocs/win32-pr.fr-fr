---
title: Événement commande de l’objet AxWindowsMediaPlayer
description: L’événement commande se produit lors de la réception d’une commande ou d’une URL synchronisée. | Événement commande de l’objet AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- événement commande de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193332"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a>Événement commande de l’objet AxWindowsMediaPlayer

L’événement commande se produit lors de la réception d’une commande ou d’une URL synchronisée.

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété | Description                                                   |
|----------|---------------------------------------------------------------|
| scType   | System. StringSpecifies le type de commande de script.<br/> |
| param    | System. StringSpecifies la commande de script.<br/>         |



 

## <a name="remarks"></a>Notes

les commandes peuvent être incorporées parmi les sons et les images d’un fichier ou d’un flux de média Windows. Les commandes sont une paire de chaînes Unicode associées à une heure désignée dans le flux. lorsque le flux atteint l’heure associée à la commande, le contrôle Lecteur Windows Media envoie un événement **commande** avec deux paramètres. Un paramètre spécifie le type de commande en cours d’envoi, tandis que l’autre paramètre spécifie la commande. Le type de paramètre est utilisé pour déterminer la façon dont le paramètre de commande est traité. Tout type de commande peut être incorporé dans un fichier ou un flux à gérer par l’événement **commande** .

le tableau suivant répertorie les types de commande de script qui sont traités automatiquement par Lecteur Windows Media.



| Type                   | Description                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Le contrôle affiche le texte associé dans l’élément HTML spécifié par IWMPClosedCaption. **captioningId**.                                                       |
| ÉVÉNEMENT                  | Le contrôle exécute les instructions définies pour l’événement spécifié.                                                                                                  |
| FILENAME               | Le contrôle réinitialise sa propriété **URL** , tente d’ouvrir le fichier spécifié et commence à lire immédiatement le nouveau flux.                                        |
| OPENEVENT              | Met en mémoire tampon la commande de type d’événement associée pour l’exécution en temps opportun du script d’événement.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | Le paramètre *param* contient le texte Lyric synchronisé. Lecteur Windows Media affiche le texte lyric dans la zone de légende fermée de la fonctionnalité de **diffusion** en cours. |
| TEXT                   | Le contrôle affiche le texte associé dans l’élément HTML spécifié par IWMPClosedCaption. **captioningId**.                                                       |
| URL                    | Le contrôle ouvre automatiquement l’URL spécifiée à l’aide du navigateur Internet par défaut si IWMPSettings. la propriété **invokeURLs** a la valeur true.                    |



 

Vous pouvez incorporer n’importe quel autre type de commande tant que vous fournissez du code pour gérer la commande. bien que les commandes inconnues soient ignorées par le contrôle Lecteur Windows Media, elles sont toujours transmises à l’événement **commande** .

L’événement commande n’est pas appelé si le fichier est en cours d’analyse en mode avance rapide ou rembobinage.

les commandes d’URL reçues par le contrôle Lecteur Windows Media sont automatiquement appelées dans votre navigateur Web par défaut si IWMPSettings. la propriété **invokeURLs** a la valeur true. Vous pouvez utiliser IWMPSettings. propriété **defaultFrame** pour spécifier le frame cible dans lequel la page Web s’affiche.

l’url envoyée à Lecteur Windows Media est traitée par rapport à l’url de base spécifiée par IWMPSettings. propriété **baseURL** . L’URL de base est concaténée avec l’URL relative, ce qui génère une URL entièrement spécifiée qui est transmise en tant que paramètre de commande par l’événement **commande** .

le contrôle Lecteur Windows Media traite toujours les commandes URL entrantes de la manière suivante :

1.  Une commande de type URL est reçue.
2.  IWMPSettings. **baseURL** est utilisé pour créer une URL complète à partir de l’URL relative spécifiée dans la commande de script.
3.  **Commande** est appelé.
4.  Après que **commande** a retourné, IWMPSettings. **invokeURLs** est activé.
5.  Si IWMPSettings. **invokeURLs** a la valeur true et la commande est une commande URL, l’URL spécifiée est appelée. Si IWMPSettings. **invokeURLs** a la valeur false ou, si la commande n’est pas une commande URL, la commande est ignorée.

lors de la création d’un fichier multimédia Windows, vous pouvez spécifier le cadre dans lequel la nouvelle URL est affichée en concaténant deux et et le nom du cadre dans le champ paramètre. L’exemple suivant illustre des paramètres **commande** typiques. Il spécifie que l’URL *MyPage* doit être lancée dans le frame *MyFrame* .


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



L’événement commande n’est pas appelé si le fichier est en cours d’analyse (transféré rapidement ou rembobiner).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB et C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. captioningId (VB et C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB et C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. defaultFrame (VB et C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB et C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





