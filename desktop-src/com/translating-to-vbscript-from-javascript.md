---
title: Conversion en VBScript à partir de JavaScript
description: Conversion en VBScript à partir de JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509185"
---
# <a name="translating-to-vbscript-from-javascript"></a>Conversion en VBScript à partir de JavaScript

En JavaScript, il existe plusieurs types de données, tels que des nombres, des chaînes, des valeurs booléennes, des objets et l’attribut null. VBScript utilise uniquement un type de données **Variant**, qui peut être sous-typé pour représenter des chaînes, des nombres, des valeurs booléennes, etc.

En JavaScript, les tableaux peuvent être étendus dynamiquement en définissant une nouvelle valeur pour la propriété Length du tableau. Dans VBScript, les tableaux ne peuvent pas être agrandis ; elles doivent être redimensionnées à l’aide de l’instruction **ReDim** .

Les fonctions de prise en charge de VBScript et JavaScript. VBScript, toutefois, prend également en charge les sous-routines. Les sous-routines sont similaires aux fonctions, sauf qu’elles ne retournent pas de valeur.

JavaScript respecte la casse. VBScript n’est pas.

JavaScript est pris en charge par un large éventail de navigateurs Web, y compris Internet Explorer et Netscape Navigator. Netscape Navigator ne prend pas en charge VBScript.

VBScript prend en charge la gestion des erreurs via son objet Err. JavaScript ne fournit pas actuellement de méthode de recouvrement et de gestion des erreurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




