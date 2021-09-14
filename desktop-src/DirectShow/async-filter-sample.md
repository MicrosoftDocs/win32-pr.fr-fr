---
description: Exemple de filtre Async
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Exemple de filtre Async
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112190"
---
# <a name="async-filter-sample"></a>Exemple de filtre Async

## <a name="description"></a>Description

L’exemple de filtre Async est un filtre de lecteur de fichier qui prend en charge le téléchargement progressif. Cet exemple de filtre implémente les interfaces [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) et [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) . Il prend en charge les fichiers MPEG, mais pas les fichiers AVI.

## <a name="usage"></a>Usage

Cet exemple comprend une petite application en ligne de commande, Memfile.exe, qui illustre le filtre. Les arguments de ligne de commande spécifient un fichier multimédia et une vitesse de transmission, en kilo-octets par seconde. L’application lit le fichier en mémoire à la vitesse spécifiée et lit le fichier. Pour ce faire, il crée une instance du filtre, ajoute le filtre au graphique de filtre et restitue la broche de sortie du filtre.

Sur la ligne de commande, tapez :

**Débit binaire de nom de fichier Memfile**  

Le filtre d’exemple Async ne prend pas en charge les fichiers AVI, car il ne peut pas se connecter au filtre de [fractionnement AVI](avi-splitter-filter.md) . La broche de sortie du filtre Async propose un flux de MEDIATYPE \_ et MEDIASUBTYPE \_ null pour le type de média. La broche d’entrée sur le filtre de séparateur AVI n’accepte pas la \_ valeur null MEDIASUBTYPE et ne propose pas de types propres. Par conséquent, la connexion du code confidentiel échoue. Le filtre asynchrone peut être amélioré pour proposer MEDIASUBTYPE \_ AVI le cas échéant. Par exemple, il peut examiner le format de fichier ou utiliser l’extension de fichier.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

cet exemple est installé sous le chemin d’accès suivant : \[ exemples *racine du kit de développement logiciel (SDK)* \] \\ \\ \\ DirectShow \\ filtres \\ asynchrones.

## <a name="related-topics"></a>Rubriques connexes



[DirectShow Extraits](directshow-samples.md)


 

 



