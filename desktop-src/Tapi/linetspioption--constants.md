---
description: Les \_ constantes LINETSPIOPTION décrivent les fournisseurs de service de commande qui doivent être appelés.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Constantes LINETSPIOPTION_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5d4a57edd80a83ab442313706fd40a2fbd79f545a0b3e9485e5d8c88b8c2f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404853"
---
# <a name="linetspioption_-constants"></a>\_Constantes LINETSPIOPTION

Les **\_ constantes LINETSPIOPTION** décrivent les fournisseurs de service de commande qui doivent être appelés.

<dl> <dt>

<span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**
</dt> <dd> <dl> <dt>



L’interface TAPI doit appeler les fonctions de ce fournisseur de services une à la fois ; il doit attendre que chaque fonction retourne (mais pas pour que les fonctions asynchrones se terminent) avant d’appeler la même fonction ou une autre fonction, sur le même thread ou sur un autre, sur le même processeur ou sur un processeur différent.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




