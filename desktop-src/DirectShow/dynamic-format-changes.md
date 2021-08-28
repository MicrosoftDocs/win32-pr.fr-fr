---
description: Modifications de format dynamique
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Modifications de format dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ce6d30b13458694b740bfb7bed8498c0f54d5b19648a484c5330d2b7627eab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998359"
---
# <a name="dynamic-format-changes"></a>Modifications de format dynamique

Lorsque deux filtres se connectent, ils s’accordent sur un type de média, qui décrit le format des données que le filtre en amont va distribuer. Dans la plupart des cas, le type de média est fixe pour la durée de la connexion. toutefois, DirectShow offre une prise en charge limitée des filtres pour modifier le type de média. Lorsqu’un filtre change de type de média, il est appelé une *modification de format dynamique*. si vous écrivez un filtre DirectShow, vous devez être conscient des mécanismes pour les modifications de format dynamique. Même si votre filtre ne prend pas en charge ces modifications, il doit répondre correctement si un autre filtre demande un nouveau format.

DirectShow définit plusieurs mécanismes distincts pour les modifications de format dynamiques, en fonction de l’état du graphique de filtre et du type de modification requis.

-   Si le graphique est arrêté, les broches peuvent se reconnecter et renégocier le type de média. Pour plus d’informations, consultez [reconnexion des codes confidentiels](reconnecting-pins.md).
-   Certains filtres peuvent reconnecter des broches même si le graphique est actif (en cours d’exécution ou en pause). Pour plus d’informations sur ce mécanisme, consultez [reconnexion dynamique](dynamic-reconnection.md).

Sinon, si le graphique est actif, mais que les filtres en question ne prennent pas en charge les reconnexions de code confidentiel dynamique, il existe trois mécanismes possibles pour modifier le format :

-   [QueryAccept (en aval)](queryaccept--downstream.md) est utilisé quand une broche de sortie propose une modification de format à son homologue en aval, mais uniquement si le nouveau format ne requiert pas une mémoire tampon plus grande.
-   [QueryAccept (en amont)](queryaccept--upstream.md) est utilisé lorsqu’une broche d’entrée propose une modification de format à son homologue en amont. Le nouveau format peut être de la même taille, ou il peut être plus grand.
-   [ReceiveConnection](receiveconnection.md) est utilisé lorsqu’une broche de sortie propose une modification de format à son homologue en aval, et que le nouveau format requiert une mémoire tampon plus grande.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des modifications de format à partir du convertisseur vidéo](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



