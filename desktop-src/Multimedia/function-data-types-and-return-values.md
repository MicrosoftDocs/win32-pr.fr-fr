---
title: Types de données de fonction et valeurs de retour
description: Types de données de fonction et valeurs de retour
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368940"
---
# <a name="function-data-types-and-return-values"></a>Types de données de fonction et valeurs de retour

Les fonctions et macros AVIFile utilisent des gestionnaires de fichiers et de flux implémentés avec la technologie OLE. Le type de données standard d’une fonction OLE est **STDAPI**, et la fonction retourne une valeur **HRESULT** (zéro en cas de réussite ou une erreur). Si une fonction retourne une valeur autre qu’un **HRESULT**, le type du prototype de la fonction a une syntaxe légèrement différente qui incorpore le type de valeur de retour entre parenthèses à la suite de « STDAPI \_ ». Par exemple, une fonction qui retourne une valeur de données de **type long** utilise **STDAPI \_ (long)** dans l’instruction prototype.

 

 




