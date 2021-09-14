---
title: Interfaces pour les applications
description: Interfaces pour les applications
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows Gestionnaire de périphériques de média, interfaces d’application
- Gestionnaire de périphériques, interfaces d’application
- applications de bureau, interfaces
- Référence de programmation, interfaces d’application
- référence pour les Gestionnaire de périphériques de média Windows, les interfaces d’application
- plug-ins, interfaces
- interfaces d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49d66272c42679fd38d01b0114a834ee6f33e92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008513"
---
# <a name="interfaces-for-applications"></a>Interfaces pour les applications

cette section décrit les interfaces utilisées ou implémentées par les applications à l’aide du kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques pour communiquer avec les appareils. Le terme « application » utilisé ici signifie un exécutable, un plug-in ou un objet COM existant sur un ordinateur de bureau et nécessitant une communication de haut niveau avec un appareil mobile connecté. il peut s’agir d’une application de lecteur multimédia, d’un plug-in Lecteur Windows Media (si elle a besoin d’un accès direct à un appareil portable) ou d’un objet COM de mesure play-count.

Certaines de ces interfaces sont implémentées par l’application, tandis que d’autres sont appelées par l’application. La documentation de chaque interface indique si elle est implémentée ou appelée (et si elle est implémentée, si elle est facultative ou obligatoire).

Les interfaces ou les classes suivantes sont utilisées par les applications.



| Interface ou classe                                           | Description                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelClient, classe](csecurechannelclient-class.md) | Classe d’assistance qui permet aux applications de s’authentifier, de chiffrer et de déchiffrer des données et de créer des Mac.                                                                                                     |
| [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | interface de Gestionnaire de périphériques de média de haut niveau Windows pour les applications.                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | Étend **IWMDeviceManager** en fournissant des méthodes d’énumération avancées et d’autres méthodes.                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | Étend l’interface **IWMDeviceManager2** en fournissant une méthode qui définit la préférence d’énumération d’appareil.                                                                                                      |
| [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | Fournit des méthodes pour examiner et explorer un seul appareil portable.                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | Étend **IWMDMDevice** en permettant d’obtenir les formats vidéo pris en charge par un appareil, de rechercher un stockage par nom et d’utiliser des pages de propriétés.                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | Étend **IWMDMDevice2** en fournissant des méthodes permettant d’interroger un appareil sur les propriétés, d’envoyer des codes de contrôle d’e/s de périphérique et de fournir des méthodes mises à niveau pour rechercher des stockages et récupérer des fonctionnalités de format de périphérique. |
| [**IWMDMDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | Fournit des méthodes pour le contrôle des appareils.                                                                                                                                                                           |
| [**IWMDMDeviceSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | Améliore l’efficacité des opérations d’appareil en regroupant plusieurs opérations dans une seule session                                                                                                                       |
| [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | Énumère les périphériques portables connectés à un ordinateur.                                                                                                                                                                 |
| [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | Énumère les stockages sur un appareil.                                                                                                                                                                                    |
| [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | Définit et récupère les propriétés de métadonnées (par exemple, artiste, album, genre, etc.) d’un stockage.                                                                                                                      |
| [**IWMDMObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | Obtient et définit des informations qui contrôlent la façon dont les fichiers lisibles sur l’appareil sont gérés par l’interface **IWMDMDeviceControl**                                                                                            |
| [**IWMDMRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | Récupère l’URL à partir de laquelle les composants mis à jour peuvent être téléchargés, si un transfert échoue avec une erreur de révocation.                                                                                                     |
| [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | Fournit des méthodes pour examiner et explorer un stockage (fichier, dossier, sélection) sur un appareil.                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | Étend **IWMDMStorage** en permettant d’obtenir un stockage enfant par nom, et d’obtenir et de définir des attributs étendus.                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | Étend **IWMDMStorage2** en exposant les métadonnées.                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | Étend **IWMDMStorage3** en fournissant des méthodes pour récupérer un sous-ensemble de métadonnées disponibles pour un stockage, et pour définir et récupérer une liste de références à d’autres stockages.                                  |
| [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | Permet d’insérer, de supprimer ou de déplacer des fichiers au sein d’un périphérique, ou entre un appareil et l’ordinateur.                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | Étend **IWMDMStorageControl** en permettant de définir le nom du fichier de destination lors de l’insertion de contenu dans un stockage.                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | Étend **IWMDMStorageControl2** en permettant de passer un pointeur d’interface **IWMDMMetaData** .                                                                                                           |
| [**IWMDMStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | Fournit des méthodes pour récupérer des informations globales sur un support de stockage (par exemple, une carte mémoire flash) sur un appareil.                                                                                                   |
| [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)                   | Permet à une application d’effectuer des mesures de contrôle, de synchronisation des licences et de mise à jour des composants DRM d’un appareil.                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | Étend **IWMDRMDeviceApp** en fournissant une nouvelle version de la méthode **QueryDeviceStatus** .                                                                                                                         |



 

Interfaces de rappel

Les interfaces facultatives suivantes sont implémentées par une application afin d’assurer le suivi de la progression d’une demande asynchrone, telle qu’une demande de lecture ou d’écriture.



| Interface                                      | Description                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | Permet aux applications et aux fournisseurs de services de recevoir des notifications lorsque des appareils ou des stockages en mémoire (tels que des cartes RAM) sont connectés ou déconnectés de l’ordinateur. |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | Étend **IWMDMOperation** en fournissant des méthodes permettant d’obtenir et de définir des attributs étendus.                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | Étend **IWMDMOperation** en fournissant une nouvelle méthode pour le transfert des données non chiffrées pour une efficacité accrue.                                                            |
| [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | Permet à une application de contrôler la façon dont les données sont lues ou écrites sur l’ordinateur lors d’un transfert de fichiers.                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | Étend la méthode **IWMDMProgress :: end** en fournissant un indicateur d’État.                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | Étend **IWMDMProgress2** en fournissant des paramètres d’entrée supplémentaires pour spécifier l’ID d’événement et les informations spécifiques au contexte.                                           |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | Permet à une application de suivre la progression des opérations, telles que la mise en forme des médias ou des transferts de fichiers.                                                                  |



 

Le diagramme suivant illustre la façon dont la plupart des interfaces d’application importantes sont acquises à partir de l’interface **IWMDeviceManager** racine. Une application obtient cette interface racine en cocréant l’objet MediaDevMgr, en demandant l’interface **IComponentAuthenticate** , en authentifiant le composant, puis en demandant le **IWMDeviceManager** (ces étapes sont décrites dans [authentification de l’application](authenticating-the-application.md)). Une fois cette interface racine acquise, [**IWMDeviceManager :: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) est appelé pour créer un objet qui implémente [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). D’autres interfaces sont obtenues en appelant des méthodes sur des interfaces dans l’ordre indiqué. Les interfaces dérivées telles que [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) sont obtenues en appelant **QueryInterface** sur l’interface de base.

Dans le diagramme suivant, les interfaces dérivées sont étiquetées par des barres obliques. par conséquent, « IWMDMStorage/2/3 » indique **IWMDMStorage**, **IWMDMStorage2** et **IWMDMStorage3**.

![Diagramme montrant comment accéder aux principales interfaces d’application dans le gestionnaire de périphériques Windows Media.](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 




