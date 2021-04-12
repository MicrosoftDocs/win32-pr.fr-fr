---
description: Le type de données HTAPICALL représente le descripteur TAPI opaque pour une structure de données d’appel.
ms.assetid: a2a17b03-5779-411e-8959-6e2de5e53c5a
title: HTAPICALL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abd90dc8453be5f5bec18e92b384b7ace830d14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318689"
---
# <a name="htapicall"></a>HTAPICALL

Le type de données **HTAPICALL** représente le descripteur TAPI opaque pour une structure de données d’appel. L’interface TAPI doit résoudre une valeur de ce type en une référence à l’instance de structure de données appropriée. Le fournisseur de services ne doit pas tenter de faire référence à ce comme s’il s’agissait d’un pointeur, faire des suppositions sur ses valeurs ou interpréter sa représentation de quelque façon que ce soit en passant sa valeur à l’interface TAPI aux moments opportuns.

 

 



