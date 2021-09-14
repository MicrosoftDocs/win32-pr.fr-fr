---
title: Traduction en VBScript à partir de JScript
description: Traduction en VBScript à partir de JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095493"
---
# <a name="translating-to-vbscript-from-jscript"></a>Traduction en VBScript à partir de JScript

Dans VBScript **, le...** **Chaque** boucle énumère les membres d’une collection ; dans JScript, le **pour**... **in** loop énumère les membres d’un objet JScript ou d’un tableau. pour énumérer une collection dans JScript, utilisez un objet énumérateur.

JScript fournit l’objet d’erreur, qui peut être utilisé pour intercepter et gérer les erreurs. L’objet Error est analogue à l’objet Err VBScript.

dans JScript, il existe plusieurs types de données, tels que des nombres, des chaînes, des valeurs booléennes, des objets et l’attribut null. VBScript utilise uniquement un type de données **Variant**, qui peut être sous-typé pour représenter des chaînes, des nombres, des valeurs booléennes, etc.

dans JScript, les tableaux peuvent être étendus dynamiquement en définissant une nouvelle valeur pour la propriété length du tableau. Dans VBScript, les tableaux ne peuvent pas être agrandis ; elles doivent être redimensionnées à l’aide de l’instruction **ReDim** .

les fonctions de prise en charge de VBScript et de JScript. VBScript, toutefois, prend également en charge les sous-routines. Les sous-routines sont similaires aux fonctions, mais ne retournent pas de valeur.

JScript respecte la casse. VBScript n’est pas.

JScript est pris en charge par un large éventail de navigateurs Web, y compris Internet Explorer et Netscape Navigator. Netscape Navigator ne prend pas en charge VBScript.

les tableaux de JScript ne sont pas des tableaux du type de variable **VARIANT SAFEARRAY**. un script de JScript doit utiliser un objet VBArray pour accéder à la variable de **type SAFEARRAY**. Les scripts VBScript peuvent accéder directement à des variables de **type SAFEARRAY**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




