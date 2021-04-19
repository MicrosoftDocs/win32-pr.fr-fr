---
title: Conversions de type de données
description: Conversions de type de données
ms.assetid: 54688ee9-2dd7-466b-b278-13d6f9d1e6ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8135a3fb86fda9ac9ab9666ec42991a8d04d9e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509880"
---
# <a name="data-type-conversions"></a>Conversions de type de données

Chaque langage de programmation définit certains types et conteneurs pour les données. La plupart de ces types de données, en particulier les primitives, sont facilement mappés à d’autres langages de programmation. Toutefois, certains types de données n’ont pas d’équivalent dans un autre langage et ne peuvent pas être convertis.

Pour obtenir des informations spécifiques sur les types de données non reconnus par votre langage de programmation, consultez les rubriques suivantes :

-   [Traduire en C++](translating-to-c--.md)
-   [Conversion en Visual Basic](translating-to-visual-basic.md)
-   [Conversion en Java](translating-to-java.md)

Le tableau suivant répertorie les conversions entre les langages de programmation pour les types de données courants.



| C++                                     | Visual Basic             | Java                               | Contient                                                                                       |
|-----------------------------------------|--------------------------|------------------------------------|------------------------------------------------------------------------------------------------|
| **signed char**<br/>              | Non pris en charge<br/> | **byte**<br/>                | entier signé sur 1 octet <br/> (VT \_ I1, \[ T \] )<br/>                                   |
| **unsigned char**<br/>            | **Byte**<br/>      | Non pris en charge<br/>           | entier non signé sur 1 octet <br/> (VT \_ UI1, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                 |
| **unsigned char**<br/>            | **Caractère**<br/> | **char**<br/>                | caractère Unicode sur 2 octets <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                          |
| **short**<br/>                    | **Integer**<br/>   | **short**<br/>               | entier signé sur 2 octets <br/> (VT \_ I2, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                    |
| **unsigned short**<br/>           | Non pris en charge<br/> | Non pris en charge<br/>           | entier non signé sur 2 octets <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                           |
| **int**<br/>                      | **Long**<br/>      | **int**<br/>                 | entier signé sur 4 octets <br/> (VT \_ I4, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                    |
| **nombre entier non signé**<br/>             | Non pris en charge<br/> | Non pris en charge<br/>           | entier non signé sur 4 octets <br/> (VT \_ UI4, \[ T \] \[ P \] )<br/>                           |
| **\_\_Int64**<br/>                | Non pris en charge<br/> | **long**<br/>                | entier signé sur 8 octets <br/> (VT \_ I8, \[ T \] \[ P \] )<br/>                              |
| **unsigned \_ \_ Int64**<br/>       | Non pris en charge<br/> | Non pris en charge<br/>           | entier non signé sur 8 octets <br/> (VT \_ UI8, \[ T \] \[ P \] )<br/>                           |
| **float**<br/>                    | **Unique**<br/>    | **float**<br/>               | nombre à virgule flottante sur 4 octets <br/> (VT \_ R4, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>             |
| **double**<br/>                   | **Double**<br/>    | **double**<br/>              | nombre à virgule flottante sur 8 octets <br/> (VT \_ R8, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>             |
| **BSTR**<br/>                     | **Chaîne**<br/>    | **Java. lang. String**<br/>    | Chaîne Automation <br/> (VT \_ BSTR, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                      |
| **Boolean**<br/>                     | **Booléen**<br/>   | **boolean**<br/>             | Boolean <br/> (VT \_ BOOL, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                                |
| **DIFFÉRENT**<br/>                  | **Différent**<br/>   | **com. ms. com. variant**<br/>  | VARIANTE EXTRÊME\* <br/> (VT \_ VARIANTE, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                       |
| [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)<br/> | **object**<br/>    | **com. ms. com. IUnknown**<br/> | Pointeur d’interface IDispatch <br/> (VT \_ DISPATCH, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>        |
| **DATE**<br/>                     | **Date**<br/>      | **com. ms. com. variant**<br/>  | Date <br/> (VT \_ DATE, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                                   |
| **CURRENCY**<br/>                 | **Devise**<br/>  | **com. ms. com. variant**<br/>  | Devise <br/> (VT \_ CY, \[ v \] \[ t \] \[ P \] \[ s \] ou VT \_ décimal, \[ v \] \[ t \] \[ S \] )<br/> |



 

Pour plus d’informations sur les valeurs VARTYPE et leur utilisation, consultez la rubrique [types de données et structures IDispatch](/previous-versions/ms221600(v=vs.100)).

Les conversions de types de données entre les langages de script sont plus simples que celles des langages de programmation. JScript et JavaScript prennent tous deux en charge les mêmes types de données, et VBScript ne prend en charge qu’un seul type de données, **Variant**. Ainsi, tous les types de données JScript et JavaScript deviennent des types **Variant** lorsqu’ils sont convertis en VBScript. Lorsque vous convertissez VBScript en JScript ou JavaScript, les types **Variant** deviennent des nombres, des chaînes, des valeurs booléennes, et ainsi de suite.

 

