---
title: Conversion en JScript à partir de VBScript
description: Conversion en JScript à partir de VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671554"
---
# <a name="translating-to-jscript-from-vbscript"></a>Conversion en JScript à partir de VBScript

Dans VBScript **, le...** **Chaque** boucle énumère les membres d’une collection ; en JScript, le **pour**... **in** Loop énumère les membres d’un objet ou d’un tableau JScript. Pour énumérer une collection en JScript, utilisez un objet énumérateur.

En JScript, il existe plusieurs types de données, tels que des nombres, des chaînes, des valeurs booléennes, des objets et l’attribut null. VBScript utilise uniquement un type de données **Variant**, qui peut être sous-typé pour représenter des chaînes, des nombres, des valeurs booléennes, etc.

Dans JScript, les tableaux peuvent être étendus dynamiquement en définissant une nouvelle valeur pour la propriété Length du tableau. Dans VBScript, les tableaux ne peuvent pas être agrandis ; elles doivent être redimensionnées à l’aide de l’instruction **ReDim** .

Les fonctions de prise en charge de VBScript et de JScript. VBScript, toutefois, prend également en charge les sous-routines. Les sous-routines sont similaires aux fonctions, mais ne retournent pas de valeur.

JScript respecte la casse. VBScript n’est pas.

JScript est pris en charge par Internet Explorer et Netscape Navigator. Netscape Navigator ne prend pas en charge VBScript.

JScript fournit l’objet d’erreur, qui peut être utilisé pour intercepter et gérer les erreurs. L’objet Error est analogue à l’objet Err VBScript.

Les tableaux JScript ne sont pas des tableaux du type de variable **Variant SAFEARRAY**. Si votre script reçoit une variable **Variant SAFEARRAY** à partir d’un objet com ou d’un script VBScript, il doit utiliser un objet VBArray pour accéder à la variable de **type SAFEARRAY** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traduire en JScript](translating-to-jscript.md)
</dt> </dl>

 

 




