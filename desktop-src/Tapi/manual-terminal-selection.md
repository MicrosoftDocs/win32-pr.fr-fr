---
description: Si les règles de sélection par défaut ne répondent pas aux besoins de l’application, l’application a la possibilité de sélectionner le terminal manuellement.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Sélection manuelle des terminaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6eaa1e0a5b8b53b1037c51b0e628d7a27ece0be65a0f9a7e86e882c722360f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514639"
---
# <a name="manual-terminal-selection"></a>Sélection manuelle des terminaux

Si les règles de la sélection par défaut ne répondent pas aux besoins de l’application, l’application a la possibilité de sélectionner le terminal tel qu’il a toujours : autrement dit, il peut utiliser [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) pour énumérer les flux présents sur l’appel et sélectionner le terminal sur les flux appropriés (ou, dans le cas des terminaux multipiste, créer des pistes pour les flux et sélectionner des pistes créées sur les flux

 

 
