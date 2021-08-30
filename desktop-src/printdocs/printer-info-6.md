---
description: Les \_ informations sur l’imprimante \_ 6 spécifient la valeur d’état d’une imprimante.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: Structure PRINTER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 76255c563066ebcffde0fb2901426b186ec96504269842d286d2dc6ccca42ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947679"
---
# <a name="printer_info_6-structure"></a>\_Structure infos imprimante \_ 6

Les **\_ informations sur \_ l’imprimante 6** spécifient la valeur d’état d’une imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwStatus**
</dt> <dd>

État de l’imprimante. Ce membre peut être une combinaison raisonnable des valeurs suivantes.



| Valeur                               | Signification                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| État de l’imprimante \_ \_ occupé               | L'imprimante est occupée.                                                                                          |
| porte de l’état de l’imprimante \_ \_ \_ ouverte         | La porte de l’imprimante est ouverte.                                                                                     |
| \_erreur d’état de l’imprimante \_              | Non utilisé.                                                                                                     |
| État de l’imprimante en cours \_ \_ d’initialisation       | L'imprimante s'initialise.                                                                                  |
| \_e/s d’état d’imprimante \_ \_ active         | L’imprimante est dans un état d’entrée/sortie actif                                                                |
| \_ \_ flux manuel de l’état de l’imprimante \_       | L’imprimante est dans un état de flux manuel.                                                                        |
| État de l’imprimante \_ \_ non \_ toner          | L'imprimante est sans toner.                                                                                  |
| l’état de l’imprimante \_ \_ n’est pas \_ disponible     | L’imprimante n’est pas disponible pour l’impression.                                                                    |
| État de l’imprimante \_ \_ hors connexion            | L'imprimante est hors connexion.                                                                                       |
| \_ \_ mémoire insuffisante sur l’état \_ de \_ l’imprimante    | La mémoire de l’imprimante est insuffisante.                                                                            |
| bac de sortie de l’état de l’imprimante \_ \_ \_ \_ plein  | Le bac de sortie de l'imprimante est plein.                                                                             |
| PAGE État de l’imprimante \_ \_ \_ chargeur         | L’imprimante ne peut pas imprimer la page active.                                                                    |
| \_ \_ bourrage papier sur l’état de l’imprimante \_         | Le papier est coincé dans l’imprimante                                                                                |
| \_ \_ sortie papier de l’état de l’imprimante \_         | L’imprimante n’est plus imprimée.                                                                                  |
| \_ \_ problème papier sur l’état de l’imprimante \_     | L’imprimante présente un problème de papier.                                                                              |
| État de l’imprimante \_ \_ suspendu             | L’imprimante est suspendue.                                                                                        |
| État de l’imprimante \_ \_ en attente de \_ suppression  | L’imprimante est en attente de suppression suite à un appel à la fonction [**DeletePrinter**](deleteprinter.md) . |
| État de l’imprimante \_ \_ économie d’énergie \_        | L'imprimante est en mode mise en veille.                                                                            |
| \_impression de \_ l’état de l’imprimante           | L’imprimante est en cours d’impression.                                                                                      |
| traitement de l’état de l’imprimante \_ \_         | L’imprimante traite une commande à partir de la fonction [**SetPrinter**](setprinter.md) .                       |
| serveur d’état d’imprimante \_ \_ \_ inconnu    | L’état de l’imprimante est inconnu.                                                                                |
| \_toner d' \_ état \_ faible de l’imprimante         | L’imprimante manque de toner.                                                                                  |
| INTERVENTION de l’utilisateur sur l’état de l’imprimante \_ \_ \_ | L’imprimante a une erreur qui oblige l’utilisateur à effectuer une opération.                                              |
| État de l’imprimante en \_ \_ attente            | L’imprimante est en attente.                                                                                       |
| État de l’imprimante \_ \_ préchauffage \_        | L'imprimante s'allume.                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos sur \_ l’imprimante 6W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 6A** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
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
</dt> <dt>

[**\_Infos sur l’imprimante \_ 5**](printer-info-5.md)
</dt> </dl>

 

 




