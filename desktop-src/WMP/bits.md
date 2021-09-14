---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Lecteur Windows Media des magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- type 2 magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- Service de transfert intelligent en arrière-plan (BITS)
- BITS (Service de transfert intelligent en arrière-plan)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855855"
---
# <a name="bits"></a>BITS

le [Service de transfert intelligent en arrière-plan](/windows/desktop/Bits/background-intelligent-transfer-service-portal) est une fonctionnalité du système d’exploitation Windows. BITS transfère les fichiers (téléchargements ou chargements) entre un client et un serveur, et fournit des informations de progression relatives aux transferts. Si vous souhaitez transférer des fichiers à l’aide de code C++, le service BITS est la technologie appropriée à utiliser. si vous souhaitez transférer des fichiers à l’aide d’JScript code dans la page web de votre boutique en ligne, utilisez le gestionnaire de téléchargement à la place.

étant donné que le gestionnaire de téléchargement Lecteur Windows Media utilise BITS, vous pouvez prendre des mesures pour configurer vos travaux de copie BITS de manière à ce que Lecteur Windows Media gère les tâches pour vous. pour ce faire, vous devez suivre la convention décrite dans la section [convention de travail Lecteur Windows Media bits](windows-media-player-bits-job-convention.md) lorsque vous ajoutez vos travaux à la file d’attente de transfert bits. Cette section décrit également un mécanisme permettant de récupérer des informations sur vos travaux BITS à partir de votre page Web de magasins en ligne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du gestionnaire de téléchargement**](using-the-download-manager.md)
</dt> <dt>

[**À propos des magasins en ligne de type 2**](about-type-2-online-stores.md)
</dt> </dl>

 

 