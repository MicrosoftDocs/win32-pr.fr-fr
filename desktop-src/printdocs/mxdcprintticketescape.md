---
description: La \_ structure MXDC PrintTicket \_ Escape \_ t est une \_ structure d' \_ en-tête d’échappement MXDC \_ concaténée avec une \_ structure de données MXDC PrintTicket \_ \_ .
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: Structure MXDC_PRINTTICKET_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535600"
---
# <a name="mxdc_printticket_escape_t-structure"></a>\_Structure MXDC PRINTTICKET \_ Escape \_ T

La structure **MXDC \_ PrintTicket \_ Escape \_ t** est une structure d' [**\_ \_ en-tête d’échappement MXDC \_**](mxdcescapeheader.md) concaténée avec une structure de [**\_ \_ données \_ MXDC PrintTicket**](mxdcprintticketpassthrough.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a>Membres

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Une [**structure \_ \_ \_ T d’en-tête d’échappement MXDC**](mxdcescapeheader.md) avec son membre **OPCODE** défini sur la \_ page fixe MXDCOP PrintTicket \_ \_ , MXDCOP \_ PRINTTICKET \_ fixed \_ doc ou MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq.

</dd> <dt>

**printTicketData**
</dt> <dd>

Structure [**de \_ \_ données MXDC \_ PRINTTICKET**](mxdcprintticketpassthrough.md) contenant le ticket d’impression.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est passée dans le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) lorsque cette fonction est appelée avec l’échappement d' [**\_ échappement MXDC**](mxdc-escape.md) et le membre **opcode** de la structure T de l' [**\_ \_ en-tête \_ d’échappement MXDC**](mxdcescapeheader.md) est **MXDCOP \_ \_ \_ page fixe PrintTicket**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** ou **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**. Le résultat est d’écrire le ticket d’impression dans le fichier de document XPS.

Allouez de la mémoire pour l’échappement comme indiqué ci-dessous, définissez les champs en fonction des besoins, puis appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



Si l' **opcode** est défini sur **la \_ \_ \_ page fixe MXDCOP PRINTTICKET**, l’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). Si le **opcode** défini sur **MXDCOP \_ PrintTicket \_ fixed \_ doc** ou **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, l’appel à **ExtEscape** doit se produire entre un appel à [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) et un appel à [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                              |
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

 

