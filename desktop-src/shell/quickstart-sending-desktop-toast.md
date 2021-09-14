---
description: Ce guide de démarrage rapide montre comment déclencher une notification toast à partir d’une application de bureau.
title: Envoi d’une notification toast à partir du Bureau
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226780"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Démarrage rapide : envoi d’une notification toast à partir du Bureau

Ce guide de démarrage rapide montre comment déclencher une notification toast à partir d’une application de bureau.

## <a name="prerequisites"></a>Prérequis

-   Bibliothèques
    -   C++ : Runtime. Object. lib
    -   C \# : Windows. Winmd
-   Un raccourci vers votre application, avec un [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), doit être installé sur l’écran d’accueil. Notez, cependant, qu’il n’est pas nécessaire d’épingler à l’écran d’accueil. Pour plus d’informations, consultez [Comment activer les notifications de Toast de bureau par le biais d’une AppUserModelID](enable-desktop-toast-with-appusermodelid.md).
-   une version de Microsoft Visual Studio qui prend en charge au moins Windows 8

## <a name="instructions"></a>Instructions

### <a name="1-create-your-toast-content"></a>1. créer votre contenu Toast

> [!Note]  
> Lorsque vous spécifiez un modèle de Toast qui comprend une image, sachez que les applications de bureau peuvent utiliser uniquement des images locales. les images Web ne sont pas prises en charge. En outre, le chemin d’accès au fichier image local doit être fourni sous la forme d’un chemin d’accès absolu (non relatif).

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a>2. créer et attacher les gestionnaires d’événements

Inscrire des gestionnaires pour les événements Toast : activé, ignoré et échec. Une application de bureau doit au moins s’abonner à l’événement activé pour pouvoir gérer l’activation attendue de l’application à partir du Toast lorsque l’utilisateur la sélectionne.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. envoyer le Toast

> [!IMPORTANT]
> Vous devez inclure la [AppUserModelID](../properties/props-system-appusermodel-id.md) du raccourci de votre application sur l’écran de démarrage chaque fois que vous appelez [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041). Si vous ne le faites pas, votre toast ne s’affichera pas.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. gérer les rappels

Placez la fenêtre de votre application au premier plan si elle reçoit un rappel « activé » de la notification Toast. Lorsqu’un utilisateur sélectionne un toast, l’attente est que l’application est lancée vers une vue relative au contenu de ce Toast.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple d’envoi de notifications toast à partir d’applications de bureau](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Guide pratique pour activer les notifications toast de bureau via un AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[Schéma de Toast XML](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Présentation des notifications Toast](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Démarrage rapide : envoi d’une notification Toast](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Démarrage rapide : envoi d’une notification push Toast](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Instructions et liste de vérification pour les notifications Toast](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Comment choisir et utiliser un modèle de Toast](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Comment gérer l’activation à partir d’une notification Toast](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Comment s’abonner aux notifications Toast](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Choix d’un modèle de Toast](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Options audio Toast](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
