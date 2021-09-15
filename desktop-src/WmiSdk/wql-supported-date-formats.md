---
description: Décrit les formats de date pris en charge pour une utilisation dans la clause WHERE WQL.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: Formats de date de WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530177"
---
# <a name="wql-supported-date-formats"></a>Formats de date de WQL-Supported

Outre le format **DateTime** WMI, les formats de date suivants sont pris en charge pour une utilisation dans **la clause WQL** WQL.

Le format d’heure affiché diffère selon les différents paramètres régionaux. Les scripts qui se connectent à des ordinateurs distants doivent spécifier l’heure au format approprié pour les paramètres régionaux de l’ordinateur cible.

Par exemple, le États-Unis format de date et d’heure est MM-jj-aaaa. Si un script sur un ordinateur américain se connecte à un ordinateur cible dont le format est JJ-MM-AAAA, les requêtes sont traitées sur l’ordinateur cible sous la forme JJ-MM-AAAA. Pour éviter des résultats différents entre les paramètres régionaux, utilisez le format [**DateTime**](datetime.md) . Pour plus d’informations, consultez [format de date et d’heure](date-and-time-format.md).



<table>
<thead>
<tr class="header">
<th>Format</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mois [th] JJ [,] [AA] AA</td>
<td>Mois (en lettres ou abrégées en trois lettres), jour, virgule facultative et année sur deux ou quatre chiffres.<br/> <dl> 21 janvier 1932<br />
21 janvier 32<br />
21 1932 janvier<br />
21 32 janvier<br />
</dl></td>
</tr>
<tr class="even">
<td>Mois [th] [,] aaaa</td>
<td>Mois (à l’aide de l’orthographe ou de l’abréviation de trois lettres), de la virgule facultative et de l’année à quatre chiffres.<br/> <dl> 1932 janvier<br />
1932 janvier<br />
</dl></td>
</tr>
<tr class="odd">
<td>Mois [th] [AA] aa jj</td>
<td>Mois (en lettres ou abrégées en trois lettres), année à deux ou quatre chiffres et jour.<br/> <dl> 1932 21 janvier<br />
32 21 janvier<br />
</dl></td>
</tr>
<tr class="even">
<td>JJ mois [th] [,] [] [AA] AA</td>
<td>Jour du mois, mois (à l’aide d’un caractère épelé ou abrégé en trois lettres), virgule facultative, espace facultatif et année sur deux ou quatre chiffres.<br/> <dl> 21 janvier, 1932<br />
21 Jan32<br />
</dl></td>
</tr>
<tr class="odd">
<td>JJ [AA] YY mois [th]</td>
<td>Jour du mois, année sur deux ou quatre chiffres et mois (à l’aide d’un caractère épelé ou abrégé en trois lettres).<br/> <dl> 21 1932 janvier<br />
</dl></td>
</tr>
<tr class="even">
<td>[YY] YY mois [th] JJ</td>
<td>Année sur deux ou quatre chiffres, mois (à l’aide d’une orthographe ou d’une abréviation en trois lettres) et jour.<br/> <dl> 1932 janvier 21<br />
</dl></td>
</tr>
<tr class="odd">
<td>aaaa mois [th]</td>
<td>Année et mois sur deux ou quatre chiffres (à l’aide d’un caractère épelé ou abrégé en trois lettres).<br/> <dl> 1932 Jan<br />
</dl></td>
</tr>
<tr class="even">
<td>AAAA JJ mois [th]</td>
<td>Année, jour et mois à deux ou quatre chiffres (à l’aide d’un caractère épelé ou abrégé en trois lettres).<br/> <dl> 1932 21 janvier<br />
</dl></td>
</tr>
<tr class="odd">
<td>Lecteur M {/-.} JJ {/-.} [AA] AA</td>
<td>Mois, jour et année sur deux ou quatre chiffres. Notez que les séparateurs doivent être identiques.<br/></td>
</tr>
<tr class="even">
<td>JJ {/-.} Lecteur M {/-.} [AA] AA</td>
<td>Jour du mois, du mois et de l’année sur deux ou quatre chiffres. Notez que les séparateurs doivent être identiques.<br/></td>
</tr>
<tr class="odd">
<td>Lecteur M {/-.} [YY] yy {/-.} JJ</td>
<td>Mois, année à deux ou quatre chiffres, et jour. Notez que les séparateurs doivent être identiques.<br/></td>
</tr>
<tr class="even">
<td>JJ {/-.} [YY] yy {/-.} Lecteur Lecteur</td>
<td>Jour du mois, année sur deux ou quatre chiffres et mois. Notez que les séparateurs doivent être identiques.<br/></td>
</tr>
<tr class="odd">
<td>[YY] yy {/-.} JJ {/-.} Lecteur Lecteur</td>
<td>Année, jour et mois à deux ou quatre chiffres. Notez que les séparateurs doivent être identiques.<br/></td>
</tr>
<tr class="even">
<td>[YY] yy {/-.} Lecteur M {/-.} JJ</td>
<td>Année, mois et jour deux ou quatre chiffres. Notez que les séparateurs doivent être identiques.<br/></td>
</tr>
<tr class="odd">
<td>[YY] AAMMJJ</td>
<td>Année, mois et jour deux ou quatre chiffres, sans espaces.<br/></td>
</tr>
<tr class="even">
<td>YYYY [MM [JJ]]</td>
<td>Année à deux ou quatre chiffres, mois facultatif et jour facultatif, sans espaces.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clause WHERE](where-clause.md)
</dt> </dl>

 

 




