---
description: La structure des informations de \_ notification \_ d’imprimante contient les informations d’imprimante retournées par la fonction FindNextPrinterChangeNotification. La fonction retourne ces informations après qu’une opération d’attente sur un objet de notification de modification d’imprimante a été satisfaite.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: Structure PRINTER_NOTIFY_INFO (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533940"
---
# <a name="printer_notify_info-structure"></a>Structure des informations de \_ notification de l’imprimante \_

La structure des informations de **\_ notification \_ d’imprimante** contient les informations d’imprimante retournées par la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) . La fonction retourne ces informations après qu’une opération d’attente sur un objet de notification de modification d’imprimante a été satisfaite.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Version de cette structure. Affectez la valeur 2 à ce membre.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Indicateur binaire qui indique l’état de la structure de notification. Si le \_ bit d’informations sur la notification d’imprimante \_ \_ ignoré est défini, cela indique que certaines notifications devaient être ignorées.

</dd> <dt>

**Count**
</dt> <dd>

Nombre d’éléments [**de \_ \_ \_ données d’informations de notification d’imprimante**](printer-notify-info-data.md) dans le tableau **adatuma** .

</dd> <dt>

**Adatum**
</dt> <dd>

Tableau de structures [**de \_ \_ \_ données d’informations de notification d’imprimante**](printer-notify-info-data.md) . Chaque élément du tableau identifie un champ de travail unique ou un champ d’informations d’imprimante, et fournit les données actuelles pour ce champ.

</dd> </dl>

## <a name="remarks"></a>Notes

Si le membre **Flags** comporte l' \_ \_ ensemble de bits d’informations de notification d’imprimante \_ , cela indique qu’un dépassement de capacité ou une erreur s’est produite et que des notifications ont peut-être été perdues. Dans ce cas, vous devez appeler [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) et spécifier l' \_ \_ \_ indicateur d’actualisation des options de notification d’imprimante pour récupérer toutes les informations actuelles. Tant que vous n’avez pas demandé cette opération d’actualisation, le système n’envoie pas de notifications supplémentaires pour cet objet de notification de modification.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_données d' \_ informations de notification d’imprimante \_**](printer-notify-info-data.md)
</dt> </dl>

 

 




