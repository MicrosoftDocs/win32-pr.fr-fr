---
description: La \_ \_ structure des options de notification d’imprimante spécifie des options pour un objet de notification de modification qui surveille une imprimante ou un serveur d’impression.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: Structure PRINTER_NOTIFY_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536687"
---
# <a name="printer_notify_options-structure"></a>Structure des options de \_ notification d’imprimante \_

La structure des **\_ \_ options** de notification d’imprimante spécifie des options pour un objet de notification de modification qui surveille une imprimante ou un serveur d’impression.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Version de cette structure. Affectez la valeur 2 à ce membre.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Indicateur de bit. Si vous définissez l' \_ indicateur d' \_ actualisation des options \_ de notification d’imprimante dans un appel à la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) , la fonction fournit des données actuelles pour tous les champs d’informations d’imprimante surveillés. La fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ignore le membre **Flags** .

</dd> <dt>

**Count**
</dt> <dd>

Nombre d’éléments dans le tableau **pTypes** .

</dd> <dt>

**pTypes**
</dt> <dd>

Pointeur vers un tableau de structures [**de \_ \_ \_ type d’options de notification d’imprimante**](printer-notify-options-type.md) . Utilisez un élément de ce tableau pour spécifier les champs d’informations d’imprimante à surveiller, et un élément pour spécifier les champs d’informations de travail à analyser. Vous pouvez surveiller les informations de l’imprimante, les informations sur le travail ou les deux.

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez cette structure avec la fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) pour spécifier le jeu de champs d’informations sur les imprimantes ou les travaux à surveiller pour la modification.

Utilisez cette structure avec la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) pour demander les données actuelles pour tous les champs d’informations sur les imprimantes et les travaux analysés. Dans ce cas, le membre **indicateurs** spécifie l' \_ indicateur d’actualisation des options de notification d’imprimante \_ \_ , et la fonction ignore les autres membres de la structure.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_type d' \_ options de notification d’imprimante \_**](printer-notify-options-type.md)
</dt> </dl>

 

 




