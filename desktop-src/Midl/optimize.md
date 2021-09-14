---
title: optimiser l’attribut
description: L’attribut \ Optimize \ ACF est utilisé pour ajuster le niveau de gradation pour le marshaling des données.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- MIDL d’attribut Optimize
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093290"
---
# <a name="optimize-attribute"></a>optimiser l’attribut

L’attribut **\[ optimize \]** ACF est utilisé pour affiner le niveau de gradation pour le marshaling des données.

> [!Note]  
> Ce mot clé est superceeded et ne doit pas être utilisé. Les compilations MIDL actuelles doivent utiliser [**/Oicf**](-oi.md)[**/Robust**](-robust.md) à la place.

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*optimisation-options* 
</dt> <dd>

Spécifie la méthode de marshaling des données. Utilisez « s » pour le marshaling en mode mixte ou « i » pour le marshaling interprété.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette version de RPC fournit deux méthodes pour le marshaling des données : mode mixte (« s ») et interprété (« i »). Ces méthodes correspondent aux commutateurs de ligne de commande [**/OS**](-os.md) et [**/OI**](-oi.md) . La méthode interprétée marshale les données complètement hors connexion. Bien que cela puisse réduire considérablement la taille du stub, les performances peuvent être affectées.

Si les performances posent un problème, la méthode en mode mixte peut être la meilleure approche. Le mode mixte permet au compilateur MIDL d’effectuer la détermination entre les données qui seront marshalées en ligne et qui seront marshalées par un appel à une bibliothèque de liens dynamiques hors connexion. Si de nombreuses procédures utilisent les mêmes types de données, une procédure unique peut être appelée à plusieurs reprises pour marshaler les données. De cette façon, les données les plus adaptées au marshaling en ligne sont traitées en ligne, tandis que les autres données peuvent être marshalées plus efficacement en mode hors connexion.

Notez que l’attribut **\[ optimize \]** peut être utilisé en tant qu’attribut d’interface ou en tant qu’attribut d’opération. S’il est utilisé comme attribut d’interface, il définit la valeur par défaut pour l’interface entière, en remplaçant les commutateurs de ligne de commande. Toutefois, si elle est utilisée en tant qu’attribut d’opération, elle affecte uniquement cette opération, en remplaçant les commutateurs de ligne de commande et l’interface par défaut.

## <a name="examples"></a>Exemples

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**/OS**](-os.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> </dl>

 

 




