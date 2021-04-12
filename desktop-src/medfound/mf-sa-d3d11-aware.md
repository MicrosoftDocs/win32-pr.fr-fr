---
description: Spécifie si une Media Foundation transformation (MFT) prend en charge Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: Attribut MF_SA_D3D11_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318646"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>\_ \_ Attribut sensible sa d3d11 MF \_

Spécifie si une Media Foundation transformation (MFT) prend en charge Microsoft Direct3D 11.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Cet attribut s’applique uniquement à la vidéo MFTs. Pour interroger cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs MFT. Si la condition **GetAttributes** est établie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

-   Si l’attribut est différent de zéro, le client peut attribuer à la MFT un pointeur vers l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) avant le démarrage de la diffusion en continu. Pour ce faire, le client envoie le message du [**\_ \_ \_ \_ Gestionnaire D3D du jeu de messages MFT**](mft-message-set-d3d-manager.md) au MFT. Le client n’est pas obligé d’envoyer ce message.
-   Si cet attribut est égal à zéro (**false**), la table MFT ne prend pas en charge Direct3D 11 et le client ne doit pas envoyer le message du [**\_ \_ \_ \_ Gestionnaire D3D de la définition de message MFT**](mft-message-set-d3d-manager.md) à la MFT.

La valeur par défaut de cet attribut est **false**. Traiter cet attribut comme étant en lecture seule. Ne modifiez pas la valeur ; la table MFT ignore toute modification apportée à la valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Prise en charge du décodage vidéo Direct3D 11 dans Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




