---
description: Spécifie si une Media Foundation transformation (MFT) prend en charge Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: Attribut MF_SA_D3D11_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59a996493ace387d1c6e93c734110772274986c6e5490b9e0e08567024d47c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955399"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>\_ \_ Attribut sensible sa d3d11 MF \_

Spécifie si une Media Foundation transformation (MFT) prend en charge Microsoft Direct3D 11.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique uniquement à la vidéo MFTs. Pour interroger cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs MFT. Si la condition **GetAttributes** est établie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

-   Si l’attribut est différent de zéro, le client peut attribuer à la MFT un pointeur vers l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) avant le démarrage de la diffusion en continu. Pour ce faire, le client envoie le message du [**\_ \_ \_ \_ Gestionnaire D3D du jeu de messages MFT**](mft-message-set-d3d-manager.md) au MFT. Le client n’est pas obligé d’envoyer ce message.
-   Si cet attribut est égal à zéro (**false**), la table MFT ne prend pas en charge Direct3D 11 et le client ne doit pas envoyer le message du [**\_ \_ \_ \_ Gestionnaire D3D de la définition de message MFT**](mft-message-set-d3d-manager.md) à la MFT.

La valeur par défaut de cet attribut est **false**. Traiter cet attribut comme étant en lecture seule. Ne modifiez pas la valeur ; la table MFT ignore toute modification apportée à la valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Prise en charge du décodage vidéo Direct3D 11 dans Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




