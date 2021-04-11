---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Windows Media Player Online stores, Service de transfert intelligent en arrière-plan (BITS)
- magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- type 2 magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- Service de transfert intelligent en arrière-plan (BITS)
- BITS (Service de transfert intelligent en arrière-plan)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315473"
---
# <a name="bits"></a>BITS

Le [service de transfert intelligent en arrière-plan](/windows/desktop/Bits/background-intelligent-transfer-service-portal) est une fonctionnalité du système d’exploitation Windows. BITS transfère les fichiers (téléchargements ou chargements) entre un client et un serveur, et fournit des informations de progression relatives aux transferts. Si vous souhaitez transférer des fichiers à l’aide de code C++, le service BITS est la technologie appropriée à utiliser. Si vous souhaitez transférer des fichiers à l’aide du code JScript dans votre page Web de boutique en ligne, utilisez le gestionnaire de téléchargement à la place.

Étant donné que le gestionnaire de téléchargement du lecteur Windows Media utilise le service BITS, vous pouvez prendre les mesures nécessaires pour configurer vos travaux de copie BITS de telle sorte que le lecteur Windows Media gère les tâches pour vous. Pour ce faire, vous devez suivre la convention décrite dans la section [Convention du travail bits du lecteur Windows Media](windows-media-player-bits-job-convention.md) lorsque vous ajoutez vos travaux à la file d’attente de transfert bits. Cette section décrit également un mécanisme permettant de récupérer des informations sur vos travaux BITS à partir de votre page Web de magasins en ligne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du gestionnaire de téléchargement**](using-the-download-manager.md)
</dt> <dt>

[**À propos des magasins en ligne de type 2**](about-type-2-online-stores.md)
</dt> </dl>

 

 