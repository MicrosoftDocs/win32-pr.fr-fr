---
description: Spécifie comment la session multimédia arrête un objet dans la topologie.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: Attribut MF_TOPONODE_NOSHUTDOWN_ON_REMOVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb7db9a883db80cc6154c72d2c4218b7815456b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412965"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a>\_TOPONODE \_ de mise à l’arrêt MF sur la \_ Suppression de l' \_ attribut

Spécifie comment la session multimédia arrête un objet dans la topologie.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Cet attribut s’applique aux types de nœuds topologie suivants :

-   Nœuds de sortie
-   Tout nœud de transformation qui contient une transformation de Media Foundation *asynchrone* (MFT).

L’attribut peut avoir les valeurs suivantes :




| Valeur | Description | 
|-------|-------------|
| <strong>TRUE</strong> | Lorsque la session multimédia bascule vers une nouvelle topologie ou efface la topologie actuelle, elle n’arrête pas l’objet qui appartient à ce nœud de topologie. | 
| <strong>FALSE</strong> | Lorsque la session multimédia bascule vers une nouvelle topologie ou efface la topologie actuelle, elle arrête l’objet de nœud, comme suit :<ul><li>Nœuds de sortie : la session appelle <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink :: Shutdown</strong></a> sur le récepteur multimédia.</li><li>Nœuds de transformation : la session appelle <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown :: Shutdown</strong></a> sur la MFT.</li></ul> | 




 

La valeur par défaut est **true**.

Si votre application met en file d’attente plusieurs topologies, il est judicieux de définir cet attribut sur **false**. Sinon, les objets de la topologie peuvent ne pas être arrêtés correctement.

Cet attribut ne s’applique pas lorsque l’application arrête la session multimédia en appelant [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Lorsque la session multimédia s’arrête, elle arrête toujours les récepteurs multimédia et les MFTs asynchrones dans la topologie actuelle.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asynchrone](asynchronous-mfts.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




