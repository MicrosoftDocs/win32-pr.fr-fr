---
title: Objet récepteur push de l’enregistreur
description: Objet récepteur push de l’enregistreur
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Media Format SDK, writer, objets récepteurs Push
- ASF (Advanced Systems Format), objets récepteurs push de l’enregistreur
- ASF (format des systèmes avancés), objets récepteurs push de l’enregistreur
- objets, rédacteurs, objets récepteurs Push
- objets de récepteur push du writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859e4d2d5cf2530e655b74705b1d6f9ef93960d28f523c00e0da7a7336ab258d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006329"
---
# <a name="writer-push-sink-object"></a>Objet récepteur push de l’enregistreur

L’objet récepteur push du writer distribue les médias numériques aux points de publication. Par exemple, un concert en direct peut être encodé par un serveur unique, puis remis, ou *poussé*, à plusieurs autres serveurs qui diffusent en réalité le contenu aux utilisateurs.

Un objet récepteur push du writer est créé par la fonction [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), qui définit un pointeur vers une interface **IWMWriterPushSink** . Les autres interfaces prises en charge par l’objet, énumérées dans le tableau suivant, peuvent être obtenues en appelant la méthode **QueryInterface** .



| Interface                                          | Description                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permet à l’application d’afficher des messages d’État à partir de l’objet.                                                  |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | Gère une session de distribution push.                                                                             |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Alloue de la mémoire, détermine si le récepteur fonctionne en temps réel et expose plusieurs fonctions de rappel. |



 

L’interface de rappel suivante peut être implémentée par l’application pour suivre la progression d’un objet récepteur push de l’enregistreur.



| Interface                                      | Description                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obligatoire lorsque les informations d’État doivent être communiquées à l’application hôte. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Envoi de données ASF à un point de publication**](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[**Utilisation des récepteurs d’écriture**](working-with-writer-sinks.md)
</dt> </dl>

 

 




