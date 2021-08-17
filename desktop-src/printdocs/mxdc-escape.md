---
description: La fonction d’échappement de l' \_ imprimante MXDC Escape permet aux applications d’écrire des documents dans un fichier ou sur une imprimante au format XPS (XML Paper Specification) au moyen de Microsoft XPS Document Converter (MXDC).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: MXDC_ESCAPE fonction (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7ace79404808db750a15b2c17b6fedb336dbd1d72b1581888324a4d87bb7cd67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460879"
---
# <a name="mxdc_escape-function"></a>MXDC \_ fonction d’échappement)

La fonction d’échappement de l’imprimante **MXDC \_ Escape** permet aux applications d’écrire des documents dans un fichier ou sur une imprimante au format XPS (XML Paper Specification) au moyen de Microsoft XPS Document Converter (MXDC).

Pour effectuer cette opération, appelez la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec les paramètres suivants.

## <a name="syntax"></a>Syntaxe


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* 
</dt> <dd>

Handle vers le contexte de périphérique d’impression.

</dd> <dt>

*cbInput* 
</dt> <dd>

Taille, en octets, des données vers lesquelles pointe le paramètre *lpszInData* .

</dd> <dt>

*lpszInData* 
</dt> <dd>

Pointeur vers une mémoire tampon contenant les données d’entrée, qui sont toujours stockées dans l’une des structures suivantes.

<dl> <dd><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></dd> <dd><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></dd> <dd><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></dd> <dd><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></dd> </dl>

Chacune de ces structures a un membre opcode qui spécifie ce que le MXDC est supposé faire. Pour obtenir des remarques détaillées sur ces codes, consultez MxdcEscapeHeader.



| Code d’opération (OpCode)                                                                                                                                                                                                  | Action                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <dt>**MXDCOP \_ obtient le \_ nom du fichier**</dt> </dl>                                          | Définit le paramètre *lpszOutData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) sur, soit le chemin d’accès complet du fichier de sortie comme une chaîne se terminant par zéro, soit la taille de cette chaîne.<br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <dt>**\_ \_ \_ Seq document fixe MXDCOP \_ PRINTTICKET**</dt> </dl> | Associe un ticket d’impression à une séquence de documents fixe XPS.<br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <dt>**\_ \_ document fixe MXDCOP \_ PRINTTICKET**</dt> </dl>              | Associe un ticket d’impression à un document XPS.<br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <dt>**\_ \_ page fixe MXDCOP \_ PRINTTICKET**</dt> </dl>           | Associe un ticket d’impression à une page XPS.<br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <dt>**MXDCOP \_ Set \_ S0PAGE**</dt> </dl>                                                | Envoie le balisage XPS de la page actuelle à la sortie.<br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <dt>**MXDCOP \_ définir \_ la \_ ressource S0PAGE**</dt> </dl>                    | Envoie une ressource sur la page, telle qu’une image ou une police, à la sortie.<br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <dt>**MXDCOP \_ définir \_ le \_ mode XPSPASSTHRU**</dt> </dl>                 | Place le MXDC dans un État pass-through, permettant à une application d’écrire XPS directement dans le fichier de sortie sans aucun traitement de la MXDC. Un document entier ou même une séquence de documents peut être écrit de cette façon.<br/> |



 

</dd> <dt>

*cbOutput* 
</dt> <dd>

Taille, en octets, des données vers lesquelles pointe le paramètre *lpszOutData* .

</dd> <dt>

*lpszOutData* 
</dt> <dd>

Pointeur vers une mémoire tampon contenant les données de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est supérieure à zéro. Si la fonction échoue ou n’est pas prise en charge, la valeur de retour est inférieure ou égale à zéro.

## <a name="remarks"></a>Remarques

Cette séquence d’échappement est prise en charge par MXDC et XPSDrv, mais pas par GDI.

Pour déterminer si le pilote d’imprimante est le MXDC, appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec l’échappement [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) . Si le pilote est le MXDC, **ExtEscape** retourne la chaîne se terminant par zéro « http://schemas.microsoft.com/xps/2005/06 ». Assurez-vous que la mémoire tampon référencée par le paramètre *lpszOutData* est suffisamment grande pour contenir cette chaîne.

pour déterminer si le pilote d’imprimante est le pilote Microsoft xps document writer intégré Windows, vérifiez que le pilote d’imprimante est le MXDC, puis déterminez si le nom du pilote d’imprimante est « Microsoft XPS Document writer ».

Pour connaître le nom du pilote d’imprimante, utilisez l’une des techniques suivantes. <dl> Appelez [**GetPrinterDriver**](getprinterdriver.md) avec la valeur de paramètre *Level* définie sur 1. Le nom du pilote d’imprimante est retourné dans le membre **pname** de la structure [**\_ informations sur le pilote \_ 1**](driver-info-1.md) .  
ou  
Appelez [**GetPrinter**](getprinter.md) avec la valeur de paramètre *Level* définie sur 2. Le nom du pilote d’imprimante est retourné dans le membre **pDriverName** de la structure [**Printer \_ info \_ 2**](printer-info-2.md) .  
</dl>

Le tableau suivant indique où trouver différents objets dans le fichier XPS. les différents types d’objets sont écrits.



| Object       | Emplacement dans le fichier de sortie    |
|--------------|--------------------------------|
| Page fixe   | /Documents/1/Pages/Esc%d.fpage |
| Thumbnail    | /Documents/1/Metadata          |
| Imprimer le ticket | /Documents/1/Metadata          |
| Police         | /Documents/1/Resources/Fonts   |
| Image        | /Documents/1/Resources/Images  |



 

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

[Fonctions d’échappement d’imprimante](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

