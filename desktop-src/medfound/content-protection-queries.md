---
description: 'Répertorie les requêtes pour la méthode IDirect3DAuthenticatedChannel9 :: Query.'
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: Requêtes protection du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5aaa8c43cf722d13550ab4a1860e7a53780e7e82da7f374e28a7f599a22638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829089"
---
# <a name="content-protection-queries"></a>Requêtes protection du contenu

Répertorie les requêtes pour la méthode [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .



| Demande d’État                                                                                                                            | Description                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Retourne le type de bus d’e/s utilisé pour envoyer des données au GPU.                                                                                                   |
| [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md)                                                           | Retourne le type de canal authentifié.                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md)                                                       | Retourne les descripteurs de la session de chiffrement et du périphérique Direct3D associés à un périphérique de décodage DirectX Video Acceleration 2 (DXVA-2) spécifié. |
| [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Retourne le type de chiffrement appliqué avant que le contenu soit accessible au processeur ou au bus.                                                            |
| [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md)                                                         | Retourne un handle vers l’appareil associé à ce canal authentifié.                                                                          |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Retourne l’un des types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.                                     |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Retourne le nombre de types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.                                  |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md)                                                                 | Retourne l’un des identificateurs de sortie qui est associé à une session de chiffrement et un périphérique Direct3D spécifiés.                                        |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md)                                                       | Retourne le nombre d’identificateurs de sortie associés à une session de chiffrement et un périphérique Direct3D spécifiés.                                             |
| [**\_Protection D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md)                                                             | Retourne le niveau de protection actuel de l’appareil.                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Retourne des informations sur un processus autorisé à ouvrir des ressources partagées avec un accès restreint.                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Retourne le nombre de processus autorisés à ouvrir des ressources partagées avec un accès restreint.                                                           |
| [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Retourne le nombre de ressources partagées protégées qui peuvent être ouvertes par n’importe quel processus sans aucune restriction.                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API vidéo Direct3D](direct3d-video-apis.md)
</dt> <dt>

[protection du contenu basé sur GPU](gpu-based-content-protection.md)
</dt> </dl>

 

 



