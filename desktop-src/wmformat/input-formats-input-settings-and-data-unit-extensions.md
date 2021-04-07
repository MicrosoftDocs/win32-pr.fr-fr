---
title: Formats d’entrée, paramètres d’entrée et extensions d’unité de données
description: Formats d’entrée, paramètres d’entrée et extensions d’unité de données
ms.assetid: 8e8a0ec8-cb7c-4483-86b0-142ea9f2b835
keywords:
- Windows Media Format SDK, formats d’entrée et paramètres
- Windows Media Format SDK, Data Unit extensions
- SDK Windows Media format, systèmes d’extension de charge utile
- ASF (Advanced Systems Format), formats d’entrée et paramètres
- ASF (format des systèmes avancés), formats d’entrée et paramètres
- ASF (Advanced Systems Format), extensions d’unité de données
- ASF (format de systèmes avancés), extensions d’unité de données
- ASF (Advanced Systems Format), systèmes d’extension de charge utile
- ASF (format de systèmes avancés), systèmes d’extension de charge utile
- extensions d’unité de données, à propos de
- systèmes d’extension de charge utile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c590895fca23a3c668a19ac4e6c5437a35ddb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940207"
---
# <a name="input-formats-input-settings-and-data-unit-extensions"></a>Formats d’entrée, paramètres d’entrée et extensions d’unité de données

L’objet Writer prend en charge les paramètres d’entrée, les formats d’entrée et les extensions d’unité de données, qui vous permettent de contrôler les fonctionnalités du writer. Il n’est pas toujours évident de déterminer les méthodes à utiliser pour contrôler une fonctionnalité spécifique.

Les formats d’entrée sont des formats multimédias qui décrivent les propriétés de base du média que vous transmettez à l’enregistreur pour l’encodage. Par exemple, la taille de frame et l’espace colorimétrique de la vidéo d’entrée sont décrits par le format d’entrée.

Les paramètres d’entrée sont des caractéristiques des données d’entrée au-delà des principes de base, ou des informations sur les transformations à effectuer sur les données. Les paramètres vidéo entrelacés et les informations sur un système de filigrane sont des exemples de paramètres d’entrée.

Les extensions d’unité de données, également appelées systèmes d’extension de charge utile, sont des valeurs qui sont attachées à des échantillons individuels dans la section de données du fichier. Les codes temporels SMPTE et les informations sur les pixels non carrés sont des exemples d’extensions d’unité de données.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration d’extensions d’unité de données**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Extensions d’unité de données**](data-unit-extensions.md)
</dt> <dt>

[**Fonctionnalités d’écriture de fichier**](file-writing-features.md)
</dt> <dt>

[**Énumération de format d’entrée**](input-format-enumeration.md)
</dt> <dt>

[**Paramètres d’entrée**](input-settings.md)
</dt> <dt>

[**Utilisation des entrées**](working-with-inputs.md)
</dt> </dl>

 

 




