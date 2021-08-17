---
description: Décrit comment écrire le contenu d’un modèle d’objet XPS dans un programme dans un fichier de document XPS.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Écrire un modèle OM XPS dans un document XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f6ef79f592ad241e54e9a01fb5e4fe72cc41573e75c78f347109cdfb1c6f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098556"
---
# <a name="write-an-xps-om-to-an-xps-document"></a>Écrire un modèle OM XPS dans un document XPS

Décrit comment écrire le contenu d’un modèle d’objet XPS dans un programme dans un fichier de document XPS.

Si un programme possède un modèle d’objet XPS qui contient un document complet, le programme peut écrire le modèle OM XPS dans un fichier en tant que document XPS, en appelant la méthode [**WritetoFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) de l’interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .

Avant d’utiliser ces exemples de code dans un programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a>Écriture d’un modèle d’objet XPS complet dans un document XPS

Une fois que vous avez défini le contenu d’un modèle d’objet XPS, vous pouvez enregistrer le modèle d’objet XPS dans un fichier en tant que document XPS, en appelant la méthode [**WritetoFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) de l’interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> L’écriture d’un modèle OM XPS dans un fichier ou un flux ne crée pas automatiquement une miniature pour le document XPS. Pour créer une miniature du document XPS, utilisez l’interface [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .

 

## <a name="incrementally-writing-an-xps-document"></a>Écriture incrémentielle d’un document XPS

L’interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) peut être utilisée pour écrire les parties d’un document XPS de manière incrémentielle. par exemple, lorsque les parties du document sont créées ou traitées dans l’ordre.

> [!Note]  
> L’écriture d’un modèle OM XPS dans un fichier ou un flux ne crée pas automatiquement une miniature pour le document XPS. Pour créer une miniature du document XPS, utilisez l’interface [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Imprimer un modèle OM XPS](print-an-xps-om.md)
</dt> <dt>

**Utilisé dans cette section**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[Initialiser un modèle d’objet XPS](xps-object-model-initialization.md)
</dt> <dt>

[Informations de référence sur l’API de document XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
