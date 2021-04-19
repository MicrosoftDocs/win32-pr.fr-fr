---
title: Verbe
description: Spécifie les verbes à inscrire pour une application.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Clé de Registre Verb COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106530798"
---
# <a name="verb"></a>Verbe

Spécifie les verbes à inscrire pour une application.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a>Notes

Chaque verbe est une **valeur \_ reg SZ** au format «*nom*, *\_ indicateur de menu*, *\_ indicateur de verbe*». Les verbes doivent être numérotés de manière consécutive.

Le *nom* décrit comment le verbe est ajouté par un appel de fonction [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) . Par exemple, « &Play ».

La valeur de l' *\_ indicateur de menu* indique comment le verbe doit apparaître dans le menu. Tous les indicateurs pris en charge par [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) sont pris en charge, à l’exception des \_ bitmaps MF, MF \_ OwnerDraw et MF \_ .

La valeur de l' *\_ indicateur de verbe* décrit les attributs des verbes. Utilisez l’une des valeurs de [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib), ou 0.

Pour plus d’informations, consultez [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject ::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)et [**IOleObject :: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 