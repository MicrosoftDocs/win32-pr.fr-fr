---
description: ICE86 émet un avertissement si le package utilise la propriété AdminUser dans la colonne de base de données du type de condition. Les auteurs de package doivent utiliser la propriété Privileged dans les instructions conditionnelles.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25df1e2a9c3ab610e78efd6f797cb916f0563e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320085"
---
# <a name="ice86"></a>ICE86

ICE86 émet un avertissement si le package utilise la propriété [**adminuser**](adminuser.md) dans la colonne de base de données du type de [condition](condition.md) . Les auteurs de package doivent utiliser la propriété [**Privileged**](privileged.md) dans les instructions conditionnelles.

## <a name="result"></a>Résultats

ICE86 publie l’avertissement suivant.



| AVERTISSEMENT ICE86                                                                                               | Description                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Propriété \` % s \` trouvée dans la colonne \` % s \` . \` % s \` dans la ligne% s. \`La \` propriété Privileged est souvent plus appropriée. | La propriété [**adminuser**](adminuser.md) a été utilisée dans un champ condition. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



