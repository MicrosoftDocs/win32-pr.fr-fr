---
description: ICE08 vérifie que la table des composants ne contient pas de GUID en double. Chaque composant doit avoir un GUID unique. Aucune validation n’est effectuée si la table de composants n’existe pas.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6075b7c895242fe5cfa7608a414643a9e3491787fc59037f8761fa66b18354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745319"
---
# <a name="ice08"></a>ICE08

ICE08 vérifie que la [table des composants](component-table.md) ne contient pas de [GUID](guid.md)en double. Chaque composant doit avoir un GUID unique. Aucune validation n’est effectuée si la table de composants n’existe pas.

## <a name="result"></a>Résultat

ICE08 publie un message d’erreur si au moins deux entrées de la colonne ComponentId de la table des composants contiennent le même GUID.

## <a name="example"></a>Exemple

Dans l’exemple suivant, ICE08 publie un message indiquant que les composants Red et Green comportent des GUID en double.

[Table des composants](component-table.md) (partielle)



| Composant | ComponentId                            |
|-----------|----------------------------------------|
| Rouge       | {0000000A-0003-0000-0000-624474736554} |
| Bleu      | {0000000A-0003-0000-0000-624474736354} |
| Vert     | {0000000A-0003-0000-0000-624474736554} |



 

Pour corriger cette erreur, modifiez l’un des GUID dupliqués.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



