---
description: La \_ \_ structure T de l’en-tête d’échappement MXDC \_ contient le code d’opération d’un appel à ExtEscape avec MXDC \_ Escape comme paramètre nEscape. Il fournit également la taille des mémoires tampons d’entrée et de sortie.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: Structure MXDC_ESCAPE_HEADER_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 53dd83e362ab21938121a986ee2402076d72f870460bc9db608b9a048cee0f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099073"
---
# <a name="mxdc_escape_header_t-structure"></a>MXDC \_ \_ structure T de l’en-tête d’échappement \_

La structure T de l' **\_ \_ \_ en-tête d’échappement MXDC** contient le code d’opération d’un appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec [**MXDC \_ Escape**](mxdc-escape.md) comme paramètre *nEscape* . Il fournit également la taille des mémoires tampons d’entrée et de sortie.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbInput**
</dt> <dd>

Taille de la mémoire tampon d’entrée qui sera passée au paramètre *lpszOutData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**cbOutput**
</dt> <dd>

Taille de la mémoire tampon de sortie. Il s’agit de la même valeur que le paramètre *cbOutput* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**opCode**
</dt> <dd>

Constante de code qui indique à MXDC ce qu’il faut faire.



| Code des opérations                      | Description                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MXDCOP \_ obtient le \_ nom du fichier                | Retourne, dans le paramètre *lpszOutData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , le chemin d’accès complet du fichier de sortie comme une chaîne se terminant par zéro ou la taille de cette chaîne. Consultez la section Notes.                   |
| \_ \_ \_ Seq document fixe MXDCOP \_ PRINTTICKET | Associe un ticket d’impression à une séquence de documents fixe XPS.                                                                                                                                                         |
| \_ \_ document fixe MXDCOP \_ PRINTTICKET      | Associe un ticket d’impression à un document XPS.                                                                                                                                                                        |
| \_ \_ page fixe MXDCOP \_ PRINTTICKET     | Associe un ticket d’impression à une page XPS.                                                                                                                                                                            |
| MXDCOP \_ Set \_ S0PAGE                  | Envoie le balisage XPS de la page actuelle à la sortie.                                                                                                                                                                |
| MXDCOP \_ définir \_ la \_ ressource S0PAGE        | Envoie une ressource sur la page, telle qu’une image ou une police, à la sortie.                                                                                                                                                 |
| MXDCOP \_ définir \_ le \_ mode XPSPASSTHRU       | Place le MXDC dans un État direct, ce qui permet à une application d’écrire XPS directement dans le fichier de sortie sans aucun traitement de la MXDC. Un document entier ou même une séquence de documents peut être écrit de cette façon. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Avant d’appeler [**MXDC \_ Escape**](mxdc-escape.md), \_ les applications doivent d’abord vérifier que le pilote est MXDC en appelant [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec l’échappement [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) . Si le pilote est le MXDC, la fonction retourne la chaîne se terminant par zéro « http://schemas.microsoft.com/xps/2005/06 ».

Cette structure est toujours au début des données passées à la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) dans son paramètre *lpszInData* .

Lorsque l' **opcode** est MXDCOP, \_ récupérez le nom de \_ fichier :

-   Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose uniquement de la structure T de l' **\_ \_ en-tête \_ d’échappement MXDC** .
-   Obtenez le nom du fichier de sortie en appelant [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deux fois.
    1.  La première fois, Pass 4 au paramètre *cbOutput* de [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Définissez le paramètre *lpszOutData* pour qu’il pointe vers tous les 4 octets alloués de la mémoire. La taille du chemin d’accès complet du fichier est retournée dans le paramètre *lpszOutData* de **ExtEscape**.
    2.  Ensuite, appelez à nouveau la fonction. Cette fois, définissez *cbOutput* et *cbInput* sur 4 + *DataSize*. Le chemin d’accès complet au fichier est retourné dans une structure [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) .

Lorsque l' **opcode** est MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq ou MXDCOP \_ PrintTicket \_ fixed \_ doc :

-   Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose de la structure **\_ \_ \_ T d’en-tête d’échappement MXDC** et d’une structure [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concaténée dans une structure [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .
-   L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) et un appel à [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

Lorsque l' **opcode** est \_ la \_ page fixe MXDCOP PRINTTICKET \_ :

-   Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose de la structure **\_ \_ \_ T d’en-tête d’échappement MXDC** et d’une structure [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concaténée dans une structure [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .
-   L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

Lorsque l' **opcode** est MXDCOP, \_ définissez \_ S0PAGE :

-   Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose de la structure **\_ \_ \_ T d’en-tête d’échappement MXDC** et d’une structure [**MxdcS0PageData**](mxdcs0pagedata.md) concaténée dans une structure [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .
-   L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).
-   L’application appelante est chargée de valider le XML.
-   La consommation de streaming est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec MXDCOP \_ définir \_ \_ la ressource S0PAGE comme **opcode** pour chaque ressource sur la page avant de l’appeler avec MXDCOP \_ définir \_ S0PAGE.

Lorsque l' **opcode** est MXDCOP, \_ définissez la \_ \_ ressource S0PAGE :

-   Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose de la structure **\_ \_ \_ T d’en-tête d’échappement MXDC** et d’une structure [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concaténée dans une structure [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .
-   L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), mais il peut y avoir plusieurs appels de ce type entre les appels **StartPage** et **EndPage** .
-   La consommation de streaming est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec MXDCOP \_ définir \_ \_ la ressource S0PAGE comme **opcode** pour chaque ressource sur la page avant de l’appeler avec MXDCOP \_ définir \_ S0PAGE.

Lorsque l' **opcode** est MXDCOP, \_ Définissez le \_ \_ mode XPSPASSTHRU :

-   Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose uniquement de la structure T de l' **\_ \_ en-tête \_ d’échappement MXDC** .
-   Cet appel doit se produire avant l’appel à [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).

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

 

