---
description: La rubrique suivante explique comment effectuer une lecture simple.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Lecture simple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523042"
---
# <a name="simple-playback"></a>Lecture simple

La rubrique suivante explique comment effectuer une lecture simple.

**Pour effectuer une lecture simple**

1.  Sélectionnez le terminal de lecture de fichier au niveau de l’appel.
2.  Créez le terminal de lecture sur l’appel TAPI.
3.  Définir les propriétés : le nom et le type de stockage du fichier.
4.  Appelez la méthode [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sur le terminal de lecture de fichier pour démarrer la lecture des flux.

L’exemple de code suivant illustre une lecture simple.

Tout d’abord, utilisez l’interface [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) pour créer le terminal pour l’enregistrement. Cela indique au TSP/MSP d’effectuer la lecture des fichiers sur cet appel. Le TSP/MSP crée un terminal pour l’application à utiliser et le retourne en cas de réussite.


```C++

```



Récupérez le pointeur d’interface [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) à partir de l’interface terminal et utilisez-le pour définir le nom de fichier à lire.


```C++
pMediaPlayback->Release();
```



En supposant que le fichier contienne un flux audio, et que l’appel possède un flux audio de capture, le contenu audio du fichier est lu sur ce flux.

 

 



