---
title: Utilisation des entrées
description: Utilisation des entrées
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows Media Format SDK, utilisation des entrées
- ASF (Advanced Systems Format), utilisation des entrées
- ASF (format de systèmes avancés), utilisation des entrées
- profils, utilisation des entrées
- flux, utilisation des entrées
- codecs, utilisation des entrées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462143"
---
# <a name="working-with-inputs"></a>Utilisation des entrées

Tout comme la configuration de flux appropriée dans le profil est requise pour obtenir le codec pour compresser un flux, vous devez également vous assurer que le type de support non compressé que vous transmettez à l’enregistreur est décrit avec précision. Chaque codec Windows Media est associé à un type d’entrée par défaut, mais plusieurs types d’entrée sont pris en charge. Vous pouvez examiner les entrées prises en charge et sélectionner celle qui correspond à vos données. Le processus d’utilisation des entrées est résumé dans les étapes suivantes :

1.  Lorsque vous chargez un profil à utiliser par le writer, l’objet Writer affecte un numéro d’entrée pour chaque connexion dans le profil. Pour plus d’informations sur le chargement des profils pour le writer, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md). À moins que vous n’utilisiez l’exclusion mutuelle par vitesse de transmission, il existe une connexion pour chaque flux. Les flux qui sont mutuellement exclusifs par la vitesse de transmission partagent une seule connexion.
2.  Votre application doit identifier les numéros d’entrée du fichier. Pour plus d’informations sur l’identification des numéros d’entrée, consultez [pour identifier les entrées par numéro](to-identify-inputs-by-number.md).
3.  Pour chaque entrée, vous devez vous assurer que le format d’entrée correspond à vos données. Vous pouvez énumérer les formats d’entrée pris en charge par le kit de développement logiciel (SDK). Pour plus d’informations, consultez [pour énumérer les formats d’entrée](to-enumerate-input-formats.md). Vous ne pouvez pas énumérer les formats d’entrée de flux arbitraires ou de flux déjà compressés. Pour plus d’informations sur ces cas spéciaux, consultez [entrées de flux arbitraires et précompressés](arbitrary-and-precompressed-stream-inputs.md).
4.  Attribuez le format d’entrée correct pour chaque connexion. Pour plus d’informations, consultez [attribution de formats d’entrée](assigning-input-formats.md).
5.  Certaines fonctionnalités du codec et de l’enregistreur sont configurées au moment de l’encodage plutôt que dans le profil. Pour configurer ces fonctionnalités, vous devez utiliser des paramètres d’entrée. Pour plus d’informations, consultez [pour définir les paramètres d’entrée](to-set-input-settings.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




