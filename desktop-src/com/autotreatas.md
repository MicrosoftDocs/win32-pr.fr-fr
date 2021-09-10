---
title: Traitement autotraité
description: Définit automatiquement le CLSID de la clé TreatAs sur la valeur spécifiée.
ms.assetid: 5adf7bc5-a4d6-444d-bd56-0c4e6eee5111
keywords:
- Clé de Registre autotraitéas COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9ff717e17f08e5d37885f3994d03671bddaa9c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363423"
---
# <a name="autotreatas"></a>Traitement autotraité

Définit automatiquement le CLSID de la clé [**TreatAs**](treatas.md) sur la valeur spécifiée.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoTreatAs = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie l’identificateur de classe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CoTreatAsClass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




