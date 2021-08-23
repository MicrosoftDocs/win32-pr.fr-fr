---
description: La structure de l’imprimante \_ info \_ 5 spécifie des informations détaillées sur l’imprimante.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: Structure PRINTER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ef50f3bfd83a0c2dd49eb0a15cdae31f25588106926e606887292c705602dd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731420"
---
# <a name="printer_info_5-structure"></a>\_Structure des infos sur l’imprimante \_ 5

La structure de l' **imprimante \_ info \_ 5** spécifie des informations détaillées sur l’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a>Membres

<dl> <dt>

**pPrinterName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante.

</dd> <dt>

**pPortName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie le ou les ports utilisés pour transmettre des données à l’imprimante. Si une imprimante est connectée à plusieurs ports, les noms de chaque port doivent être séparés par des virgules (par exemple, « LPT1 :, LPT2 :, LPT3 : »).

</dd> <dt>

**Attributs**
</dt> <dd>

Attributs de l’imprimante. Ce membre peut être une combinaison raisonnable des valeurs suivantes.

| Valeur                                   | Signification                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| attribut d’imprimante \_ \_ direct              | Le travail est envoyé directement à l’imprimante (il n’est pas mis en file d’attente).                                                                                                                                |
| l’attribut d’imprimante se \_ \_ \_ termine en \_ premier | Si l’imprimante est définie et que l’imprimante est définie pour l’impression pendant la mise en file d’attente, toutes les tâches dont l’attente est terminée sont planifiées pour s’imprimer avant les travaux qui n’ont pas terminé la mise en attente.                          |
| attribut d’imprimante \_ \_ Enable \_ DEVQ        | Si cette valeur est définie, **DevQueryPrint** est appelé. **DevQueryPrint** peut échouer si les configurations du document et de l’imprimante ne correspondent pas. La définition de cet indicateur entraîne la conservation des documents incompatibles dans la file d’attente. |
| \_attribut imprimante \_ masqué              | Réservé.                                                                                                                                                                               |
| \_attribut Printer \_ KEEPPRINTEDJOBS     | Si cette valeur est définie, les tâches sont conservées après leur impression. S’il est désactivé, les travaux sont supprimés.                                                                                                               |
| \_attribut imprimante \_ local               | L’imprimante est une imprimante locale.                                                                                                                                                             |
| attribut d’imprimante \_ \_ réseau             | L’imprimante est une connexion d’imprimante réseau.                                                                                                                                                |
| \_attribut Printer \_ publié           | Indique si l’imprimante est publiée dans le service d’annuaire.                                                                                                                    |
| \_attribut d’imprimante en \_ file d’attente              | Si cette valeur est définie, l’imprimante est mise en file d’attente et commence l’impression une fois que la dernière page est mise en file d’attente. Si la valeur n’est pas définie et que \_ l’attribut Printer \_ direct n’est pas défini, l’imprimante met en attente et imprime pendant la mise en attente.      |
| attribut d’imprimante \_ \_ RAW \_ uniquement           | Indique que seuls les travaux d’impression de type de données brutes peuvent être mis en file d’attente.                                                                                                                            |
| attribut d’imprimante \_ \_ partagé              | L’imprimante est partagée.                                                                                                                                                                      |



 

dans Windows XP et les versions ultérieures de Windows, la valeur suivante peut également être utilisée.

| Valeur                   | Signification                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_télécopie d’attribut d’imprimante \_ | S’il est défini, l’imprimante est une imprimante-télécopieur. Cela ne peut être défini que par [**AddPrinter**](addprinter.md), mais il peut être récupéré par [**EnumPrinters**](enumprinters.md) et [**GetPrinter**](getprinter.md). |



 

dans Windows Vista et les versions ultérieures de Windows, les valeurs suivantes peuvent également être utilisées.

| Valeur                               | Signification                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| \_ \_ nom convivial de l’attribut d’imprimante \_  | Un ordinateur s’est connecté à cette imprimante et lui a donné un nom convivial.           |
| \_ordinateur d’attribut d’imprimante \_         | L’imprimante est une connexion par ordinateur.                                             |
| attribut d’imprimante \_ \_ Push \_ User    | L’imprimante a été installée à l’aide de la stratégie d’utilisateur envoyer des connexions d’imprimante.     |
| attribut d’imprimante, \_ \_ \_ ordinateur poussé | L’imprimante a été installée à l’aide de la stratégie de l’ordinateur Push Printer Connections. |



 

</dd> <dt>

**DeviceNotSelectedTimeout**
</dt> <dd>

Cette valeur n'est pas utilisée.

</dd> <dt>

**TransmissionRetryTimeout**
</dt> <dd>

Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos sur \_ l’imprimante 5W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 5A** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




