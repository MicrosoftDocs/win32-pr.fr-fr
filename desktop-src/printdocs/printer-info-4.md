---
description: La structure de l’imprimante \_ info \_ 4 spécifie des informations générales sur l’imprimante. La structure peut être utilisée pour récupérer des informations d’imprimante minimales sur un appel à EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: Structure PRINTER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204228"
---
# <a name="printer_info_4-structure"></a>Structure de l’imprimante \_ info \_ 4

La structure de l' **imprimante \_ info \_ 4** spécifie des informations générales sur l’imprimante.

La structure peut être utilisée pour récupérer des informations d’imprimante minimales sur un appel à [**EnumPrinters**](enumprinters.md). Un tel appel est un moyen simple et rapide de récupérer les noms et les attributs de toutes les imprimantes installées localement sur un système et toutes les connexions d’imprimante distantes qu’un utilisateur a établies.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a>Membres

<dl> <dt>

**pPrinterName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante (locale ou distante).

</dd> <dt>

**pServerName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui est le nom du serveur.

</dd> <dt>

**Attributs**
</dt> <dd>

Spécifie des informations sur les données retournées.



| Valeur                       | Signification                          |
|-----------------------------|----------------------------------|
| \_attribut imprimante \_ local   | L’imprimante est une imprimante locale.  |
| attribut d’imprimante \_ \_ réseau | L’imprimante est une imprimante distante. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La structure **Printer \_ info \_ 4** offre un moyen simple et extrêmement rapide de récupérer les noms des imprimantes installées sur un ordinateur local, ainsi que les connexions distantes qu’un utilisateur a établies. Quand [**EnumPrinters**](enumprinters.md) est appelé avec une structure de données **Printer \_ info \_ 4** , cette fonction interroge le registre pour obtenir les informations spécifiées, puis retourne immédiatement. Cela diffère du comportement de **EnumPrinters** lorsqu’il est appelé avec d’autres niveaux de structures de données d' **informations d’imprimante \_ \_ xxx** . En particulier, quand **EnumPrinters** est appelé avec une structure de données de niveau 2 (**Printer \_ info \_ 2** ), il effectue un appel **OpenPrinter** sur chaque connexion à distance. Si une connexion distante est interrompue, si le serveur distant n’existe plus, ou si l’imprimante distante n’existe plus, la fonction doit attendre l’expiration du délai d’attente de RPC et, par conséquent, échouer l’appel **OpenPrinter** . Cette opération peut prendre du temps. Le passage d’une structure **Printer \_ info \_ 4** permet à une application de récupérer un minimum d’informations requises ; si des informations plus détaillées sont souhaitées, un appel **EnumPrinter** de niveau 2 suivant peut être effectué.

Les **attributs** peuvent également contenir des valeurs définies dans le champ **attributs** de **Printer \_ info \_ 2**.

Certaines configurations d’imprimante, telles que les connexions d’imprimante à certains serveurs d’impression non Windows, peuvent renvoyer à la fois l’attribut d' **imprimante \_ \_ local** et l' **\_ attribut Printer \_ réseau**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos sur \_ l’imprimante 4W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 4a** (ANSI)<br/>                           |



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

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 3**](printer-info-3.md)
</dt> </dl>

 

 




