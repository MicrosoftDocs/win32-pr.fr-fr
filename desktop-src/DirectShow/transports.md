---
description: Transports
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transports
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519943"
---
# <a name="transports"></a>Transports

Pour déplacer des données multimédias via le graphique de filtre, un filtre DirectShow doit prendre en charge l’un des différents protocoles possibles. Ces protocoles sont appelés transports. Lorsque deux filtres se connectent, ils doivent prendre en charge le même transport. dans le cas contraire, ils ne peuvent pas échanger de données multimédias. En règle générale, un transport requiert que l’un des codes confidentiels prenne en charge une interface particulière. Lorsque les filtres se connectent, un code confidentiel interroge l’autre pour l’interface.

La plupart des filtres DirectShow contiennent les données multimédias dans la mémoire principale et les transmettent à d’autres filtres sur les connexions de code confidentiel. Ce type de transport est appelé transport de mémoire locale. Bien que le transport de mémoire locale soit le transport le plus courant dans DirectShow, tous les filtres ne l’utilisent pas. Par exemple, certains filtres envoient des données multimédias le long d’un chemin d’accès matériel et utilisent des broches uniquement pour fournir des informations de contrôle. Par exemple, consultez l’interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) .

DirectShow définit deux mécanismes pour le transport de mémoire locale, le modèle push et le modèle pull. Dans le modèle push, un filtre source génère des données et les remet au filtre suivant en aval. Ce filtre reçoit passivement les données, les traite, puis les envoie en aval. Dans le modèle d’extraction, le filtre source est connecté à un filtre d’analyseur. Le filtre de l’analyseur demande des données à partir du filtre source. Le filtre source répond aux demandes en livrant des données. Le modèle d’émission utilise l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , et le modèle d’extraction utilise l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

Le modèle push est plus courant que le modèle d’extraction. Par conséquent, les articles qui suivent supposent un modèle push. Le dernier article de cette section, [pull Model](pull-model.md), décrit comment l’interface **IAsyncReader** diffère de **IMemInputPin**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



