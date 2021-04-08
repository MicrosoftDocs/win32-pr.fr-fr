---
title: Désactivation de STRICT
description: Pour désactiver la vérification de type STRICTe, définissez le nom du symbole sur non \_ strict. Dans Visual C/C++, vous pouvez également spécifier cette définition sur la ligne de commande ou dans un Makefile en spécifiant/DNO \_ strict comme option du compilateur.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674185"
---
# <a name="disabling-strict"></a>Désactivation de STRICT

Pour désactiver la vérification de type **stricte** , définissez le nom du symbole sur **non \_ strict**. Dans Visual C/C++, vous pouvez également spécifier cette définition sur la ligne de commande ou dans un Makefile en spécifiant **/DNO \_ strict** comme option du compilateur.

Pour **ne définir aucune \_ restriction** au niveau fichier par fichier, insérez une instruction **\# define** avant d’inclure Windows. h :


```C++
#define NO_STRICT
#include <windows.h>
```



Pour de meilleurs résultats, vous devez également définir le niveau d’avertissement pour les messages d’erreur sur au moins **/W3**. Cela est toujours recommandé avec les applications pour Windows, car une pratique de codage qui génère un avertissement (par exemple, en passant un nombre incorrect de paramètres) provoque généralement une erreur irrécupérable au moment de l’exécution si elle n’est pas corrigée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation du STRICT](enabling-strict.md)
</dt> <dt>

[Conformité STRICTe](strict-compliance.md)
</dt> </dl>

 

 




