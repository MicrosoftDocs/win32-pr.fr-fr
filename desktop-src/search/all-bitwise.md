---
description: TOUT au niveau du bit et certains mots clés au niveau du bit sont utilisés pour tester les bits dans un type intégral.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: Toutes les opérations de bits and au niveau du bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac133e04eae78fe9b943c1e354d9e4dcf451640ad60be1883eecc938ec1d418a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594719"
---
# <a name="all-bitwise-and-some-bitwise"></a>Toutes les opérations de bits and au niveau du bit

**Tout au niveau du bit** et certains mots clés au niveau du **bit** sont utilisés pour tester les bits dans un type intégral. Si tous les bits définis dans une propriété correspondent au masque, **tout le bit** est true. Si au moins l’un des bits définis dans une propriété correspond au masque, **une partie du bit** est vraie.

Les opérateurs peuvent être appliqués aux propriétés scalaires (à valeur unique) et aux propriétés vectorielles (valeurs multiples). L’exemple de code suivant montre comment tester des valeurs de propriété avec l' **opération de bits** and au **niveau du bit**.


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a>Opérateurs de comparaison

Les opérateurs de comparaison pris en charge pour les tests au niveau du bit sont répertoriés dans le tableau suivant.



| Opérateur de comparaison | Description  |
|---------------------|--------------|
| =                   | Égal à     |
| ! = ou <>      | Différent de |



 

La logique des tests au niveau du bit est indiquée dans le tableau suivant.



| Test de bits et opérateur de comparaison | Logique                   |
|--------------------------------------|-------------------------|
| = TOUTES LES OPÉRATIONS AU NIVEAU DU BIT                        | Propriété & Masque = Masque  |
| = UN OPÉRATEUR DE BITS                       | Masque de & de propriété ! = 0    |
| <> TOUTES LES OPÉRATIONS AU NIVEAU DU BIT                 | Masque de & de propriété ! = masque |
| <> UN OPÉRATEUR DE BITS                | Propriété & masque = 0     |



 

La table de vérité suivante utilise des exemples de valeurs binaires et hexadécimales pour expliquer la logique des tests au niveau du bit.



| Propriété en binaire (hex) | Masque en binaire (hex) | Propriété & masque = Binary (hex) | = UN OPÉRATEUR DE BITS | = TOUTES LES OPÉRATIONS AU NIVEAU DU BIT |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| 0001 (0x1)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0001 (0x1)               | 0011 (0x3)           | 0001 (0x1)                     | Vrai           | Faux         |
| 0011 (0x3)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0010 (0X2)               | 0001 (0x1)           | 0000 (0x0)                     | Faux          | False         |
| 11110000 (0xF0)          | 00000011 (0x03)      | 00000000 (0x00)                | Faux          | False         |
| 11110010 (0xF2)          | 11110010 (0xF2)      | 11110010 (0xF2)                | True           | True          |
| 11110010 (0xF2)          | 00000011 (0x03)      | 00000010 (0x02)                | Vrai           | Faux         |



 

## <a name="example"></a>Exemples

Voici un exemple de prédicat All au **niveau du bit** .


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



