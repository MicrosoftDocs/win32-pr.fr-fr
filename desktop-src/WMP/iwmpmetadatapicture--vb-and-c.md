---
title: interface IWMPMetadataPicture (VB et C) (Wmp. h)
description: Fournit des propriétés pour obtenir des informations sur l’image contenue dans un fichier multimédia numérique qui est représenté par un attribut WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- interface IWMPMetadataPicture (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPMetadataPicture (VB et C), description
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311110"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>interface IWMPMetadataPicture (VB et C#)

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

l’interface **IWMPMetadataPicture (VB et C#)** ne définit aucun membre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

