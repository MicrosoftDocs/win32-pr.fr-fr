---
title: Speak, méthode
description: Speak, méthode
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8798809dc4cdfa38438bee2fa9449f879871e4018b0e6b046d95a73583b03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475341"
---
# <a name="speak-method"></a>Speak, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Parle le texte ou le fichier audio spécifié pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ *  \[ *Texte* Speak \] , \[ *URL*\]



| Partie   | Description                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Text* | Facultatif. Chaîne qui spécifie ce que le caractère dit.                                                                                                                                                                                                   |
| *Url*  | Facultatif. Expression de chaîne spécifiant l’emplacement d’un fichier audio (. WAV ou. Format LWV). L’emplacement peut être spécifié sous la forme d’un fichier (y compris une spécification de chemin d’accès UNC) ou d’une URL (lorsque les données d’animation de caractères sont également récupérées via le protocole HTTP). |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Bien que les paramètres *Text* et *URL* soient facultatifs, l’un d’eux doit être fourni. Pour utiliser cette méthode avec un caractère configuré pour parler uniquement dans sa bulle de mot ou à l’aide d’un moteur TTS (Text-to-Speech), fournissez simplement le paramètre *Text* . Insérez un espace entre les mots pour définir les césures lexicales appropriées dans la bulle de mot, même pour les langues qui n’incluent pas traditionnellement des espaces.

Vous pouvez également inclure des caractères de barre verticale ( \| ) dans le paramètre *Text* pour désigner d’autres chaînes, afin que le serveur choisisse de manière aléatoire une autre chaîne chaque fois qu’il traite la méthode.

La prise en charge des caractères de la sortie TTS est définie lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent. Pour générer une sortie TTS, un moteur TTS compatible doit déjà être installé avant d’appeler cette méthode. Pour plus d’informations, consultez [accès aux services vocaux](accessing-speech-services.md).

Si vous utilisez le fichier audio enregistré (. WAV ou. LWV format uniquement) sortie pour le caractère, spécifiez l’emplacement du fichier dans le paramètre *URL* . Cette spécification de fichier peut inclure un chemin d’accès local (absolu ou relatif) ou UNC (Universal Naming Convention). Le nom de fichier ne peut pas contenir de caractères non inclus dans la page de codes US 1252. Toutefois, si vous utilisez le protocole HTTP pour accéder aux données d’animation de caractères, utilisez la méthode d' [**extraction**](get-method.md) pour charger l’animation avant d’appeler la méthode **Speak** . Pour plus d’informations sur Creative, consultez [utilisation de l’outil de modification des informations linguistiques Microsoft](using-the-microsoft-linguistic-information-sound-editing-tool.md) . Fichiers LWV.

Lorsque vous utilisez la sortie enregistrée de fichier audio, vous pouvez toujours utiliser le paramètre text pour spécifier les mots qui apparaissent dans la bulle de *texte* du caractère. Toutefois, si vous spécifiez un fichier audio linguistiquement amélioré (. LWV) pour le paramètre *URL* et ne spécifiez pas de texte pour le mot Balloon, le paramètre *Text* utilise le texte stocké dans le fichier.

Vous pouvez également modifier les paramètres de la sortie vocale avec des balises spéciales que vous incluez dans le paramètre *Text* . Pour plus d’informations, consultez [balises de sortie vocale Microsoft Agent](microsoft-agent-speech-output-tags.md).

Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) . Vous pouvez l’utiliser pour synchroniser d’autres parties de votre code avec la sortie orale du caractère, comme dans l’exemple suivant :


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here it is.")
...
   Sub Agent1_RequestComplete (ByVal Request as Object)
   ' Make certain the request exists
   If SpeakRequest Not Nothing Then
      ' See if it was this request
      If Request = SpeakRequest Then
         ' Display the message box 
         Msgbox "Ta da!"
      End If
   End If
   End Sub
```



Vous pouvez également utiliser un objet de [**requête**](/windows/desktop/lwef/the-request-object) pour vérifier certaines conditions d’erreur. Par exemple, si vous utilisez la méthode **Speak** pour parler et que vous n’avez pas de moteur TTS compatible installé, le serveur définit la propriété [**Status**](status-property.md) de l’objet **Request** sur « failed » et sa propriété [**Description**](description-property.md) sur « Class not registered » ou « Unknown or Object retournad Error ». Pour déterminer si un moteur TTS est installé, utilisez la propriété [**TTSModeID**](ttsmodeid-property.md) .

De même, si vous avez le caractère de la tentative de dicter un fichier audio, et si le fichier n’a pas été chargé ou qu’il y a un problème avec le périphérique audio, le serveur définit également la propriété [**Status**](status-property.md) de l’objet [**Request**](/windows/desktop/lwef/the-request-object) sur « failed » avec un numéro de code d’erreur approprié.

Vous pouvez également inclure des balises vocales de signets dans votre texte Speak pour synchroniser votre code :


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here \mrk=100\it is.")
...
   Sub Agent1_Bookmark (ByVal BookmarkID As Long)
   If BookmarkID = 100 Then
      ' Display the message box 
         Msgbox "Tada!"
      End If
   End Sub
```



Pour plus d’informations sur la balise de discours de signet, consultez [balises de sortie vocale](mrk-tag.md).

La méthode **Speak** utilise la dernière action jouée pour déterminer l’animation parlant à lire. Par exemple, si vous avez précédé la commande **Speak** avec la [**lecture**](play-method.md) «**GestureRight**», le serveur lira **GestureRight** , puis l’animation **GestureRight** Speaking. Si la dernière animation jouée n’a pas d’animation parlant, agent lit l’animation affectée à l’état de **conversation** du caractère.

Si vous appelez **Speak** et que le canal audio est occupé, la sortie audio du caractère n’est pas audible, mais le texte s’affiche dans la bulle.

La césure automatique des mots de l’agent dans le mot-bulle arrête les mots à l’aide de caractères d’espace blanc (par exemple, espace ou tabulation). Toutefois, si ce n’est pas le cas, il peut endommager un mot pour l’ajuster à la bulle. Dans les langages tels que le japonais, le chinois et le thaï, où les espaces ne sont pas utilisés pour couper des mots, insérez un caractère d’espace de largeur nulle Unicode (0x200B) entre les caractères pour définir des césures lexicales.

> [!Note]  
> La propriété [**Enabled**](enabled-property.md) de la bulle de mot doit également avoir la **valeur true** pour que le texte s’affiche.

 

> [!Note]  
> Définissez l’ID de langue du caractère (en définissant la valeur **LanguageID** du caractère avant d’utiliser la méthode **Speak** pour garantir l’affichage du texte approprié dans la bulle.

 

## <a name="see-also"></a>Voir aussi

[**Événement Bookmark**](bookmark-event.md), [**événement RequestStart**](requeststart-event.md), [**événement RequestComplete**](requestcomplete-event.md)


 

 