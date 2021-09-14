---
title: Représentation visuelle
description: Un contrôle prend en charge le positionnement et l’affichage lui-même dans son conteneur par le biais d’une technologie de document composite et d’une technologie glisser-déplacer OLE qui implique à la fois le contrôle et son conteneur.
ms.assetid: a7940560-360c-4c0d-9ac1-d051adb0b83e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9711dccbc7aa17f0b4a2ff228b2e2e4421e5083b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095453"
---
# <a name="visual-representation"></a>Représentation visuelle

Un contrôle prend en charge le positionnement et l’affichage lui-même dans son conteneur par le biais d’une technologie de document composite et d’une technologie glisser-déplacer OLE qui implique à la fois le contrôle et son conteneur. Le contrôle doit pouvoir se dessiner lui-même pendant que le conteneur gère la position du contrôle et sa taille.

Les contrôles s’ajoutent aux fonctions de base fournies par les documents OLE. Un contrôle appelle la méthode [**IOleClientSite :: RequestNewObjectLayout**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-requestnewobjectlayout) de son client pour indiquer à son conteneur qu’il souhaite modifier sa taille. Le client appelle [**IOleObject :: GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent) du contrôle pour récupérer la nouvelle taille et appelle [**IOleInPlaceObject :: SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects) pour définir le contrôle sur sa nouvelle taille.

Les contrôles qui prennent en charge uniquement [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) ne prennent pas en charge la mise en cache via [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2) , car le cache requiert la prise en charge de [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage). Toutefois, ces contrôles doivent offrir au client un moyen de restituer le contrôle via [**IDataObject :: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) afin que le client puisse éventuellement créer et gérer son propre cache des données de présentation du contrôle.

Les contrôles utilisent le type HIMETRIC pour ses coordonnées. Toutefois, différents conteneurs peuvent utiliser des systèmes de coordonnées différents. Le conteneur souhaite recevoir des coordonnées dans son propre système, mais le contrôle ne sait pas nécessairement quelles coordonnées son conteneur utilise. Pour communiquer avec succès, le contrôle a besoin d’un moyen de convertir des valeurs en coordonnées de conteneur. Le conteneur fournit un objet site avec la méthode [**IOleControlSite :: TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) . Le contrôle appelle d’abord cette méthode sur le site client de son conteneur pour convertir ses coordonnées en coordonnées appropriées pour le conteneur. Ensuite, il peut passer les coordonnées converties au conteneur.

Les contrôles peuvent appeler [**IOleControlSite :: LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive) dans l’objet site du conteneur pour empêcher le conteneur de tenter de rétrograder le contrôle de l’état actif sur place. Si vous rétrogradez le contrôle de cette manière, le contrôle est désactivé et sa fenêtre détruite. par conséquent, si le contrôle doit conserver sa fenêtre pendant une durée connue, il peut appeler **LockInPlaceActive** pour garantir son état.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ActiveX Commandes](activex-controls.md)
</dt> </dl>

 

 




