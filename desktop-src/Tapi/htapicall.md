---
description: Le type de données HTAPICALL représente le descripteur TAPI opaque pour une structure de données d’appel.
ms.assetid: a2a17b03-5779-411e-8959-6e2de5e53c5a
title: HTAPICALL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5157cc75773097c869384e303c7e386fce54d7c16ac2e2dc36d0495f766d5a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519188"
---
# <a name="htapicall"></a>HTAPICALL

Le type de données **HTAPICALL** représente le descripteur TAPI opaque pour une structure de données d’appel. L’interface TAPI doit résoudre une valeur de ce type en une référence à l’instance de structure de données appropriée. Le fournisseur de services ne doit pas tenter de faire référence à ce comme s’il s’agissait d’un pointeur, faire des suppositions sur ses valeurs ou interpréter sa représentation de quelque façon que ce soit en passant sa valeur à l’interface TAPI aux moments opportuns.

 

 



