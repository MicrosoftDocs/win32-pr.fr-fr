---
description: La \_ structure info 7 de l’imprimante \_ spécifie les informations d’imprimante des services d’annuaire.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: Structure PRINTER_INFO_7 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c8ba37176bb970883533be1e0ddcc47a09b164bf48767442f75096828c9bce5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867765"
---
# <a name="printer_info_7-structure"></a>\_Structure info 7 de l’imprimante \_

La **structure \_ info \_ 7** de l’imprimante spécifie les informations d’imprimante des services d’annuaire. Utilisez cette structure avec la fonction [**SetPrinter**](setprinter.md) pour publier les données d’une imprimante dans le service d’annuaire (DS), ou pour mettre à jour ou supprimer les données publiées de l’imprimante à partir du DS. Utilisez cette structure avec la fonction [**GetPrinter**](getprinter.md) pour déterminer si une imprimante est publiée dans le service d’annuaire.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a>Membres

<dl> <dt>

**pszObjectGUID**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le GUID de l’objet de file d’attente à l’impression du service d’annuaire associé à une imprimante publiée. Utilisez la fonction [**GetPrinter**](getprinter.md) pour récupérer ce GUID.

Avant d’appeler [**SetPrinter**](setprinter.md), affectez la valeur **null** à **pszObjectGUID** .

</dd> <dt>

**dwAction**
</dt> <dd>

Indique l’action à effectuer par la fonction [**SetPrinter**](setprinter.md) . Pour la fonction [**GetPrinter**](getprinter.md) , ce membre indique si l’imprimante spécifiée est publiée. Ce membre peut être une combinaison des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**DSPRINT \_ 0x80000000 en attente**</dt> <dt></dt> </dl>       | [**GetPrinter**](getprinter.md): indique que le système tente de terminer une opération de publication ou d’annulation de publication lancée par un appel [**SetPrinter**](setprinter.md) .<br/> [**SetPrinter**](setprinter.md): cette valeur n’est pas valide. <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**DSPRINT \_ PUBLIER**</dt> <dt>0x00000001</dt> </dl>       | [**SetPrinter**](setprinter.md): publie les données de l’imprimante dans le service d’annuaire.<br/> [**GetPrinter**](getprinter.md): indique que l’imprimante est publiée. <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**DSPRINT \_ Republier**</dt> <dt>0x00000008</dt> </dl> | [**SetPrinter**](setprinter.md): les données du service d’annuaire pour l’imprimante ne sont pas publiées, puis publiées à nouveau, ce qui a pour actualiser toutes les propriétés de l’imprimante publiée. La republication modifie également le GUID de l’imprimante publiée.<br/> [**GetPrinter**](getprinter.md): ne retourne jamais cette valeur. <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**DSPRINT \_ Annuler la publication**</dt> <dt>0x00000004</dt> </dl> | [**SetPrinter**](setprinter.md): supprime les données publiées de l’imprimante du service d’annuaire.<br/> [**GetPrinter**](getprinter.md): indique que l’imprimante n’est pas publiée. <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**DSPRINT \_ METTRE à jour**</dt> <dt>0x00000002</dt> </dl>          | [**SetPrinter**](setprinter.md): met à jour les données publiées de l’imprimante dans le service d’annuaire.<br/> [**GetPrinter**](getprinter.md): ne retourne jamais cette valeur. <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

La **structure \_ info \_ 7** de l’imprimante est utilisée dans un appel [**SetPrinter**](setprinter.md) pour publier des informations sur l’imprimante dans le service d’annuaire. Les données publiées incluent l’ensemble des valeurs et des données pour l’imprimante spécifiée, qui se trouvent sous la \_ clé de spouleur SPLDS \_ , la clé de \_ pilote SPLDS ou les clés de clé d' \_ \_ utilisateur SPLDS \_ créées par [**SetPrinterDataEx**](setprinterdataex.md).

Pour [**SetPrinter**](setprinter.md), *pszObjectGUID* doit avoir la valeur **null**. Pour [**GetPrinter**](getprinter.md), *PSZOBJECTGUID* retourne le GUID de l’objet file d’attente à l’impression des services d’annuaire associé à une imprimante publiée. Vous pouvez utiliser ce GUID avec les méthodes de l’interface Active Directory Services (ADSI) pour récupérer les données publiées pour l’imprimante. Toutefois, la méthode recommandée pour récupérer des données publiées consiste à appeler la fonction [**GetPrinterDataEx**](getprinterdataex.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos sur \_ l’imprimante 7W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 7A** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




