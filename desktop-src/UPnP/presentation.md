---
title: Présentation
description: La présentation est la dernière étape du processus UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92f8457a881dc0414713e996d230261330c10911f2aea285a2e365ad0d59320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137192"
---
# <a name="presentation"></a>Présentation

La présentation est la dernière étape du processus UPnP. Si un appareil possède une URL pour la présentation, un point de contrôle peut récupérer une page à partir de cette URL et charger la page dans un navigateur. Selon les fonctionnalités de la page de présentation et de l’appareil, le point de contrôle peut contrôler l’appareil et afficher l’état de l’appareil.

Le chemin d’accès de la ressource, qui est transmis à [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) pendant l’inscription, est l’emplacement où se trouvent tous les fichiers pertinents pour la présentation de l’appareil. Les développeurs d’appareils peuvent fournir des pages distinctes pour chaque appareil intégré. L’URL de présentation dans le modèle de description de l’appareil peut être une URL absolue ou une URL relative. Pour les URL relatives, qui sont relatives au chemin d’accès de la ressource, le modèle de description de l’appareil doit contenir un nom de fichier. **IUPnPRegistrar** convertit ce en URL avec l’emplacement réel. Pour les URL absolues, l’emplacement n’est pas modifié.

Pour prendre en charge les scripts côté client dans une page de présentation, des informations supplémentaires sont généralement ajoutées à l’URL sous la forme d’une « chaîne de requête ». Les informations supplémentaires ajoutées sont l’URL du document de description de l’appareil, ainsi que le UDN de l’appareil ou de l’appareil intégré. L’URL de description de l’appareil peut être utilisée pour charger un document de description dans le script, puis contrôler l’appareil par le biais de ses services. Le UDN est utilisé pour sélectionner un appareil intégré à partir de l’appareil racine.

Le format de l’URL de présentation modifiée est : l’URL de présentation réelle, un point d’interrogation («  ? »), l’URL de description de l’appareil, un signe plus (« + »), le UDN d’appareil. Le point d’interrogation indique le début de la chaîne de requête.

Si l’URL de présentation dans le modèle de description de périphérique était une URL absolue et qu’elle contenait déjà un point d’interrogation («  ? »), les informations supplémentaires ne sont pas ajoutées à l’URL de présentation.



| Description                        | URL                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Dans le modèle de description de l’appareil | **presentationURL** MyDevice.html **/presentationURL**                                                                                              |
| Généré par l’hôte d’appareil       | **presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ... + UDN **/presentationURL** |



 

Un script côté client peut avoir besoin d’extraire l’URL de description de l’appareil à partir de l’URL de présentation pour charger l’objet [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . Pour ce faire, prenez la chaîne de requête et terminez-la au signe plus (« + »).


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



Dans le cas d’une page de présentation pour un appareil intégré, des tâches supplémentaires sont nécessaires. Après avoir chargé le [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), le script doit obtenir la collection de périphériques intégrés, puis sélectionner l’appareil qui correspond au UDN dans la chaîne de requête. Le script suivant montre comment sélectionner l’appareil intégré pour la page de présentation actuelle. Il suppose que LightDesc est déjà chargé.


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




