---
title: WM/MediaClassPrimaryID
description: L’attribut WM/MediaClassPrimaryID contient le GUID de la classe de média principale.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Format Windows Media WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841462"
---
# <a name="wmmediaclassprimaryid"></a>WM/MediaClassPrimaryID

L’attribut **WM/MediaClassPrimaryID** contient le GUID de la classe de média principale.

## <a name="global-constant"></a>Constante globale

\_wszWMMediaClassPrimaryID g

## <a name="data-type"></a>Type de données

**\_GUID du type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut doit être défini sur l’une des valeurs du tableau suivant.



| GUID de la classe principale                     | Description                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | Utilisez pour les fichiers musicaux. N’utilisez pas pour le son qui n’est pas musical. |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | Utilisez pour les fichiers vidéo.                                         |
| "01CD0F29-DA4E-4157-897B-6275D50C4F11" | Utilisez pour les fichiers audio qui ne sont pas musicaux.                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | Utilisez pour les fichiers qui ne sont ni du son ni de la vidéo.               |



 

Lorsque vous spécifiez un identificateur de classe primaire, vous devez également définir un identificateur de classe secondaire pour clarifier le type de contenu dans le fichier.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




