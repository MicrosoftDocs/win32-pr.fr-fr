---
title: Configuration de VBR Flux
description: Configuration de VBR Flux
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- flux, configuration des flux VBR
- flux, débit binaire variable (VBR)
- Vitesse de transmission variable (VBR), flux
- VBR (vitesse de transmission variable), flux
- flux, interface IWMPropertyVault
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219588"
---
# <a name="configuring-vbr-streams"></a>Configuration de VBR Flux

Vous pouvez utiliser l’encodage VBR (variable binaire rate) pour produire des flux de haute qualité pour les fichiers locaux ou pour le téléchargement et la diffusion. Il existe trois options pour VBR : basée sur la qualité (une passe), sans contrainte (deux passes) et contraint (deux passes). Pour plus d’informations sur les types d’encodage VBR, consultez l' [encodage VBR (variable bit rate)](variable-bit-rate--vbr--encoding.md).

Vous pouvez configurer l’encodage VBR dans un profil en définissant les propriétés avec l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) . Le tableau suivant décrit les propriétés utilisées pour configurer l’encodage VBR.



| Propriété                     | Description                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| **\_wszVBREnabled g**         | Valeur booléenne. Affectez la valeur true pour utiliser l’encodage VBR.                                                   |
| **\_wszVBRQuality g**         | Valeur **DWORD** . Définissez le niveau de qualité souhaité (de 1 à 100) pour l’encodage VBR basé sur la qualité.      |
| **\_wszVBRBitrateMax g**      | Valeur **DWORD** . Définissez sur la vitesse de transmission maximale, en bits par seconde, pour l’encodage VBR limité.   |
| **\_wszVBRBufferWindowMax g** | Valeur **DWORD** . Défini sur la fenêtre de mémoire tampon maximale, en millisecondes, pour l’encodage VBR limité. |



 

Les sections suivantes décrivent comment utiliser les différents types de codage à vitesse de transmission variable.



| Section                                                              | Description                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Pour configurer Quality-Based VBR](to-configure-quality-based-vbr.md) | Décrit comment utiliser un encodage à débit binaire variable basé sur un niveau de qualité statique.                                   |
| [Pour configurer le VBR sans contrainte](to-configure-unconstrained-vbr.md) | Décrit comment utiliser un encodage à débit binaire variable basé sur un taux de bits moyen cible sans valeur de pic explicite. |
| [Pour configurer le VBR restreint](to-configure-constrained-vbr.md)     | Décrit comment utiliser un encodage à débit binaire variable basé sur une vitesse de transmission moyenne cible et une valeur de pic explicite.     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de Flux**](configuring-streams.md)
</dt> </dl>

 

 




