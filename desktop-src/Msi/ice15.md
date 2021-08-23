---
description: ICE15 valide le fait que le type de contenu et les références d’extension dans les tables MIME et d’extension soient réciproques. La table MIME doit faire référence à un type de contenu dans une extension que la table d’extension fait référence au même type de contenu.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e5e54dedd2663a9f849abee43e244c73d7aa5835426be05d4e0163f599ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529309"
---
# <a name="ice15"></a>ICE15

ICE15 valide le fait que le type de contenu et les références d’extension dans les tables [MIME](mime-table.md) et d' [extension](extension-table.md) soient réciproques. La table MIME doit faire référence à un type de contenu dans une extension que la table d’extension fait référence au même type de contenu.

Plusieurs extensions peuvent référencer le même type MIME, à condition que le type MIME fasse référence à l’une des extensions. Plusieurs types MIME peuvent faire référence à la même extension, à condition que l’extension fasse référence à l’un des types MIME.

Notez que chaque fois qu’un MIME fait référence à une extension, cette extension ne peut pas avoir la \_ colonne MIME dans la table d’extension définie sur null.

## <a name="result"></a>Résultat

ICE15 publie une erreur si le type de contenu et les références d’extension ne sont pas réciproques.

## <a name="example"></a>Exemples

ICE15 publie deux messages d’erreur pour l’exemple ci-dessous :

-   Le type de contenu test/aile x dans la table MIME fait référence à l’extension TST, mais l’extension TST dans la table d’extension fait référence aux rabats/x-rabats. Ce n’est pas réciproque.
-   Les rabats de type de contenu/rabats font référence à l’extension FLP, mais cette extension a une entrée null dans la \_ colonne MIME de la table d’extension.

[Table MIME](mime-table.md) (partielle)



| ContentType   | Extension\_ |
|---------------|-------------|
| test/x-test   | TST         |
| rabats/rabats | FLP         |



 

[Table d’extension](extension-table.md) (partielle)



| Extension | MIME\_        |
|-----------|---------------|
| TST       | rabats/rabats |
| FLP       | Null          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



