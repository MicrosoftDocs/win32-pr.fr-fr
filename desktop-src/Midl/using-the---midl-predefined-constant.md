---
title: Utilisation de la constante prédéfinie __midl
description: Lorsque le compilateur MIDL traite les fichiers IDL et ACF d’entrée, \_ \_ MIDL est défini par défaut et est utilisé pour la compilation conditionnelle afin d’atteindre la cohérence dans l’ensemble de la génération.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL MIDL du compilateur MIDL, à l’aide de la constante prédéfinie _midl
- _midl MIDL de constante prédéfinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029287"
---
# <a name="using-the-__midl-predefined-constant"></a>Utilisation de la \_ \_ constante prédéfinie MIDL

Lorsque le compilateur MIDL traite les fichiers IDL et ACF d’entrée, \_ \_ MIDL est défini par défaut et est utilisé pour la compilation conditionnelle afin d’atteindre la cohérence dans l’ensemble de la génération. Cela permet d’extraire l’utilisation d’instructions de définition dans les fichiers d’en-tête, telles que **MIDL \_ Pass**, et de les remplacer par un indicateur cohérent. La valeur de la \_ \_ constante MIDL indique la version du compilateur *major. minor* en fonction de la formule *principale* \* 100 + *Minor*; par exemple, MIDL ver. 6.0. x a le \_ \_ MIDL défini en tant que 600.

Si vous le souhaitez, vous pouvez remplacer cette valeur par défaut en spécifiant les éléments suivants sur la ligne de commande : **/u \_ \_ MIDL**. Pour plus d’informations, consultez [**/u**](-u.md).

 

 




