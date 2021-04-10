---
title: Configuration du compresseur et du décompresseur
description: Configuration du compresseur et du décompresseur
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Gestionnaire de compression vidéo (VCM), configuration des compresseurs
- VCM (gestionnaire de compression vidéo), configuration des compresseurs
- Message ICM_CONFIGURE
- ICQueryConfigure macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939890"
---
# <a name="compressor-and-decompressor-configuration"></a>Configuration du compresseur et du décompresseur

Votre application peut configurer automatiquement le compresseur ou le décompresseur, ou elle peut permettre à l’utilisateur de les configurer. Si cela est possible, autorisez l’utilisateur à configurer le compresseur ou le décompresseur ; Cela vous évite d’avoir à prendre en compte toutes les options pour le compresseur ou le décompresseur.

L’utilisateur peut configurer le compresseur ou le décompresseur à l’aide d’une boîte de dialogue de configuration. Vous pouvez envoyer le message de [**\_ configuration ICM**](icm-configure.md) à VCM (ou utiliser la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) ) pour déterminer si un compresseur ou un décompresseur peut afficher une boîte de dialogue de configuration. Dans ce cas, envoyez le \_ message de configuration ICM (ou utilisez la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) ) pour l’afficher.

Votre application peut envoyer les [**messages \_ GETSTATE**](icm-getstate.md) et [**ICM \_ SETSTATE**](icm-setstate.md) (ou utiliser les macros [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)et [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) ) pour obtenir et définir l’état d’un compresseur ou d’un décompresseur. Si votre application crée ou modifie l’État, elle doit obtenir la disposition des données du compresseur ou du décompresseur avant de restaurer son état. En guise d’alternative, si votre application obtient l’État à partir d’un compresseur ou d’un décompresseur et l’utilise pour restaurer l’État dans une session suivante, elle doit s’assurer qu’elle restaure uniquement les informations d’État obtenues à partir du compresseur ou du décompresseur qu’elle utilise actuellement.

 

 




