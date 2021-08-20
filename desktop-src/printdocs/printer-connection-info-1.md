---
description: Représente des informations sur une connexion à une imprimante.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: Structure PRINTER_CONNECTION_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b9adbe18d3f75062a67440fd7f7586c4336323ff3035416f3ad9799f5e34a17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033897"
---
# <a name="printer_connection_info_1-structure"></a>Structure d’informations de connexion d’imprimante \_ \_ \_ 1

Représente des informations sur une connexion à une imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwFlags**
</dt> <dd>

Les valeurs suivantes sont définies :



| Valeur                                      | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Non-concordance de la connexion à l’imprimante \_ \_ (0x00000020) | Si cet indicateur de bit est défini, la connexion à l’imprimante n’est pas compatible. L’utilisateur peut fournir un pilote d’impression local en tant que *pszDriverName* et l’utiliser pour effectuer le rendu au lieu d’utiliser le pilote installé sur l’imprimante serveur à laquelle l’utilisateur est connecté.<br/>                                                                                                                                                                                                                                    |
| \_ \_ \_ Interface utilisateur de connexion à l’imprimante (0x00000040)   | Si cet indicateur de bit est défini, cet appel ne peut pas afficher une boîte de dialogue. Si une boîte de dialogue doit être affichée pour installer un pilote d’imprimante à partir du serveur et que cet indicateur de bit est défini, le pilote d’imprimante n’est pas installé, la connexion d’imprimante n’est pas ajoutée et l’appel échoue.<br/> **Windows 7 :** dans Windows 7 et les versions ultérieures de Windows, si cet indicateur est défini et que l’utilisateur s’exécute en mode élevé, la boîte de dialogue **faites-vous confiance à cette imprimante ?** ne s’affichera pas.<br/> |



 

</dd> <dt>

**pszDriverName**
</dt> <dd>

Pointeur vers le nom du pilote.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




