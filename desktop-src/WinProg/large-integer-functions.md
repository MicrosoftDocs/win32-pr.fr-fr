---
title: Fonctions entières de type long
description: Les fonctions suivantes sont utilisées avec des entiers volumineux.
ms.assetid: f34932f4-b126-4d6c-a2f0-3ad706fd5629
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7878d817e7647f46da52105cea264f6332303de2ca1d7b440697defc656cd0b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071629"
---
# <a name="large-integer-functions"></a>Fonctions entières de type long

Les fonctions suivantes sont utilisées avec des entiers volumineux.

## <a name="in-this-section"></a>Dans cette section



| Fonction                                                                    | Description                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64)<br/>                             | Multiplie deux entiers 32 bits signés, en retournant un résultat entier 64 bits signé.<br/>                                                                                                                   |
| [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)<br/>                         | Effectue une opération de décalage logique vers la gauche sur une valeur entière 64 bits non signée. La fonction fournit un code de décalage amélioré pour les décalages logiques de gauche où le nombre de décalages se trouve dans la plage 0-31.<br/>      |
| [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)<br/>                         | Effectue une opération de décalage arithmétique droite sur une valeur entière 64 bits signée. La fonction fournit un code de décalage amélioré pour les décalages arithmétiques appropriés où le nombre de décalages se trouve dans la plage 0-31.<br/> |
| [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32)<br/>                         | Effectue une opération de décalage logique droite sur une valeur entière 64 bits non signée. La fonction fournit un code de décalage amélioré pour les décalages logiques appropriés où le nombre de décalages se trouve dans la plage 0-31.<br/>    |
| [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv)<br/>                                         | Multiplie les valeurs 2 32 bits, puis divise le résultat 64 bits par une troisième valeur 32 bits.<br/>                                                                                                           |
| [**Multiply128**](/windows/desktop/api/Winnt/nf-winnt-multiply128)<br/>                               | Multiplie les entiers 2 64 bits pour produire un entier 128 bits.<br/>                                                                                                                                       |
| [**MultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-multiplyextract128)<br/>                 | Multiplie les entiers 2 64 bits pour produire un entier 128 bits, décale le produit vers la droite du nombre de bits spécifié et retourne les 64 bits de poids faible du résultat.<br/>                           |
| [**MultiplyHigh**](/windows/desktop/api/Winnt/nf-winnt-multiplyhigh)<br/>                             | Multiplie les entiers 2 64 bits pour produire un entier 128 bits et obtient les 64 bits de poids fort.<br/>                                                                                                             |
| [**PopulationCount64**](/windows/desktop/api/Winnt/nf-winnt-populationcount64)<br/>                   | Compte le nombre d’un octet (nombre de remplissage) dans un entier non signé 64 bits.<br/>                                                                                                                     |
| [**ShiftLeft128**](/windows/desktop/api/winnt/nf-winnt-shiftleft128)<br/>                             | Décale 128 bits vers la gauche.<br/>                                                                                                                                                                               |
| [**ShiftRight128**](/windows/desktop/api/winnt/nf-winnt-shiftright128)<br/>                           | Décale vers la droite 128 bits.<br/>                                                                                                                                                                              |
| [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64)<br/>                           | Multiplie deux entiers non signés 32 bits, en retournant un résultat entier 64 bits non signé.<br/>                                                                                                              |
| [**UnsignedMultiply128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiply128)<br/>               | Multiplie deux entiers non signés 64 bits pour produire un entier non signé 128 bits.<br/>                                                                                                                    |
| [**UnsignedMultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyextract128)<br/> | Multiplie deux entiers non signés 64 bits pour produire un entier non signé 128 bits, décale le produit vers la droite du nombre de bits spécifié et retourne les 64 bits de poids faible du résultat.<br/>        |
| [**UnsignedMulitplyHigh**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyhigh)<br/>             | Multiplie les entiers 2 64 bits pour produire un entier 128 bits et obtient les bits non signés élevés (64).<br/>                                                                                                    |



 

 

 





