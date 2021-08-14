---
description: Les rédacteurs et les demandeurs maintiennent les informations nécessaires à une opération de sauvegarde ou de restauration dans leurs propres documents de métadonnées.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Métadonnées VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e69d0a40bbbce2d231573d187843c14bd83fea419a7024940d0fd618838500b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986579"
---
# <a name="vss-metadata"></a>Métadonnées VSS

Les rédacteurs et les demandeurs maintiennent les informations nécessaires à une opération de sauvegarde ou de restauration dans leurs propres documents de métadonnées.

Ces documents, respectivement le [*document de métadonnées*](vssgloss-w.md) de l’enregistreur et le [*document composants de sauvegarde*](vssgloss-b.md), sont utilisés comme base pour la communication et la coordination des rédacteurs et des demandeurs pendant les activités de sauvegarde et de restauration.

Les métadonnées sont représentées au format XML à l’aide d’un schéma propriétaire. Les métadonnées peuvent être copiées sur disque, sur bande ou sur tout autre dispositif de stockage de masse. Il doit toujours être enregistré sur le support de sauvegarde au cours d’une opération de sauvegarde et doit être récupéré à partir de ce média au cours d’une opération de restauration.

**Attention :** Les détails spécifiques au format et au schéma sont destinés uniquement à une utilisation système. Les développeurs ne doivent pas tenter de modifier ou d’utiliser directement la représentation XML des métadonnées.

Les enregistreurs et les demandeurs sont fournis avec diverses méthodes de requête et de définition pour accéder et modifier les composants de sauvegarde et les documents de métadonnées d’écriture :

-   [Utilisation du document de métadonnées de l’enregistreur](working-with-the-writer-metadata-document.md)
-   [Utilisation du document sur les composants de sauvegarde](working-with-the-backup-components-document.md)
-   [Composants de métadonnées VSS](vss-metadata-components.md)

 

 



