---
description: Pour les constantes de données scalaires extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs dans une plage spécifiée.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Constantes de données scalaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3187d2064501727614dfcbf0b8e11c136fea13e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414682"
---
# <a name="scalar-data-constants"></a>Constantes de données scalaires

Pour les constantes de données scalaires extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs dans une plage spécifiée. Étant donné que la plupart des constantes de données sont **DWORD** s, la plage comprise entre 0X00000000 et 0x7FFFFFFF est généralement réservée aux extensions futures courantes, tandis que 0X80000000 à 0xFFFFFFFF est disponible pour les extensions spécifiques au fournisseur. L’hypothèse est qu’un fournisseur définit des valeurs qui sont des extensions naturelles des types de données définis par l’API.

 

 



