---
description: Spécifie si une mémoire tampon contient le début d’un paquet ASF (Advanced Systems Format).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: Attribut MFASFSPLITTER_PACKET_BOUNDARY (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313846"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>MFASFSPLITTER \_ attribut de limite de paquet \_

Spécifie si une mémoire tampon contient le début d’un paquet ASF (Advanced Systems Format).

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Si une mémoire tampon de média expose l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) via **QueryInterface** et que la valeur de cet attribut est différente de zéro, le séparateur ASF traite la mémoire tampon comme le début d’un nouveau paquet.

Cet attribut s’applique si vous utilisez le séparateur ASF pour analyser les données ASF. Si vos données ASF ont des longueurs de paquets variables, vous devez définir cet attribut sur les mémoires tampons de média que vous transmettez à la méthode [**IMFASFSplitter ::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . Affectez la **valeur true** à l’attribut si la mémoire tampon contient le début d’un nouveau paquet. Si la mémoire tampon contient une continuation du paquet précédent, affectez la valeur **false** à l’attribut. Les mémoires tampons ne peuvent pas couvrir plusieurs paquets.

Pour les données ASF avec des tailles de paquets fixes, cet attribut n’est pas obligatoire et une mémoire tampon peut s’étendre sur plusieurs paquets.

Notez que les implémentations standard du [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) fournies par Media Foundation n’exposent pas [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes). Pour utiliser cet attribut, vous devez fournir votre propre implémentation de **IMFMediaBuffer**; par exemple, en encapsulant les mémoires tampons retournées par [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




