---
title: Interface IWMPMetadataPicture (VB et C) (WMP. h)
description: Fournit des propriétés pour obtenir des informations sur l’image contenue dans un fichier multimédia numérique qui est représenté par un attribut WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB et C) interface Windows Media Player
- Interface IWMPMetadataPicture (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541681"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>Interface IWMPMetadataPicture (VB et C#)

Fournit des propriétés pour obtenir des informations sur l’image contenue dans un fichier multimédia numérique représenté par un attribut de métadonnées [**WM/Picture**](/windows/desktop/wmformat/wmpicture). Cet attribut correspond aux images de la pochette d’album contenues dans un fichier multimédia numérique, et non à une pochette d’album téléchargée sur Internet.

L’interface **IWMPMetadataPicture** expose les propriétés suivantes.



| Propriété                                                                                   | Description                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Description**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | Obtient la description de l’image représentée par l’attribut de métadonnées.  |
| [**mimeType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | Obtient le type MIME de l’image représentée par l’attribut de métadonnées.    |
| [**Picture**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | Obtient le type d’image de l’image représentée par l’attribut de métadonnées. |
| [**URL**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | À usage interne uniquement                                                        |



 

Récupérez une interface **IWMPMetadataPicture** en passant le nom d’attribut [**WM/Picture**](/windows/desktop/wmformat/wmpicture) à la méthode suivante et en effectuant un cast de l’objet retourné.



| Interface                                  | Propriété                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>Membres

L’interface **IWMPMetadataPicture (VB et C#)** ne définit aucun membre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

