---
title: Vitesse de transmission
description: Vitesse de transmission
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Media Format SDK, vitesses de bits
- ASF (Advanced Systems Format), vitesses de transmission
- ASF (format des systèmes avancés), vitesses de transmission
- vitesses de transmission, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a15332e18d47a72974098ad38c6a942ceaf4780e1b79dffacd49382e3416ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809869"
---
# <a name="bit-rate"></a>Vitesse de transmission

La vitesse de transmission fait référence à la quantité de données par seconde qui est fournie à partir d’un fichier ASF. Les mesures de la vitesse de transmission sont exprimées en bits par seconde (BPS) ou en kilobits par seconde (Kbits/s). La vitesse de transmission est souvent confondue avec la bande passante, qui est une mesure de la capacité de transfert de données d’un réseau. La bande passante est également mesurée en BPS et en Kbits/s.

le kit de développement logiciel (SDK) de Format de média Windows peut être utilisé pour créer des applications qui diffusent du contenu multimédia Windows en continu à partir d’emplacements Internet ou intranet. Lorsque vous diffusez des données sur un réseau ou sur Internet, le taux d’échantillonnage revêt une importance vitale pour l’expérience de l’utilisateur final. Si la bande passante disponible sur le réseau est inférieure à la vitesse de transmission du fichier ASF, la lecture du fichier sera interrompue d’une certaine manière. En règle générale, une bande passante insuffisante entraîne l’omission des exemples ou la suspension de la lecture, tandis que davantage de données sont mises en mémoire tampon.

Chaque fichier ASF reçoit une valeur de vitesse de transmission au moment de la création, en fonction du type et du nombre de flux inclus dans le profil utilisé. Les flux individuels ont leurs propres vitesses de transmission. Les vitesses de transmission peuvent être constantes (les données d’origine sont compressées de façon à conserver un flot constant de données à approximativement la même vitesse) ou variable (les données d’origine sont compressées de façon à conserver la même qualité dans tout, même si cela peut entraîner un flot de données inégal). Différents types de taux de bits peuvent être appliqués à différents flux dans le même fichier.

Vous pouvez encoder le même contenu dans plusieurs flux différents, chacun avec une vitesse de transmission différente. Vous pouvez ensuite configurer les flux afin qu’ils s’excluent mutuellement. Cela vous permet de créer un fichier unique qui peut être transmis en continu aux utilisateurs avec des bandes passantes différentes. Cette fonctionnalité est appelée débit binaire multiple, ou MBR.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](concepts.md)
</dt> <dt>

[**Encodage à débit binaire constant (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**entrées, Flux et sorties**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Profils**](profiles.md)
</dt> <dt>

[**Encodage à vitesse de transmission variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




