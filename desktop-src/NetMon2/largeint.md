---
description: Le type de données LARGEINT définit une \_ valeur entière de type long.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (NetMon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517336"
---
# <a name="largeint"></a>LARGEINT

Le type de données **LARGEINT** définit une valeur [**entière de \_ type long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) .


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>Notes

Le membre **lpLargeIntTable** de la structure [**Set**](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent une ou plusieurs valeurs LARGEINT. Lorsque ce type de structure de **jeu** est spécifié, moniteur réseau affiche l’une des étiquettes suivantes avec chaque valeur LARGEINT trouvée dans le paquet de protocole.

-   Correspond à la valeur définie. La valeur LARGEINT est incluse dans le jeu.
-   Valeur définie inconnue. La valeur LARGEINT n’est pas incluse dans le jeu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

