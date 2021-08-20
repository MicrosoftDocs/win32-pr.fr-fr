---
title: Plug-ins sources
description: Plug-ins sources
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows Media Format SDK, plug-ins source
- ASF (Advanced Systems Format), plug-ins source
- ASF (Advanced Systems Format), plug-ins source
- plug-ins sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16d0edc82423a43e50591fa07e14623adc23b94234a28985afca8a496822a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845803"
---
# <a name="source-plug-ins"></a>Plug-ins sources

un plug-in source est une option disponible pour les développeurs qui souhaitent implémenter leur propre système de stockage pour Windows fichiers® Media. Un plug-in source le permet via l’implémentation d’une interface COM appelée **IStream**, qui est une interface standard pour fournir des données.

Le plug-in source doit être écrit en tant que dll et sa présence est connue du kit de développement logiciel (SDK) par le biais d’une entrée de registre. Plusieurs plug-ins sources peuvent être implémentés de cette façon. Le plug-in source doit exporter la fonction [**WMCreateStreamForURL**](wmcreatestreamforurl.md) .

Pour inscrire un plug-in source, l’entrée de Registre suivante doit être ajoutée :

HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows Media \\ WMSDK \\ sources

Name = « n’importe quel nom unique »

Valeur = chemin d’accès de la dll du plug-in source

Une fois la dll inscrite, l’application peut utiliser la méthode **IWMReader :: Open** (avec l’URL appropriée comme paramètre) pour accéder aux données de flux, qui peuvent être stockées dans des fichiers ou des conteneurs de données définis par l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> <dt>

[**WMCreateStreamForURL**](wmcreatestreamforurl.md)
</dt> </dl>

 

 




