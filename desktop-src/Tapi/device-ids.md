---
description: D’autres fonctions de téléphone TAPI utilisent un handle vers un appareil téléphonique ouvert pour identifier l’appareil téléphonique ouvert.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: ID des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514830"
---
# <a name="device-ids"></a>ID des appareils

D’autres fonctions de téléphone TAPI utilisent un handle vers un appareil téléphonique ouvert pour identifier l’appareil téléphonique ouvert. Les seules fonctions des appareils téléphoniques qui prennent un paramètre d’identificateur de périphérique téléphonique (par opposition à un handle de téléphone) sont les fonctions [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) et [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) . Une application peut récupérer l’identificateur d’appareil du téléphone à l’aide de la fonction [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) avec le descripteur de téléphone comme paramètre.

Une application peut également obtenir des identificateurs d’appareil pour différentes classes d’appareils associées à un téléphone ouvert en appelant [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid). Consultez [classes d’appareils TAPI](tapi-device-classes.md) pour les noms de classes d’appareils.

Cette fonction prend un handle de téléphone et une description de classe d’appareil. Elle retourne l’identificateur de l’appareil de la classe d’appareil donnée associée à l’appareil téléphonique ouvert. Si la classe d’appareil est « TAPI/Phone », l’identificateur d’appareil de l’appareil téléphonique est retourné.

Contrairement aux appareils en ligne, pour lesquels les services de base de ligne fournissent l’équivalent des POTS, aucun jeu de fonctions minimal garanti n’est défini pour les appareils téléphoniques. Bien que chaque appareil téléphonique fournisse au moins les fonctions et les messages décrits dans cette section, il n’offre pas d’opérations réelles sur l’appareil mobile physique.

 

 



