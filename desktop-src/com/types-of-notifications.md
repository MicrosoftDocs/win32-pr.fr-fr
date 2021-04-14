---
title: Types de notifications
description: Types de notifications
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380215"
---
# <a name="types-of-notifications"></a>Types de notifications

Les notifications sont classées en trois groupes : document composé, données et vue. Un objet envoie des notifications de document composé en réponse à un changement de nom, d’enregistrement, de fermeture ou, dans le cas d’un lien, dont la source de lien est renommée. Comme vous pouvez vous y attendre, les objets envoient des notifications de données en réponse à des modifications de leurs données et envoient des notifications d’affichage en réponse aux modifications apportées à leur présentation. Les applications de conteneur doivent s’inscrire séparément pour chacun de ces types de notification, mais elles peuvent toutes être gérées par un seul récepteur de notifications.

Tous les conteneurs, le gestionnaire d’objets et l’objet lié s’inscrivent pour les notifications de document composé. Le conteneur standard s’inscrit également pour les notifications d’affichage. Les notifications de données sont généralement envoyées à l’objet lié et au gestionnaire d’objets. Un conteneur à usage spécial, tel qu’un conteneur qui restitue les données lui-même, peut tirer parti de la réception de notifications de données au lieu de notifications d’affichage. Par exemple, un conteneur de graphique incorporé avec un lien vers une table peut s’inscrire aux notifications de données. Comme une modification apportée à la table affecte le graphique, la réception d’une notification de données dirigerait le conteneur pour obtenir les nouvelles données tabulaires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Notifications](notifications.md)
</dt> </dl>

 

 




