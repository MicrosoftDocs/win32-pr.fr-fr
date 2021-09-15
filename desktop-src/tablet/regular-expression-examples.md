---
description: Les exemples suivants illustrent des expressions régulières d’écriture manuscrite que vous pouvez créer.
ms.assetid: b4954e05-64d0-434a-96fd-6185671252d0
title: Exemples d'expressions régulières
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe207be6378754bfe4b3e504d51e6ff49cadba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525301"
---
# <a name="regular-expression-examples"></a>Exemples d'expressions régulières

Les exemples suivants illustrent des expressions régulières d’écriture manuscrite que vous pouvez créer.



| Expression                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                               | Correspond à                                                                          | Non-correspondances                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------|
| s ( ! est \_ ONECHAR) + p<br/>                                                                                                                                                                                                                                                                | Correspond à tout mot qui commence par « s » en minuscules, contient un ou plusieurs caractères (comme défini par l' \_ étendue d’entrée ONECHAR) et se termine par un « p » en minuscules.<br/> | stop<br/> soupe<br/> schlep<br/> s234p<br/>               | Arrêter<br/> sp<br/>             |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/>                                                                                                                                                                                                                                                   | Correspond à n’importe quel chiffre unique, 1 à 9.<br/>                                                                                                                         | 1<br/> 6<br/> 0<br/>                                           | 42<br/> Une<br/>              |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9 \| , \| -) +<br/>                                                                                                                                                                                                                                            | Correspond à un ou plusieurs chiffres, virgules ou tirets. Utile pour limiter l’entrée à une plage ou à un ensemble de nombres, par exemple une plage de pages à imprimer.<br/>               | 1<br/> 1 à 6<br/> 2, 4, 7<br/> 2-6, 9135<br/> ,,,<br/> | Trois<br/> 7 à 9<br/>   |
| (0 1 2 3 4 5 6 7 8 9) (0 1 2 3 4 5 6 7 8 9) (0 1 2 3 4 5 6 7 8 9)-(0 1 2 3 4 5 6 7 8 9) (0 1 2 3 4 5 \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| 6 \| 7 \| 8 \| 9)-(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 9) \| (0 \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| \| 1 2 3 4 5 6 7 8 9) (0 1 2 3 4 5 6 7 8 9) (0 1 2 3 4 5 6 7 8 9)<br/> | Numéro de sécurité sociale. Le format d’un numéro de sécurité sociale est *nnn*  -  *nn*  -  *nnnn*.<br/>                                                                     | 123-45-6789<br/>                                                           | 12-123-12<br/> 12-2-3456<br/> |



 

 

 




