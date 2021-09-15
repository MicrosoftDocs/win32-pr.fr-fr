---
description: Cette interface IXpsOMPrintTicketResource de l’API de document XPS donne accès à un ticket d’impression existant et permet également de créer un ticket d’impression dans un modèle d’objet XPS.
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: Interfaces du ticket d’impression XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646089455e7106b1be3716c0ccf0774be361f130
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519437"
---
# <a name="xps-om-print-ticket-interfaces"></a>Interfaces du ticket d’impression XPS OM

Cette interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) de l’API de document XPS donne accès à un ticket d’impression existant et permet également de créer un ticket d’impression dans un modèle d’objet XPS.

## <a name="print-ticket-resources"></a>Imprimer les ressources du ticket

L’interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) permet à un programme de lire le contenu d’un ticket d’impression existant en appelant la méthode **GetPrintTicketResource** d’une interface qui prend en charge un ticket d’impression. De nouvelles ressources de ticket d’impression peuvent être ajoutées à une partie de document en appelant **SetPrintTicketResource**.

Il existe trois niveaux de ticket d’impression qui spécifient l’étendue du ticket d’impression. Les niveaux de ticket d’impression sont : le niveau du travail (ou du package), le niveau du document et le niveau de la page. Le tableau suivant montre la relation entre le niveau de ticket d’impression, l’interface XPS OM correspondante et les méthodes utilisées pour accéder à la ressource de ticket d’impression.

| Niveau du ticket d’impression | Interface                                                | Get, méthode                                                                      | Set, méthode                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Travail                | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| Document           | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| Page               | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>Imprimer le contenu du ticket

Le contenu d’une ressource de ticket d’impression existante est accessible en lisant à partir du flux associé à la ressource. La méthode [**GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) de l’interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) retourne le pointeur vers un flux de données en lecture seule qui contient le contenu au format XML du ticket d’impression. Le format du contenu du ticket d’impression est décrit dans la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Une nouvelle ressource de ticket d’impression peut être créée en créant une nouvelle interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) . Un ticket d’impression au format XML valide est écrit dans un flux de données et un URI de composant est créé pour identifier la partie du ticket d’impression. Pour plus d’informations sur le contenu d’un ticket d’impression valide, reportez-vous à la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). Le flux et l’URI du composant sont passés comme paramètres de l’appel [**SetContent**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) pour définir la nouvelle ressource de ticket d’impression et la ressource de ticket d’impression est ajoutée à la partie de document correspondante en appelant la méthode **SetPrintTicketResource** indiquée dans le tableau précédent.

## <a name="print-ticket-inheritance"></a>Héritage du ticket d’impression

Les tickets d’impression héritent des propriétés des tickets d’impression avec une plus grande étendue. Par exemple, un ticket d’impression au niveau du document hérite des propriétés du ticket d’impression au niveau du travail qui est associé à la séquence de documents du document. De même, un ticket d’impression au niveau de la page hérite des propriétés du ticket d’impression au niveau du document qui est associé au document de la page. Dans ce processus d’héritage, les propriétés spécifiées dans le ticket d’impression de niveau inférieur remplacent les propriétés correspondantes qui, autrement, seraient héritées du ticket d’impression de niveau supérieur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



