---
title: Objet récepteur réseau de l’enregistreur
description: Objet récepteur réseau de l’enregistreur
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows Media Format SDK, writer Network Sink Objects
- ASF (Advanced Systems Format), objets récepteur réseau du writer
- ASF (format des systèmes avancés), objets du récepteur réseau de l’enregistreur
- objets, enregistreur réseau du récepteur
- objets du récepteur réseau du writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2011fd161fc4ac5e1cd03d955f06259e6499e343970cc309b1e8c41db051a32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843724"
---
# <a name="writer-network-sink-object"></a>Objet récepteur réseau de l’enregistreur

L’objet récepteur réseau du writer est utilisé pour écrire des médias numériques sur un réseau.

L’objet récepteur réseau du writer est créé par la fonction [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), qui définit un pointeur vers une interface **IWMWriterNetworkSink** . Les autres interfaces de l’objet récepteur réseau du writer peuvent être obtenues en appelant la méthode **QueryInterface** .



| Interface                                              | Description                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | Collecte des informations sur les clients connectés.                                                                                                                                                                      |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | Récupère des informations sur le client avancé.                                                                                                                                                                          |
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | Permet à l’application d’afficher des messages d’État à partir de l’objet.                                                                                                                                                 |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | Ouvre et ferme les ports, définit et récupère le nombre maximal de clients qui peuvent se connecter à l’objet récepteur, définit le protocole réseau à utiliser par l’objet Writer et effectue d’autres fonctions avancées. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | Alloue de la mémoire, détermine si le récepteur fonctionne en temps réel et gère plusieurs fonctions de rappel.                                                                                                |



 

L’interface de rappel suivante peut être implémentée par l’application pour suivre la progression d’un objet récepteur réseau du writer.



| Interface                                      | Description                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obligatoire lorsque les informations d’État doivent être communiquées à l’application hôte. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Diffusion de données ASF**](broadcasting-asf-data.md)
</dt> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Utilisation des récepteurs d’écriture**](working-with-writer-sinks.md)
</dt> </dl>

 

 




