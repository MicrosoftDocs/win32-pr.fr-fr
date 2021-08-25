---
title: Indexeur (objet)
description: Indexeur (objet)
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Media Format SDK, indexer Objects
- ASF (Advanced Systems Format), objets indexer
- ASF (format des systèmes avancés), objets indexer
- objets, indexeurs, objets
- objets indexer
- index, objets indexeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795ef166f6b3ad46897305cbd3f6c38bbc7a219bb99df1dcf8b14dbfb1443577
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839786"
---
# <a name="indexer-object"></a>Indexeur (objet)

L’objet indexeur crée un index dans un fichier ASF. Un index est une partie standard d’un fichier ASF qui correspond à des échantillons de vidéos avec des heures, des numéros de trames ou (le cas échéant) de la société des horodatages standard d’image et de télévision (SMPTE). Sans index, l’objet lecteur et l’objet lecteur synchrone ne peuvent pas Rechercher un point au milieu d’un fichier.

Les index créés par cet objet ne sont nécessaires que si le fichier contient un ou plusieurs flux vidéo. Cela est dû au fait que les données audio ne sont pas compressées temporellement, ce qui permet de trouver facilement un moment donné dans un flux audio.

L’objet indexeur est créé par la fonction [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) , qui définit un pointeur vers une interface **IWMIndexer** . Les autres interfaces de l’objet indexeur peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet indexeur.



| Interface                          | Description                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | Démarre et arrête le processus d’indexation.                                              |
| [**IWMIndexer2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | Configure l’indexeur, en activant l’indexation par Frame, par heure ou par code de temps SMPTE. |



 

L’interface de rappel suivante doit être implémentée par l’application afin d’utiliser l’objet indexeur.



| Interface                                      | Description                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Reçoit des messages d’état des processus qui s’exécutent dans un thread séparé. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> </dl>

 

 




