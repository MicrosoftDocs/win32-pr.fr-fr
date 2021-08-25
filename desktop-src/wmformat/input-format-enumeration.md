---
title: Énumération de format d’entrée
description: Énumération de format d’entrée
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Media Format SDK, énumérations de format d’entrée
- Windows Media Format SDK, énumération des formats d’entrée
- ASF (Advanced Systems Format), énumérations de format d’entrée
- ASF (format des systèmes avancés), énumérations de format d’entrée
- ASF (Advanced Systems Format), énumération des formats d’entrée
- ASF (format avancé des systèmes), énumération des formats d’entrée
- énumérations de format d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a261b2edae285a970bead5d039c4e85076530eb363aa025289b75ec56618406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809039"
---
# <a name="input-format-enumeration"></a>Énumération de format d’entrée

L’objet Writer obtient les informations de format de flux à partir du profil que vous lui donnez. Les informations de configuration de flux dans un profil donnent à l’enregistreur toutes les informations dont il a besoin sur la façon dont les données doivent être écrites dans le fichier. Le profil ne fournit à l’enregistreur aucune information sur le format des exemples d’entrée fournis par votre application. les formats d’entrée sont inconnus uniquement pour les flux compressés avec l’un des codecs de média Windows ; les entrées des types de flux arbitraires sont prévisibles en fonction des informations contenues dans le profil.

L’objet Writer peut communiquer avec le codec d’un flux pour déterminer les types d’entrée qui peuvent être utilisés. Des méthodes sont fournies pour énumérer les types d’entrée possibles. Vous devez toujours trouver le type d’entrée qui correspond à votre média d’entrée en énumérant les types pris en charge au lieu de définir manuellement les propriétés du média d’entrée. Pour plus d’informations, consultez [pour énumérer les formats d’entrée](to-enumerate-input-formats.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités d’écriture de fichier**](file-writing-features.md)
</dt> <dt>

[**Utilisation des entrées**](working-with-inputs.md)
</dt> </dl>

 

 




