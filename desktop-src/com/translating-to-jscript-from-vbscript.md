---
title: conversion en JScript à partir de VBScript
description: conversion en JScript à partir de VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221601"
---
# <a name="translating-to-jscript-from-vbscript"></a>conversion en JScript à partir de VBScript

Dans VBScript **, le...** **Chaque** boucle énumère les membres d’une collection ; dans JScript, le **pour**... **in** loop énumère les membres d’un objet JScript ou d’un tableau. pour énumérer une collection dans JScript, utilisez un objet énumérateur.

dans JScript, il existe plusieurs types de données, tels que des nombres, des chaînes, des valeurs booléennes, des objets et l’attribut null. VBScript utilise uniquement un type de données **Variant**, qui peut être sous-typé pour représenter des chaînes, des nombres, des valeurs booléennes, etc.

dans JScript, les tableaux peuvent être étendus dynamiquement en définissant une nouvelle valeur pour la propriété length du tableau. Dans VBScript, les tableaux ne peuvent pas être agrandis ; elles doivent être redimensionnées à l’aide de l’instruction **ReDim** .

les fonctions de prise en charge de VBScript et de JScript. VBScript, toutefois, prend également en charge les sous-routines. Les sous-routines sont similaires aux fonctions, mais ne retournent pas de valeur.

JScript respecte la casse. VBScript n’est pas.

JScript est pris en charge par Internet Explorer et Netscape Navigator. Netscape Navigator ne prend pas en charge VBScript.

JScript fournit l’objet d’erreur, qui peut être utilisé pour intercepter et gérer les erreurs. L’objet Error est analogue à l’objet Err VBScript.

les tableaux de JScript ne sont pas des tableaux du type de variable **VARIANT SAFEARRAY**. Si votre script reçoit une variable **Variant SAFEARRAY** à partir d’un objet com ou d’un script VBScript, il doit utiliser un objet VBArray pour accéder à la variable de **type SAFEARRAY** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en JScript](translating-to-jscript.md)
</dt> </dl>

 

 




