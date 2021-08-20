---
description: La \_ \_ \_ structure de type options de notification d’imprimante spécifie le jeu de champs d’informations d’imprimante ou de travail à surveiller par un objet de notification de modification d’imprimante. Un appel à la fonction FindFirstPrinterChangeNotification spécifie une \_ \_ structure d’options Notify d’imprimante, qui contient un tableau de structures de types d’options de notification d’imprimante \_ \_ \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: Structure PRINTER_NOTIFY_OPTIONS_TYPE (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2b593a502a668345cdd0206b4f1363cf160074b6c9aa26696427b5b42a0fbdc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056276"
---
# <a name="printer_notify_options_type-structure"></a>\_Structure de \_ type des options de notification d’imprimante \_

La structure de **\_ \_ \_ type options de notification d’imprimante** spécifie le jeu de champs d’informations d’imprimante ou de travail à surveiller par un objet de notification de modification d’imprimante.

Un appel à la fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) spécifie une structure d' [**\_ \_ options Notify d’imprimante**](printer-notify-options.md) , qui contient un tableau de structures de **\_ \_ \_ types d’options de notification d’imprimante** .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Type à suivre. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                      | Signification                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Travail \_ \_Type de notification**</dt> <dt>0x01</dt> </dl>             | Indique que les champs spécifiés dans le tableau **pFields** sont \_ des \_ constantes de champ de notification de travail \_ \* .<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Imprimante \_ \_Type de notification**</dt> <dt>0x00</dt> </dl> | Indique que les champs spécifiés dans le tableau **pFields** sont \_ des \_ constantes de champ de notification d’imprimante \_ \* .<br/> |



 

</dd> <dt>

**Reserved0**
</dt> <dd>

Réservé.

</dd> <dt>

**Reserved1**
</dt> <dd>

Réservé.

</dd> <dt>

**Réservé 2**
</dt> <dd>

Réservé.

</dd> <dt>

**Count**
</dt> <dd>

Nombre d’éléments dans le tableau **pFields** .

</dd> <dt>

**pFields**
</dt> <dd>

Pointeur vers un tableau de valeurs. Chaque élément du tableau spécifie un champ d’information de travail ou d’imprimante qui vous intéresse. Pour obtenir la liste des champs d’informations sur les imprimantes et les travaux pris en charge, consultez la structure des [**\_ \_ \_ données de notification d’imprimante**](printer-notify-info-data.md) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**\_données d' \_ informations de notification d’imprimante \_**](printer-notify-info-data.md)
</dt> <dt>

[**\_options de notification d’imprimante \_**](printer-notify-options.md)
</dt> </dl>

 

 




