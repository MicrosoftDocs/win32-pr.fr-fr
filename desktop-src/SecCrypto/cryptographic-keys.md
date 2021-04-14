---
description: Les clés de chiffrement sont centrales aux opérations de chiffrement.
ms.assetid: dda7b527-1522-4b43-8d8e-44ce7983a9aa
title: Clés de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82858b26fa70ceacb4e7f9714e29983a773e66ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484617"
---
# <a name="cryptographic-keys"></a>Clés de chiffrement

Les [*clés de chiffrement*](../secgloss/c-gly.md) sont centrales aux opérations de chiffrement. De nombreux schémas de chiffrement sont constitués de paires d’opérations, telles que le chiffrement et le déchiffrement, la signature et la vérification. Une *clé* est un élément de données variables qui est chargé comme entrée dans un algorithme de chiffrement pour effectuer une opération de ce type. Dans un schéma de chiffrement bien conçu, la sécurité du schéma dépend uniquement de la sécurité des clés utilisées.

Les clés de chiffrement peuvent être classées en fonction de leur utilisation dans un schéma de chiffrement, sous la forme de [clés symétriques](symmetric-keys.md) ou de [clés asymétriques](public-private-key-pairs.md). Une [*clé symétrique*](../secgloss/s-gly.md) est une clé unique utilisée pour les deux opérations dans un schéma de chiffrement (par exemple, pour [*chiffrer*](../secgloss/e-gly.md) et [*déchiffrer*](../secgloss/d-gly.md) vos données). En règle générale, la sécurité du schéma dépend de s’assurer que la clé est uniquement connue des participants autorisés. En revanche, les clés asymétriques sont utilisées dans les schémas de chiffrement où différentes clés sont nécessaires pour chaque opération. Les exemples courants de tels modèles sont ceux qui utilisent des [*paires de clés publiques/privées*](../secgloss/p-gly.md), où la sécurité du schéma dépend de la garantie que la [*clé privée*](../secgloss/p-gly.md) est connue uniquement d’un tiers. Par exemple, les systèmes de chiffrement à clé publique/privée utilisent deux clés : une [*clé publique*](../secgloss/p-gly.md) que tout le monde peut utiliser pour chiffrer les données et une [*clé privée*](../secgloss/p-gly.md) que seul le destinataire autorisé possède et qui peut être utilisée pour déchiffrer les données.

Les clés de chiffrement peuvent être classées en fonction de l’objectif pour lequel elles sont utilisées. Ces utilisations incluent la génération de signature numérique, la vérification de signature numérique, l’authentification des messages, le chiffrement et le déchiffrement des données, le retour à la clé et le transport de clé. Pour obtenir la liste complète des types de clés tels que définis par le NIST ( [*National Institute of Standards and Technology*](../secgloss/n-gly.md) ), consultez la section 5 de l’aide générale sur la gestion des clés de la [publication spéciale de NIST 800-57 : recommandation pour la gestion des clés, partie 1 : général (révisé)](https://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf).

 

 
