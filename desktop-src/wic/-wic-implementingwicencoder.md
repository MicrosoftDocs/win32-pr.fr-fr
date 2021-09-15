---
description: Implémentation d’un encodeur WIC-Enabled
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implémentation d’un encodeur WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412220"
---
# <a name="implementing-a-wic-enabled-encoder"></a>Implémentation d’un encodeur WIC-Enabled

## <a name="introduction"></a>Introduction

l’implémentation d’un encodeur wic (Windows Imaging Component) requiert l’écriture de deux classes, comme c’est également le cas pour l’implémentation d’un décodeur wic. les interfaces sur ces classes correspondent directement aux responsabilités d’encodeur décrites dans la section [encodage](-wic-howwicworks.md) du composant de création d’images Windows.

L’une des classes fournit des services au niveau du conteneur et gère la sérialisation des trames d’image individuelles dans le conteneur. Cette classe implémente l’interface [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) . Si votre format d’image prend en charge les métadonnées au niveau du conteneur, vous devez également implémenter l’interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sur cette classe.

L’autre classe fournit des services au niveau de la trame et effectue l’encodage réel des bits d’image pour chaque frame dans le conteneur. Il itère également au sein des blocs de métadonnées pour chaque frame et demande les enregistreurs de métadonnées appropriés pour sérialiser les blocs. Cette classe implémente l’interface **IWICBitmapFrameEncode** et l’interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) . Cette classe doit avoir un membre IStream que la classe de niveau conteneur initialise lors de l’instanciation, dans laquelle la méthode **Commit** sérialise les données de frame.

Dans certains cas, tels que les formats bruts, l’auteur du codec peut ne pas souhaiter que les applications soient en mesure d’encoder ou de recoder au format brut, car l’objectif d’un fichier brut est de contenir les données de capteur exactement telles qu’elles proviennent de l’appareil photo. Dans les cas où l’auteur du codec ne souhaite pas activer l’encodage, il est toujours nécessaire d’implémenter un encodeur rudimentaire uniquement pour permettre l’ajout de métadonnées. Dans ce cas, l’encodeur a uniquement besoin de prendre en charge les méthodes nécessaires pour écrire des métadonnées et peut copier les bits d’image non touchés du décodeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Implémentation de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Interfaces d’encodeur](-wic-encoderinterfaces.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



