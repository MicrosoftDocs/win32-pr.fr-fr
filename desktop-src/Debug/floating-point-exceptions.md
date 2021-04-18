---
description: Par défaut, toutes les exceptions FP sont désactivées sur le système.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Exceptions de virgule flottante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519200"
---
# <a name="floating-point-exceptions"></a>Exceptions de virgule flottante

Par défaut, toutes les exceptions FP sont désactivées sur le système. Par conséquent, les calculs aboutissent à NAN ou à Infinity, plutôt qu’à une exception. Avant de pouvoir intercepter les exceptions à virgule flottante (FP) à l’aide de la gestion structurée des exceptions, vous devez appeler la fonction de la bibliothèque Runtime C [ \_ controlfp \_ ](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) pour activer toutes les exceptions FP possibles. Pour intercepter uniquement des exceptions particulières, utilisez uniquement les indicateurs qui correspondent aux exceptions à intercepter. Notez que tout gestionnaire d’erreurs FP doit appeler [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) comme première instruction FP. Cette fonction efface les exceptions à virgule flottante.

 

 
