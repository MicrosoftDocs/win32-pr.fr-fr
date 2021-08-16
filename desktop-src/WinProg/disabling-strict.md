---
title: Désactivation de STRICT
description: Pour désactiver la vérification de type STRICTe, définissez le nom du symbole sur non \_ strict. Dans Visual C/C++, vous pouvez également spécifier cette définition sur la ligne de commande ou dans un Makefile en spécifiant/DNO \_ strict comme option du compilateur.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078361b5cc3fd4916ac2ab4f7207752e869568b8781c9ef3dd8e38427d252592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743655"
---
# <a name="disabling-strict"></a>Désactivation de STRICT

Pour désactiver la vérification de type **stricte** , définissez le nom du symbole sur **non \_ strict**. Dans Visual C/C++, vous pouvez également spécifier cette définition sur la ligne de commande ou dans un Makefile en spécifiant **/DNO \_ strict** comme option du compilateur.

pour **ne définir aucune \_ restriction** au niveau fichier par fichier, insérez une instruction **\# define** avant d’inclure Windows. h :


```C++
#define NO_STRICT
#include <windows.h>
```



Pour de meilleurs résultats, vous devez également définir le niveau d’avertissement pour les messages d’erreur sur au moins **/W3**. cela est toujours recommandé avec les applications pour Windows, car une pratique de codage qui génère un avertissement (par exemple, en passant un nombre incorrect de paramètres) provoque généralement une erreur irrécupérable au moment de l’exécution si elle n’est pas corrigée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation du STRICT](enabling-strict.md)
</dt> <dt>

[Conformité STRICTe](strict-compliance.md)
</dt> </dl>

 

 




