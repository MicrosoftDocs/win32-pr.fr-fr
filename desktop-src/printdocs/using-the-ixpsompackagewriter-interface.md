---
description: L’interface IXpsOMPackageWriter crée un fichier de document XPS dans lequel les applications peuvent écrire le contenu des interfaces IXpsOMPage d’un modèle OM XPS.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Utilisation de l’interface IXpsOMPackageWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a4437f939821b826fa0d5c30407777b7d44c5d03c236f4ef850d52145b4f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098701"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Utilisation de l’interface IXpsOMPackageWriter

L’interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crée un fichier de document XPS dans lequel les applications peuvent écrire le contenu des interfaces [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) d’un modèle OM XPS. L’interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) est particulièrement utile lorsque le contenu du document est traité ou créé de manière séquentielle. Contrairement aux méthodes [**WritetoFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) et [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) de l’interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) , pour que l’interface **IXpsOMPackageWriter** soit utilisée, l’intégralité du FixedDocument et du FixedDocumentSequence ne doit pas être terminée.

## <a name="overview"></a>Vue d’ensemble

L’interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) écrit une page à la fois, de la première page d’un document XPS au dernier. L’interface peut être utilisée pour créer des fichiers de document XPS simples, ainsi que des fichiers de document XPS complexes contenant plus d’un FixedDocument dans le FixedDocumentSequence. Dans les fichiers de document XPS complexes, les FixedDocuments sont également créés en séquence, en commençant par le premier FixedDocument dans le FixedDocumentSequence. L’interface **IXpsOMPackageWriter** ne prend pas en charge la création de contenu de document dans un ordre aléatoire. Utilisez-la, par exemple, pour créer un rapport séquentiel ou pour effectuer un traitement dans un filtre de pilote de périphérique dans lequel le contenu du document est transmis au pilote en séquence.

## <a name="terminology-review"></a>Revue terminologique

Un *fichier de document XPS* est un package OPC (Open Packaging Conventions) qui est conforme à la spécification Paper XML. Techniquement, l’interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crée un *package OPC*, mais il s’agit d’un package OPC conforme à la spécification Paper XML. C’est pourquoi, dans les discussions sur les documents XPS, les termes *document XPS* et *package* sont souvent utilisés indifféremment.

Le *package* créé par l’interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) contient les composants de document XPS requis : un FixedDocumentSequence, au moins un FixedDocument et au moins un FixedPage. Le FixedDocumentSequence est créé lors de l’instanciation de l’interface **IXpsOMPackageWriter** . Un FixedDocument est créé chaque fois que [**IXpsOMPackageWriter :: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) est appelé, et un FixedPage est créé chaque fois que [**IXpsOMPackageWriter :: AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) est appelé. Étant donné que l’interface écrit le contenu du document de manière séquentielle, la méthode **AddPage** ajoute la page au dernier créé.

## <a name="using-the-ixpsompackagewriter-interface"></a>Utilisation de l’interface IXpsOMPackageWriter

La procédure suivante décrit comment créer un fichier de document XPS à l’aide de l’interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) . La procédure ne décrit pas comment instancier une interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) et son contenu. Pour plus d’informations sur **IXpsOMPage** et l’ajout de contenu à une page, consultez [interfaces de page OM XPS](xps-object-model-page-interfaces.md) et les rubriques figurant dans la section Voir aussi.

 **Création d’un document**

1.  Instanciez une interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) .

    Cela crée un FixedDocumentSequence vide dans le package.

    -   Pour créer un document XPS dans un fichier, appelez [**IXpsOMObjectFactory :: CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile).
    -   Pour créer un document XPS dans un flux, appelez [**IXpsOMObjectFactory :: CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream).

2.  Démarrez un nouveau document dans le package en appelant [**IXpsOMPackageWriter :: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).

    Avant d’ajouter une page, appelez [**IXpsOMPackageWriter :: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) pour ajouter un FixedDocument au FixedDocumentSequence créé à l’étape 1.

3.  Ajoutez du contenu.
    -   Pour ajouter un nouvel FixedPage au document, appelez [**IXpsOMPackageWriter :: AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage), en lui transmettant un pointeur vers l’interface [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) dont vous souhaitez ajouter le contenu de FixedPage.
    -   Pour créer un FixedDocument dans le FixedDocumentSequence, appelez [**IXpsOMPackageWriter :: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).
4.  Fermez le package et son contenu en appelant [**IXpsOMPackageWriter :: Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close).

## <a name="advanced-features"></a>Fonctionnalités avancées

Les méthodes de l’interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) prennent également en charge l’ajout de ressources, de miniatures et de tickets d’impression. Ces composants de document peuvent être ajoutés aux niveaux package, FixedDocumentSequence, FixedDocument et FixedPage. Pour plus d’informations sur l’utilisation de cette interface pour l’impression, consultez [imprimer un modèle OM XPS](print-an-xps-om.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’API de signature numérique XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Interfaces de page OM XPS](xps-object-model-page-interfaces.md)
</dt> <dt>

[Naviguer dans le modèle d’objet XPS](navigate-the-xps-om.md)
</dt> <dt>

[Utilisation d’une zone de dessin et d’interfaces visuels XPS OM](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Utilisation des interfaces de chemin d’accès OM XPS](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Utilisation du texte, des graphiques et des interfaces d’images XPS OM](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[Interfaces du ticket d’impression XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[Informations de référence sur l’API de document XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



