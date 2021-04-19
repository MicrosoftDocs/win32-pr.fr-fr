---
description: La \_ structure par défaut de l’imprimante spécifie le type de données par défaut, l’environnement, les données d’initialisation et les droits d’accès d’une imprimante.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: Structure PRINTER_DEFAULTS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534333"
---
# <a name="printer_defaults-structure"></a>\_Structure par défaut de l’imprimante

La **structure \_ par défaut** de l’imprimante spécifie le type de données par défaut, l’environnement, les données d’initialisation et les droits d’accès d’une imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a>Membres

<dl> <dt>

**pDatatype**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données par défaut pour une imprimante.

</dd> <dt>

**pDevMode**
</dt> <dd>

Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui identifie l’environnement par défaut et les données d’initialisation d’une imprimante.

</dd> <dt>

**DesiredAccess**
</dt> <dd>

Spécifie les droits d’accès souhaités pour une imprimante. La fonction [**OpenPrinter**](openprinter.md) utilise ce membre pour définir les droits d’accès à l’imprimante. Ces droits peuvent affecter le fonctionnement des fonctions [**SetPrinter**](setprinter.md) et [**DeletePrinter**](deleteprinter.md) . Les droits d’accès peuvent être l’un des suivants :



| Valeur                                       | Signification                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_administration de l’accès aux imprimantes \_                 | Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md).                                                                                                 |
| \_utilisation de l’accès à l’imprimante \_                        | Pour effectuer des opérations d’impression de base.                                                                                                                                                        |
| \_gestion de l’accès à l’imprimante \_ \_ limitée            | Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md) et [**SetPrinterData**](setprinterdata.md). Cette valeur est disponible à partir de Windows 8.1. |
| \_tout \_ accès imprimante                        | Pour effectuer toutes les tâches d’administration et les opérations d’impression de base, à l’exception de la synchronisation (voir [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights) ).                                   |
| valeurs de sécurité génériques, telles que WRITE \_ DAC | Pour autoriser des droits d’accès de contrôle spécifiques. Consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ DEFAULTSW d’imprimante** (Unicode) et **\_ \_ Erreurs d’imprimante** (ANSI)<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

