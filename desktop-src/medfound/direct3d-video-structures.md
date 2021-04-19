---
description: Décrit les structures utilisées par les interfaces vidéo de Microsoft Direct3D 9.
ms.assetid: 584c087e-53f0-42d8-99ed-a0d013379363
title: Structures vidéo Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ac8e03ff524f7f943c6adbee39b57785112a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530825"
---
# <a name="direct3d-9-video-structures"></a>Structures vidéo Direct3D 9

Décrit les structures utilisées par les interfaces vidéo de Microsoft Direct3D 9.



| Structure                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_OMAC D3D**](d3d-omac.md)<br/> Contient un code d’authentification de message (MAC).<br/>                                                                                                                                                                                                                                                                        |
| [**D3DAES \_ CTR \_ CS**](d3daes-ctr-iv.md)<br/> Contient un vecteur d’initialisation (IV).<br/>                                                                                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ configurer l' \_ entrée**](d3dauthenticatedchannel-configure-input.md)<br/> Contient des données d’entrée pour la méthode [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ configurer la \_ sortie**](d3dauthenticatedchannel-configure-output.md)<br/> Contient la réponse à un appel à la méthode [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md)<br/> Contient des données d’entrée pour une commande [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION**](d3dauthenticatedchannel-configureprotection.md)<br/> Contient des données d’entrée pour une commande de [**\_ protection D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-protection.md) .<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md)<br/> Contient des données d’entrée pour une commande [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) .<br/>                                                                                                           |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**](d3dauthenticatedchannel-configuresharedresource.md)<br/> Contient des données d’entrée pour une commande [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .<br/>                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**](d3dauthenticatedchannel-configureuncompressedencryption.md)<br/> Contient des données d’entrée pour une commande [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .<br/>                                                                   |
| [**\_Indicateurs de protection D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-protection-flags.md)<br/> Spécifie le niveau de protection pour le contenu vidéo.<br/>                                                                                                                                                                                                   |
| [**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)<br/> Contient des données d’entrée pour la méthode [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                                     |
| [**Sortie de la \_ requête D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-output.md)<br/> Contient la réponse à un appel à la méthode [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                        |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYCHANNELTYPE \_**](d3dauthenticatedchannel-querychanneltype-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) .<br/>                                                                                                                     |
| [**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYCRYPTOSESSION \_**](d3dauthenticatedchannel-querycryptosession-input.md)<br/> Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                                |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_**](d3dauthenticatedchannel-querycryptosession-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                             |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_**](d3dauthenticatedchannel-querydevicehandle-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) .<br/>                                                                                                                 |
| [**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID \_**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)<br/> Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                                |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                             |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) .<br/>                                         |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_**](d3dauthenticatedchannel-queryinfobustype-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) .<br/>                                                                                             |
| [**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID \_**](d3dauthenticatedchannel-queryoutputid-input.md)<br/> Contient les données INTPUT pour une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                   |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_**](d3dauthenticatedchannel-queryoutputid-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                 |
| [**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYOUTPUTIDCOUNT \_**](d3dauthenticatedchannel-queryoutputidcount-input.md)<br/> Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                                |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_**](d3dauthenticatedchannel-queryoutputidcount-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                             |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_**](d3dauthenticatedchannel-queryprotection-output.md)<br/> Contient la réponse à une requête de [**\_ protection D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md) .<br/>                                                                                                                         |
| [**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)<br/> Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                        |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                     |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .<br/>                 |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) .<br/>                                             |
| [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md)<br/> Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) .<br/> |
| [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps)<br/> Décrit les fonctionnalités de protection du contenu d’un pilote d’affichage.<br/>                                                                                                                                                                                                                    |
| [**\_Informations sur le bloc D3DENCRYPTED \_**](d3dencrypted-block-info.md)<br/> Spécifie les octets qui sont chiffrés dans une surface vidéo protégée.<br/>                                                                                                                                                                                                                     |
| [**D3DOVERLAYCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3doverlaycaps)<br/> Spécifie les fonctionnalités de la superposition matérielle pour un appareil Direct3D.<br/>                                                                                                                                                                                                                                            |
| [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)<br/> Spécifie une mémoire tampon pour la méthode [**IDirect3DDXVADevice9 :: Execute**](idirect3ddxvadevice9-execute.md) .<br/>                                                                                                                                                                                                  |
| [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)<br/> Spécifie la configuration requise pour les surfaces compressées pour l’accélération vidéo DirectX (DXVA).<br/>                                                                                                                                                                                                         |
| [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)<br/> Spécifie les dimensions et le format de pixel des surfaces non compressées pour le décodage vidéo DXVA.<br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API vidéo Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




