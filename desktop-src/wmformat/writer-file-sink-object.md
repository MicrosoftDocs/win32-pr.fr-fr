---
title: Récepteur de fichiers d’auteur, objet
description: Récepteur de fichiers d’auteur, objet
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows Media Format SDK, writer file sink, objets
- ASF (Advanced Systems Format), objets de récepteur de fichiers de writer
- ASF (format de systèmes avancés), objets de récepteur de fichiers de writer
- objets, writer file sink, objets
- objets du récepteur de fichiers du writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404185"
---
# <a name="writer-file-sink-object"></a>Récepteur de fichiers d’auteur, objet

l’objet récepteur de fichiers du writer est utilisé lors de l’écriture Windows sortie multimédia dans un fichier.

L’objet récepteur de fichiers du writer est créé par la fonction [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), qui définit un pointeur vers une interface **IWMWriterFileSink** . Les autres interfaces de l’objet récepteur de fichiers du writer peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet récepteur de fichiers du writer.



| Interface                                          | Description                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Permet à l’application d’afficher des messages d’État à partir de l’objet.                                                                 |
| [**IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | Ouvre un fichier dans lequel l’objet Writer peut écrire des données.                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | Fournit la gestion étendue d’un objet de récepteur de fichiers. Hérite de toutes les méthodes de **IWMWriterFileSink**.                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | Fournit des options supplémentaires pour l’écriture de fichiers. Hérite de toutes les méthodes de **IWMWriterFileSink** et **IWMWriterFileSink2**. |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Alloue de la mémoire, détermine si le récepteur fonctionne en temps réel et gère plusieurs fonctions de rappel.                |



 

L’interface de rappel suivante doit être implémentée par l’application pour suivre la progression d’un objet récepteur de fichiers de writer.



| Interface                                      | Description                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Obligatoire lorsque les informations d’État doivent être communiquées à l’application hôte. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Utilisation des récepteurs d’écriture**](working-with-writer-sinks.md)
</dt> </dl>

 

 




