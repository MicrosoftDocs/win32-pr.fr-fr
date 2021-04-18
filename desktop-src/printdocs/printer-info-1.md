---
description: La \_ structure infos imprimante \_ 1 spécifie des informations générales sur l’imprimante.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: Structure PRINTER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519372"
---
# <a name="printer_info_1-structure"></a>\_Structure infos imprimante \_ 1

La **structure \_ infos imprimante \_ 1** spécifie des informations générales sur l’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**Indicateurs**
</dt> <dd>

Spécifie des informations sur les données retournées. Voici les valeurs de ce membre.



| Valeur                    | Signification                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_étendre l’énumération de l’imprimante \_    | Un fournisseur d’impression peut définir cet indicateur comme indicateur pour une application appelante afin d’énumérer plus précisément cet objet si l’extension par défaut est activée. Par exemple, lorsque des domaines sont énumérés, un fournisseur d’impression peut indiquer le domaine de l’utilisateur en définissant cet indicateur. |
| \_conteneur d’énumération d’imprimante \_ | Si cet indicateur est défini, l’objet Printer peut contenir des objets énumérables. Par exemple, l’objet peut être un serveur d’impression qui contient des imprimantes.                                                                                                             |
| \_ICON1 d’énumération d’imprimante \_     | Indique que, le cas échéant, une application doit afficher une icône identifiant l’objet comme un nom de réseau de niveau supérieur, tel que réseau Microsoft Windows.                                                                                           |
| \_ICON2 d’énumération d’imprimante \_     | Indique que, le cas échéant, une application doit afficher une icône qui identifie l’objet en tant que domaine réseau.                                                                                                                                  |
| \_ICON3 d’énumération d’imprimante \_     | Indique que, le cas échéant, une application doit afficher une icône qui identifie l’objet en tant que serveur d’impression.                                                                                                                                    |
| \_ICON4 d’énumération d’imprimante \_     | Réservé.                                                                                                                                                                                                                                                 |
| \_ICON5 d’énumération d’imprimante \_     | Réservé.                                                                                                                                                                                                                                                 |
| \_ICON6 d’énumération d’imprimante \_     | Réservé.                                                                                                                                                                                                                                                 |
| \_ICON7 d’énumération d’imprimante \_     | Réservé.                                                                                                                                                                                                                                                 |
| \_ICON8 d’énumération d’imprimante \_     | Indique que, le cas échéant, une application doit afficher une icône qui identifie l’objet en tant qu’imprimante.                                                                                                                                         |



 

</dd> <dt>

**pDescription**
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère null qui décrit le contenu de la structure.

</dd> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui nomme le contenu de la structure.

</dd> <dt>

**pComment**
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère null qui contient des données supplémentaires qui décrivent la structure.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos imprimante \_ 1s** (Unicode) et **\_ \_ infos imprimante \_ 1a** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




