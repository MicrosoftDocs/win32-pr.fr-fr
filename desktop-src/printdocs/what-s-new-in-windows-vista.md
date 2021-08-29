---
description: répertorie les interfaces de programmation d’applications (api) d’impression introduites dans Windows Vista.
ms.assetid: 7a4eb5d7-b37d-4090-aea4-7274daa1e15c
title: nouveautés pour l’impression dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da41943d56f4cc49a6264c741519ef3a991925f3e3cfc61c154570499ce7b5a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600269"
---
# <a name="whats-new-for-printing-in-windows-vista"></a>nouveautés pour l’impression dans Windows Vista

répertorie les interfaces de programmation d’applications (api) d’impression introduites dans Windows Vista.

Les fonctions et énumérations suivantes sont utilisées pour gérer les tickets d’impression.



| Fonction                                                               | Description                                                                                                                                   | En-tête    | Bibliothèque     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------|-------------|
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) | Convertit un ticket d’impression en une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .                                                                            | Prntvpt. h | Prntvpt. lib |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) | Convertit un [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un ticket d’impression.                                                                                      | Prntvpt. h | Prntvpt. lib |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)                             | Libère les mémoires tampons créées par certaines fonctions de gestion des tickets d’impression.                                                                        | Prntvpt. h | Prntvpt. lib |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) | Valide et fusionne deux tickets d’impression dans un ticket d’impression viable.                                                                            | Prntvpt. h | Prntvpt. lib |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)               | Obtient un compte des fonctionnalités de l’imprimante.                                                                                                | Prntvpt. h | Prntvpt. lib |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)                               | Ouvre un fournisseur de tickets d’impression.                                                                                                                | Prntvpt. h | Prntvpt. lib |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)                           | Ouvre un fournisseur de tickets d’impression, même s’il ne prend pas en charge la version par défaut du [schéma d’impression](./print-schema.md). | Prntvpt. h | Prntvpt. lib |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)                             | Ferme un fournisseur de tickets d’impression.                                                                                                               | Prntvpt. h | Prntvpt. lib |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)     | Obtient la dernière version du [schéma d’impression](./print-schema.md) qu’une imprimante spécifiée prend en charge.                        | Prntvpt. h | Prntvpt. lib |



 



| Énumération                                        | Description                                                                                                                                                                               | En-tête    |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) | Permet aux appelants de spécifier quel [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) est utilisé comme source de valeurs par défaut lorsqu’un ticket d’impression ne spécifie pas tous les paramètres qui peuvent être dans une **DEVMODE**. | Prntvpt. h |
| [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope)     | Spécifie l’étendue d’un ticket d’impression.                                                                                                                                                    | Prntvpt. h |



 

Les fonctions suivantes sont utilisées pour installer des pilotes d’imprimante.



| Fonction                                                                   | Description                                                                                                                                                                 | En-tête     | Bibliothèque      |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CorePrinterDriverInstalled**](coreprinterdriverinstalled.md)           | Indique si un pilote d’imprimante principal avec un GUID, une date et une version spécifiés est installé.                                                                                | Winspool. h | Winspool. lib |
| [**DeletePrinterDriverPackage**](deleteprinterdriverpackage.md)           | Supprime un package de pilotes d’imprimante du magasin de pilotes.                                                                                                                     | Winspool. h | Winspool. lib |
| [**GetCorePrinterDrivers**](getcoreprinterdrivers.md)                     | Obtient le GUID, la version et la date des pilotes d’imprimante principaux spécifiés et le chemin d’accès à leurs packages.                                                                      | Winspool. h | Winspool. lib |
| [**GetPrinterDriverPackagePath**](getprinterdriverpackagepath.md)         | Obtient le chemin d’accès au package de pilotes d’imprimante spécifié sur un serveur d’impression.                                                                                                    | Winspool. h | Winspool. lib |
| [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) | Installe un pilote d’imprimante à partir d’un package de pilotes dans le magasin de pilotes du serveur d’impression.                                                                                         | Winspool. h | Winspool. lib |
| [**UploadPrinterDriverPackage**](uploadprinterdriverpackage.md)           | Charge un pilote d’imprimante dans le magasin de pilotes d’un serveur d’impression afin qu’il puisse être installé avec [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md). | Winspool. h | Winspool. lib |



 

Les fonctions, énumérations et structures suivantes sont utilisées pour l’impression et la gestion des imprimantes et des connexions d’imprimante.



| Fonction                                               | Description                                                                                                                                              | En-tête     | Bibliothèque      |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**AddPrinterConnection2**](addprinterconnection2.md) | Ajoute une connexion à l’imprimante spécifiée pour l’utilisateur actuel.                                                                                         | Winspool. h | Winspool. lib |
| [**OpenPrinter2**](openprinter2.md)                   | Récupère un handle vers l’imprimante ou le serveur d’impression spécifié ou d’autres types de handles dans le sous-système d’impression, tout en définissant certaines options d’imprimante. | Winspool. h | Winspool. lib |



 



| Énumération                                            | Description                                                                                       | En-tête     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------|------------|
| [**\_indicateurs d’option d’imprimante \_**](printer-option-flags.md) | Spécifie la mise en cache d’un handle pour une imprimante ouverte avec [**OpenPrinter2**](openprinter2.md). | Winspool. h |



 



| Structure                                                         | Description                                                                            | En-tête     |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------|
| [**\_pilote d’imprimante principal \_**](core-printer-driver.md)              | Représente un pilote d’imprimante dont dépendent d’autres pilotes d’imprimante.              | Winspool. h |
| [**\_Informations sur le pilote \_ 8**](driver-info-8.md)                          | Représente un pilote d’imprimante.                                                           | Winspool. h |
| [**Informations de formulaire \_ \_ 2**](form-info-2.md)                              | Représente des informations sur un formulaire d’impression localisable.                                 | Winspool. h |
| [**\_Informations sur le travail \_ 4**](job-info-4.md)                                | Représente un jeu complet de valeurs associées à un travail et prend en charge les fichiers de mise en file d’attente 64 bits. | Winspool. h |
| [**Informations de connexion d’imprimante \_ \_ \_ 1**](printer-connection-info-1.md) | Représente des informations sur une connexion à une imprimante.                                | Winspool. h |
| [**OPTIONS de l’imprimante \_**](printer-options.md)                       | Représente les options de l’imprimante.                                                            | Winspool. h |
| [**PRINTPROCESSOR \_ Cap \_ 2**](printprocessor-caps-2.md)          | Représente des informations sur les fonctionnalités de l’imprimante.                                             | Winspool. h |



 

Les fonctions, énumérations et interfaces suivantes sont utilisées pour implémenter un nouveau système de notification d’impression asynchrone.



| Fonction                                                                             | Description                                                                                                                                                                                       | En-tête     | Bibliothèque      |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)               | Crée un canal de communication entre le composant d’impression hébergé par le spouleur, tel qu’un pilote d’impression ou un moniteur de port, et une application qui doit recevoir des notifications du composant. | Prnasnot. h | Winspool. lib |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)     | Inscrit une application pour recevoir des notifications de composants hébergés par le spouleur, tels que des pilotes d’imprimante, des processeurs d’impression et des moniteurs de port.                                                    | Prnasnot. h | Winspool. lib |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications) | Permet à une application qui s’est inscrite de recevoir des notifications des composants d’impression hébergés par le spouleur de mettre fin à son abonnement aux notifications.                                         | Prnasnot. h | Winspool. lib |



 



| Énumération                                                                    | Description                                                                                                                                                                                                          | En-tête     |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| [**PrintAsyncNotifyConversationStyle**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle) | Spécifie si la communication entre les applications et les composants hébergés par le spouleur d’impression, tels que les pilotes d’imprimante, les processeurs d’impression et les moniteurs de port, est bidirectionnelle ou unidirectionnelle.                          | Prnasnot. h |
| [**PrintAsyncNotifyError**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)                         | Spécifie une erreur dans une transaction de notification asynchrone.                                                                                                                                                      | Prnasnot. h |
| [**PrintAsyncNotifyUserFilter**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)               | Spécifie si les notifications sont envoyées uniquement aux applications d’écoute associées au même utilisateur que l’expéditeur hébergé par le spouleur d’impression ou qu’elles accèdent à un ensemble plus étendu d’applications d’écoute. | Prnasnot. h |



 



| Interface et méthode                                                                                                      | Description                                                                                                                                                   | En-tête     | Bibliothèque      |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**IPrintAsyncNotifyCallback::ChannelClosed**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-channelclosed)    | Utilisé par un membre d’un canal de communication pour informer l’autre membre que le canal est en cours de fermeture.                                                    | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyCallback::OnEventNotify**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-oneventnotify)    | Appelé par le spouleur d’impression pour avertir un écouteur qu’une notification est disponible sur un canal spécifié.                                                      | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyChannel::CloseChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel)         | Ferme un canal de communication.                                                                                                                               | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyChannel :: SendNotification**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification) | Envoie une notification à partir d’un composant hébergé par le spouleur d’impression vers une ou plusieurs applications d’écoute, ou renvoie une réponse d’une application à un composant. | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyDataObject::AcquireData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata)  | Les points écoutent les applications dans les données de notification, ainsi que la taille et le type des données.                                                                   | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyDataObject::ReleaseData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata)  | Libère la mémoire utilisée par les données encapsulées dans le [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject).                                  | Prnasnot. h | Winspool. lib |



 

L’énumération et les structures suivantes sont utilisées pour appeler Microsoft XPS Document Converter (MXDC) qui écrit des documents XPS (XML Paper Specification) sur un appareil ou un fichier.



| Énumération                                | Description                                                            | En-tête |
|--------------------------------------------|------------------------------------------------------------------------|--------|
| [**MxdcS0PageEnums**](mxdcs0pageenums.md) | Spécifie les types de ressources, tels que les polices ou les images, sur une page XPS. | Mxdc. h |



 



| Structure                                                          | Description                                                                                                                                    | En-tête |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| [**MxdcEscapeHeader**](mxdcescapeheader.md)                       | Représente une instruction au MXDC.                                                                                                         | Mxdc. h |
| [**MxdcGetFileNameData**](mxdcgetfilenamedata.md)                 | Représente le chemin d’accès complet et le nom d’un fichier de sortie MXDC.                                                                                     | Mxdc. h |
| [**MxdcPrintTicketEscape**](mxdcprintticketescape.md)             | Représente une combinaison de [**MxdcEscapeHeader**](mxdcescapeheader.md) et [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md). | Mxdc. h |
| [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)   | Représente un ticket d’impression qui sera associé à un document XPS.                                                                        | Mxdc. h |
| [**MxdcS0PageData**](mxdcs0pagedata.md)                           | Représente une page au format XPS à passer au fichier de sortie MXDC sans aucun traitement.                                                  | Mxdc. h |
| [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) | Représente une combinaison de [**MxdcEscapeHeader**](mxdcescapeheader.md) et [**MxdcS0PageData**](mxdcs0pagedata.md).                         | Mxdc. h |
| [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md)       | Représente une combinaison de [**MxdcEscapeHeader**](mxdcescapeheader.md) et [**MxdcS0PageResource**](mxdcs0pageresourceescape.md).           | Mxdc. h |
| [**MxdcS0PageResource**](mxdcs0pageresourceescape.md)             | Représente une ressource, telle qu’une police ou une image, qui est incluse dans une page XPS par le MXDC.                                                   | Mxdc. h |



 

 

 
