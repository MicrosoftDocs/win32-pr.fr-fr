---
description: Spécifie la mise en cache d’un handle pour une imprimante ouverte avec OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Énumération PRINTER_OPTION_FLAGS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209786"
---
# <a name="printer_option_flags-enumeration"></a>\_Énumération d’indicateurs d’option d’imprimante \_

Spécifie la mise en cache d’un handle pour une imprimante ouverte avec [**OpenPrinter2**](openprinter2.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**OPTION d’imprimante \_ \_ sans \_ cache**
</dt> <dd>

Le descripteur n’est pas mis en cache. Toutes les fonctions appliquées à un handle retourné par [**OpenPrinter2**](openprinter2.md) seront dirigées vers l’ordinateur distant.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_cache des options d’imprimante \_**
</dt> <dd>

Le descripteur est mis en cache. Toutes les fonctions appliquées à un handle retourné par [**OpenPrinter2**](openprinter2.md) seront placées dans le cache local.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**OPTION d’imprimante \_ \_ modification du client \_**
</dt> <dd>

Le descripteur retourné par [**OpenPrinter2**](openprinter2.md) peut être utilisé par [**SetPrinter**](setprinter.md) pour renommer la connexion d’imprimante.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




