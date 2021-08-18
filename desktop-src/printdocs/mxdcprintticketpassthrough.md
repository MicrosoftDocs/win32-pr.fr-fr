---
description: La \_ structure MXDC PRINTTICKET \_ Data \_ T contient un ticket d’impression de document XPS, qui contient les paramètres d’imprimante et de travail d’impression, à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: Structure MXDC_PRINTTICKET_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 3cf778781340323a78495f87b1408e1011641797ed52a3565bafe41ca450d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471640"
---
# <a name="mxdc_printticket_data_t-structure"></a>\_Structure de \_ données MXDC PRINTTICKET \_

La structure **MXDC \_ PRINTTICKET \_ Data \_ T** contient un ticket d’impression de document XPS, qui contient les paramètres d’imprimante et de travail d’impression, à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwDataSize**
</dt> <dd>

Taille du ticket d’impression en octets.

</dd> <dt>

**bData**
</dt> <dd>

Ticket d’impression du document XPS.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est ajoutée à une structure [**\_ T d' \_ en \_ -tête d’échappement MXDC**](mxdcescapeheader.md) dont le membre **opcode** est défini sur la **\_ \_ \_ page fixe MXDCOP PrintTicket**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** ou **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq** pour créer une structure [**MXDC \_ PrintTicket \_ Escape \_ T**](mxdcprintticketescape.md) . La **structure \_ MXDC \_ PRINTTICKET \_ Escape T** est ensuite transmise au paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quand elle est appelée avec l’échappement d' [**\_ échappement MXDC**](mxdc-escape.md) . L’effet est d’écrire le ticket d’impression dans le fichier de document XPS.

Si l' **opcode** est défini sur **la \_ \_ \_ page fixe MXDCOP PRINTTICKET**, l’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). Si le **opcode** défini sur **MXDCOP \_ PrintTicket \_ fixed \_ doc** ou **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, l’appel à **ExtEscape** doit se produire entre un appel à [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) et un appel à [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ échappement**](mxdc-escape.md)
</dt> </dl>

 

