---
description: La rubrique suivante explique comment effectuer une lecture simple.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Lecture simple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51724b92fea0a46850609e96de85231a9f1df1f7e538f6def4df07442ef19ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118862225"
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

 

 



