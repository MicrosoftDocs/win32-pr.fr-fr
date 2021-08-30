---
description: Décrit comment lire un document XPS existant à partir d’un fichier dans un modèle d’objet XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Lire un document XPS dans un modèle d’objet XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0361f00d148f8f29ab36577683cecc0087ff91af81469e7de527de90a8b1a795
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112189"
---
# <a name="read-an-xps-document-into-an-xps-om"></a>Lire un document XPS dans un modèle d’objet XPS

Décrit comment lire un document XPS existant à partir d’un fichier dans un modèle d’objet XPS.

Pour créer un modèle d’objet XPS à partir d’un document XPS, appelez la méthode [**IXpsOMObjectFactory :: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .

Avant d’utiliser ces exemples de code dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).

## <a name="code-example"></a>Exemple de code

L’exemple de code suivant suppose que l’initialisation décrite dans [initialiser un modèle d’objet XPS](xps-object-model-initialization.md) a réussi.


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



Pour créer un modèle d’objet XPS à partir d’un document XPS stocké sous forme de flux, appelez [**IXpsOMObjectFactory :: CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).

## <a name="remarks"></a>Remarques

Si vous écrivez un modèle d’objet XPS immédiatement après y avoir lu un package XPS, une partie du contenu d’origine peut être perdue ou modifiée.

Certaines des modifications qui peuvent se produire dans ce cas sont répertoriées dans le tableau suivant :

| Fonctionnalité de document                      | Action                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| Signatures numériques<br/>         | Supprimé du document<br/>                               |
| Partie DiscardControl<br/>        | Supprimé du document<br/>                               |
| Parties de documents étrangers<br/>     | Supprimé du document<br/>                               |
| FixedPage, balisage<br/>           | Modifié à partir de l’original<br/>                              |
| Balisage du dictionnaire de ressources<br/> | Modifié à partir de l’original, si l’indicateur d’optimisation est défini<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Naviguer dans le modèle d’objet XPS](navigate-the-xps-om.md)
</dt> <dt>

[Écrire du texte dans un modèle d’objet XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Dessiner des graphiques dans un modèle d’objet XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Placer des images dans un modèle d’objet XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Utilisé dans cette section**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[Initialiser un modèle d’objet XPS](xps-object-model-initialization.md)
</dt> <dt>

[API d’empaquetage](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Informations de référence sur l’API de document XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

