---
description: Les interfaces de document fournissent l’accès aux composants de package XPS qui déterminent la structure d’un document dans un modèle d’objet XPS.
ms.assetid: 3302d164-81ad-4198-a116-f967e7a14147
title: Interfaces de document XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31dff84f7be5ab27f3819f087ddd1da057cb51522dd6ef9f8f3e38b4f93087de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112099"
---
# <a name="xps-om-document-interfaces"></a>Interfaces de document XPS OM

Les interfaces de document fournissent l’accès aux composants de package XPS qui déterminent la structure d’un document dans un modèle d’objet XPS. Le tableau suivant répertorie les interfaces de document.



| Nom de l’interface                                                      | Interfaces enfants logiques                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>           | Représente un ensemble de documents qui sont liés ensemble dans une liste ordonnée.<br/> Les interfaces enfants sont collectées dans une interface [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection) .<br/>                                                                                                                                                                                                  |
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Représente une seule partie FixedDocument et lie la collection de références de page des pages dans un document.<br/> Les interfaces enfants sont collectées dans une interface [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) .<br/> La structure du document est exposée dans une interface [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource) .<br/> |
| [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                   | Version virtualisée légère d’une page dans le document. Une référence de page décrit les caractéristiques principales de la page (telles que ses dimensions), mais n’inclut pas le contenu de la page.<br/>                                                                                                                                                                                             |
| [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/>     | Aucun<br/>                                               | Collection des objets de la page qui sont des cibles de lien hypertexte.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>       | Aucun<br/>                                               | Collection des ressources de composant associées à une page.<br/>                                                                                                                                                                                                                                                                                                                                |



 

## <a name="contents"></a>Contenu

-   L' [utilisation des interfaces IXpsOMDocumentSequence](working-with-xpsomdocumentsequence-interfaces.md) contient des informations sur l’utilisation des interfaces suivantes :
    -   [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
    -   [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
-   L' [utilisation des interfaces IXpsOMDocument](working-with-xpsomdocument-interfaces.md) contient des informations sur l’utilisation des interfaces suivantes :
    -   [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
    -   [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
    -   [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
-   L' [utilisation des interfaces IXpsOMPageReference](working-with-xpsompagereference-interfaces.md) contient des informations sur l’utilisation des interfaces suivantes :
    -   [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
    -   [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
    -   [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
    -   [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)

 

 




