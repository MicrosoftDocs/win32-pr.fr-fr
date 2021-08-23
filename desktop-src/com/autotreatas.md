---
title: Traitement autotraité
description: Définit automatiquement le CLSID de la clé TreatAs sur la valeur spécifiée.
ms.assetid: 5adf7bc5-a4d6-444d-bd56-0c4e6eee5111
keywords:
- Clé de Registre autotraitéas COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196e389780d75c0e33a20775df6e087b130e11453d5335130003bc2f0611f726
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731629"
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

 

 




