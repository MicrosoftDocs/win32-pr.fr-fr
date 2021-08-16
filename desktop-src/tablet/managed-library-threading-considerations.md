---
description: Les considérations suivantes relatives au thread de Tablet PC sont spécifiques à la bibliothèque managée.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Considérations sur les threads de bibliothèque managée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60908618fe3b566a552167f3448ee1d4269f9246c7b08f9bb1acf3269cf2ae77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031707"
---
# <a name="managed-library-threading-considerations"></a>Considérations sur les threads de bibliothèque managée

Les considérations suivantes relatives au thread de Tablet PC sont spécifiques à la bibliothèque managée.

-   [Sécurité des threads](#thread-safety)
-   [Applications STA et MTA](#sta-and-mta-applications)
-   [Windows Considérations sur les threads de formulaires](#windows-forms-threading-considerations)
-   [Considérations sur le presse-papiers](#clipboard-considerations)
-   [Exceptions dans les gestionnaires d’événements](#exceptions-within-event-handlers)
-   [Suppression d’objets et de contrôles](#disposing-objects-and-controls)
-   [API StylusInput](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

Les classes de la bibliothèque managée de la plateforme Tablet PC ne sont généralement pas thread-safe. Les collections suivantes sont thread-safe au niveau du membre ; Toutefois, ces collections ne garantissent pas qu’un énumérateur est protégé si un autre thread opère simultanément sur la collection :

-   [CursorButtons](/previous-versions/ms839506(v=msdn.10))
-   [Curseurs](/previous-versions/ms839493(v=msdn.10))
-   [DivisionUnits](/previous-versions/ms837954(v=msdn.10))
-   [RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))
-   [Modules de reconnaissance](/previous-versions/ms828520(v=msdn.10))
-   [Tablettes](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>Applications STA et MTA

les applications managées créées à l’aide des assistants contenus dans Microsoft Visual Studio .net sont des threads cloisonnés (STA) par défaut. Vous pouvez modifier le cloisonnement de votre application en définissant le thread STA ou l’attribut de thread du cloisonnement multithread (MTA) sur le point d’entrée de votre application.

Si votre application s’exécute dans un MTA, vous devez écrire du code thread-safe. Toutefois, en procédant ainsi, vous pouvez améliorer certains problèmes de performances de gestion des événements.

Pour plus d’informations sur les attributs du thread STA et du thread MTA, consultez la classe [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) et la classe [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) .

## <a name="windows-forms-threading-considerations"></a>Windows Considérations sur les threads de formulaires

les contrôles [InkPicture](/previous-versions/aa514604(v=msdn.10)) et [InkEdit](/previous-versions/ms552265(v=vs.100)) étendent Windows Forms contrôles. Windows les contrôles forms utilisent le modèle sta (single-threaded apartment), car les Windows Forms sont basés sur des fenêtres Win32 natives qui sont intrinsèquement des threads uniques. Dans le code managé, les contrôles d’encre doivent être créés dans le même thread que le thread principal pour le formulaire.

Dans une application STA, certains événements se produisent sur un thread autre que le thread d’interface utilisateur de l’application. lors de l’appel d’un objet ou d’un contrôle Windows Forms, y compris les contrôles [InkPicture](/previous-versions/aa514604(v=msdn.10)) et [InkEdit](/previous-versions/ms552265(v=vs.100)) , à partir d’un gestionnaire d’événements Tablet PC, utilisez la méthode [control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) héritée de l’objet ou du contrôle. La propriété [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , héritée de la classe Control, peut être utilisée pour déterminer si cela est nécessaire.

Par exemple, dans le gestionnaire d’événements suivant pour l’événement de [reconnaissance](/previous-versions/ms829424(v=msdn.10)) , la propriété [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) est testée et, si la **valeur est true**, le gestionnaire d’événements est à nouveau appelé à partir du thread d’interface utilisateur.


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



Si vous placez un [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) sur awebpagein un navigateur (consultez [contrôles Web](web-controls.md)), il s’exécute en tant qu’application STA. Pour les applications Smart client (voir [aucun déploiement Touch](no-touch-deployment.md)), le développeur a un contrôle total sur le [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1). (La valeur par défaut est généralement STA, mais peut être MTA, en fonction de votre version de CLR.) Pour les problèmes de Threading impliquant l' [**RealTimeStylus**](realtimestylus-class.md), consultez [Considérations sur les threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

pour plus d’informations sur l’appel d’Windows Forms à partir d’une application MTA, consultez [exemple de contrôle multithread Windows Forms](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).

## <a name="clipboard-considerations"></a>Considérations sur le presse-papiers

L’objet [Clipboard](../dataxchg/clipboard.md) ne fonctionne qu’à partir d’un thread STA. Lors d’une tentative de copie ou de collage à partir du presse-papiers à partir d’un thread qui n’est pas STA, vous recevez un [ThreadStateException](/previous-versions/windows/). Si votre application est MTA, créez un thread STA pour gérer les appels de méthode du presse-papiers et certains des autres aspects de l’interface utilisateur de votre application.

## <a name="exceptions-within-event-handlers"></a>Exceptions dans les gestionnaires d’événements

Les exceptions ne peuvent pas être levées à partir des gestionnaires d’événements Tablet PC. Par exemple, si un délégué de gestionnaire d’événements pour un objet ou une collection Tablet PC a trois gestionnaires inscrits et que le premier lève une exception, la séquence suivante se produit :

1.  Le premier gestionnaire se termine.
2.  L’exception est perdue.
3.  Les gestionnaires restants ne sont pas appelés.

## <a name="disposing-objects-and-controls"></a>Suppression d’objets et de contrôles

Pour éviter une fuite de mémoire, vous devez appeler explicitement la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) sur tout objet ou contrôle Tablet PC auquel un gestionnaire d’événements a été attaché avant que l’objet ou le contrôle ne soit hors de portée.

Pour améliorer les performances de votre application, supprimez manuellement tout objet ou contrôle Tablet PC qui implémente la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) lorsque l’objet ou le contrôle n’est plus nécessaire.

## <a name="stylusinput-apis"></a>API StylusInput

Pour plus d’informations sur les considérations relatives aux threads pour l’objet [**RealTimeStylus**](realtimestylus-class.md) et les interfaces de programmation d’applications (API) StylusInput, consultez [Considérations sur les threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

 

 
