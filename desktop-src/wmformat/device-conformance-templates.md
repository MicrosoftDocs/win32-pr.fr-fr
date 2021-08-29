---
title: Modèles de conformité des appareils
description: Modèles de conformité des appareils
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- Windows Media Format SDK, modèles de conformité des appareils
- codecs, modèles de conformité des appareils
- modèles de conformité des appareils, à propos de
- modèles, modèles de conformité des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4eea2bcb923cef2a92519b613f22bab046fbde9a50cbbdf29f22a0921a56fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655670"
---
# <a name="device-conformance-templates"></a>Modèles de conformité des appareils

les codecs de la série Media 9 Windows prennent en charge les modèles de conformité des appareils, qui sont des plages définies de paramètres de configuration de flux et d’algorithmes de codec. Chaque modèle définit les plages de valeurs appropriées pour certains périphériques.

Par le passé, les fabricants de matériel qui rendaient des appareils aptes à émettre des fichiers ASF fonctionnaient tous avec leurs propres normes. Cela a abouti à une large gamme de fonctionnalités sur des appareils similaires qui se poursuivent aujourd’hui.

avec les modèles de conformité des appareils, les codecs multimédias Windows établissent un motif commun pour les appareils similaires. Les fabricants de matériel peuvent indiquer les modèles auxquels leurs appareils sont conformes, ce qui permet aux créateurs de contenu de cibler plus en toute confiance leurs fichiers pour la lecture des appareils. Il est également plus facile pour les applications de lecteur de déterminer si un fichier est inapproprié pour l’appareil avant de tenter de le lire.

Un modèle de conformité de périphérique est identifié par une chaîne, qui est stockée sous la forme d’un attribut de métadonnées associé au flux auquel le modèle s’applique. Pour obtenir la liste des modèles et leurs chaînes et paramètres, consultez [paramètres de modèle de conformité des appareils](device-conformance-template-parameters.md).

les modèles de conformité des appareils sont pris en charge pour tous les codecs de la série Windows Media 9 et versions ultérieures, à l’exception du codec d’écran Windows Media Video 9 et du codec Windows Media Audio 9 Lossless.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités du codec**](codec-features.md)
</dt> <dt>

[**Utilisation des modèles de conformité des appareils**](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




