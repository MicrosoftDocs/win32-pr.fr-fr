---
title: Types de données de fonction et valeurs de retour
description: Types de données de fonction et valeurs de retour
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d85ed42a0751147a1a6a61a078ac0899ce0b5756467005fd02ec72d6190096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988314"
---
# <a name="function-data-types-and-return-values"></a>Types de données de fonction et valeurs de retour

Les fonctions et macros AVIFile utilisent des gestionnaires de fichiers et de flux implémentés avec la technologie OLE. Le type de données standard d’une fonction OLE est **STDAPI**, et la fonction retourne une valeur **HRESULT** (zéro en cas de réussite ou une erreur). Si une fonction retourne une valeur autre qu’un **HRESULT**, le type du prototype de la fonction a une syntaxe légèrement différente qui incorpore le type de valeur de retour entre parenthèses à la suite de « STDAPI \_ ». Par exemple, une fonction qui retourne une valeur de données de **type long** utilise **STDAPI \_ (long)** dans l’instruction prototype.

 

 




