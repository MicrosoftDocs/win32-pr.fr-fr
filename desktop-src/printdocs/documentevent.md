---
description: La fonction DocumentEvent est un gestionnaire d’événements pour les événements associés à l’impression d’un document.
ms.assetid: 1250116e-55c7-470f-97f6-36f27a31a841
title: DocumentEvent, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentEvent
- DocumentEventA
- DocumentEventW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aa80e5fe17047eceacdc30e2a40a4a629088d89f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529008"
---
# <a name="documentevent-function"></a>DocumentEvent fonction)

La fonction **DocumentEvent** est un gestionnaire d’événements pour les événements associés à l’impression d’un document.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DocumentEvent(
  _In_  HANDLE hPrinter,
  _In_  HDC    hdc,
        INT    iEsc,
        ULONG  cbIn,
  _In_  PVOID  pvIn,
        ULONG  cbOut,
  _Out_ PVOID  pvOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle d’un objet Printer. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*HDC* \[ dans\]
</dt> <dd>

Handle de contexte de périphérique qui est généré par un appel de [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca). Il s’agit de zéro si *iEsc* est défini sur DOCUMENTEVENT \_ CREATEDCPRE. Pour des restrictions sur l’impression à partir d’une application 32 bits sur une version 64 bits de Windows, consultez la section Notes.

</dd> <dt>

*iEsc* 
</dt> <dd>

Code d’échappement qui identifie l’événement à gérer. Ce paramètre peut être l’une des constantes entières suivantes.



| Constante                                                                                                                                                                                                                                                                                                                                               | Événement                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | GDI va traiter un appel à sa fonction [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | GDI a simplement traité un appel à son [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ou à sa fonction [**créée**](/windows/desktop/api/wingdi/nf-wingdi-createica) .<br/> Ce code d’échappement ne doit pas être utilisé, sauf si un appel précédent à **DocumentEvent** avec *iEsc* a été défini sur DocumentEvent \_ CREATEDCPRE.<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | GDI est sur le paragraphe de traiter un appel à son [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ou à sa fonction [**créée**](/windows/desktop/api/wingdi/nf-wingdi-createica) .<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | GDI va traiter un appel à sa fonction [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | GDI a simplement traité un appel à sa fonction [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE ou DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | GDI va traiter un appel à sa fonction [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | GDI va traiter un appel à sa fonction [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) .<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ échappement**</dt> </dl>                                                                                                                                                                     | GDI va traiter un appel à sa fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | L' \_ événement DOCUMENTEVENT QUERYFILTER représente une opportunité pour le spouleur d’interroger le pilote pour obtenir la liste des événements DOCUMENTEVENT \_ *xxx* auxquels le pilote répond. Cet événement est émis juste avant un appel à **DocumentEvent** qui transmet l' \_ événement CREATEDCPRE DocumentEvent.<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | GDI a simplement traité un appel à sa fonction [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) .<br/> Ce code d’échappement ne doit pas être utilisé, sauf si un appel précédent à **DocumentEvent** avec *iEsc* a été défini sur DocumentEvent \_ RESETDCPRE.<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | GDI va traiter un appel à sa fonction [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) .<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | GDI a simplement traité un appel à sa fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE ou DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | GDI va traiter un appel à sa fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ StartPage**</dt> </dl>                                                                                                                                                            | GDI va traiter un appel à sa fonction [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) .<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*MacBinary* 
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pvIn*.

</dd> <dt>

*pvIn* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon. Le contenu de la mémoire tampon dépend de la valeur de *iEsc*, comme indiqué dans le tableau suivant.



| Constante                                                                                                                                                                                                                                                                                                                                               | Contenu PVin                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | Non utilisé.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* contient l’adresse d’un pointeur vers la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) spécifiée dans le paramètre *pvOut* lors d’un appel précédent à cette fonction, pour laquelle le paramètre *iEsc* a été défini sur DOCUMENTEVENT \_ CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | *pvIn* pointe vers une \_ structure DOCEVENT CREATEDCPRE qui est documentée dans le [Kit de développement de pilotes Windows](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | Non utilisé.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | Non utilisé.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE ou DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | Non utilisé.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | Non utilisé.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ échappement**</dt> </dl>                                                                                                                                                                     | *pvIn* pointe vers une \_ structure de séquence d’échappement DOCEVENT qui est documentée dans le kit de développement de [pilotes Windows](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | Identique à DOCUMENTEVENT \_ CREATEDCPRE.<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | *pvIn* contient l’adresse d’un pointeur vers la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) spécifiée dans le paramètre *pvOut* lors d’un appel précédent à cette fonction, pour laquelle le paramètre *iEsc* a été défini sur DOCUMENTEVENT \_ RESETDCPRE.<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | *pvIn* contient l’adresse d’un pointeur vers la structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fournie par l’appelant de [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* pointe vers une valeur long qui spécifie l’identificateur de travail d’impression retourné par [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE ou DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | *pvIn* contient l’adresse d’un pointeur vers une structure [**docinfo**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa) fournie par l’appelant de [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ StartPage**</dt> </dl>                                                                                                                                                            | Non utilisé.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbOut*</dt> <dd> 

| Valeur                       | Signification                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| IDOCUMENTEVENT \_ QUERYFILTER | Taille, en octets, du pointeur de la mémoire tampon vers par *pvOut*.                             |
| DOCUMENTEVENT \_ échappement       | Valeur utilisée comme paramètre *cbOutput* pour [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). |
| Pour toutes les autres valeurs        | *iEsc* n’est pas utilisé.                                                                  |



 

</dd> <dt>

*pvOut* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon. Le contenu de la mémoire tampon dépend de la valeur fournie pour *iEsc*, comme indiqué dans le tableau suivant.



| Constante                                                                                                                                                                                          | Contenu pvOut                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl> | Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fournie par le pilote, que GDI utilise à la place de celui fourni par l’appelant [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) . (Si la **valeur est null**, GDI utilise la structure fournie par l’appelant.)<br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ échappement**</dt> </dl>                | Pointeur vers une mémoire tampon utilisée comme paramètre *lpszOutData* pour [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl> | Pointeur vers une mémoire tampon contenant une \_ structure de filtre DOCEVENT qui est documentée dans le [Kit de développement de pilotes Windows](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>    | Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fournie par le pilote, que GDI utilise à la place de celui fourni par l’appelant [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) . (Si la **valeur est null**, GDI utilise la structure fournie par l’appelant.)<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de la fonction dépend de l’échappement fourni pour *iEsc*. Pour certains codes d’échappement, la valeur de retour n’est pas utilisée (voir ci-dessous). Si la fonction fournit une valeur de retour, elle doit être l’une des valeurs suivantes.



| Valeur renvoyée               | Signification                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| échec de DOCUMENTEVENT \_     | Le pilote prend en charge le code d’échappement identifié par *iEsc*, mais une erreur s’est produite. |
| réussite de DOCUMENTEVENT \_     | Le pilote a réussi à gérer le code d’échappement identifié par *iEsc*.             |
| DOCUMENTEVENT \_ non pris en charge | Le pilote ne prend pas en charge le code d’échappement identifié par *iEsc*.                 |



 

La liste suivante indique les codes d’échappement qui nécessitent une valeur de retour et ce qui n’est pas le cas, et explique la signification de la \_ réussite DOCUMENTEVENT, de DOCUMENTEVENT \_ Failure et des \_ codes de retour DOCUMENTEVENT non pris en charge.



| Valeur renvoyée                                          | Signification                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ ABORTDOC                               | La valeur de retour n’est pas utilisée et ne doit pas être lue.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPOST                           | La valeur de retour n’est pas utilisée et ne doit pas être lue.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPRE                            | \_Échec de DOCUMENTEVENT-GDI ne crée pas le contexte de périphérique ou le contexte d’information, et fournit une valeur de retour de 0 pour [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ou [**créer**](/windows/desktop/api/wingdi/nf-wingdi-createica). |
| DOCUMENTEVENT \_ DELETEDC                               | La valeur de retour n’est pas utilisée et ne doit pas être lue.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPOST                             | La valeur de retour n’est pas utilisée et ne doit pas être lue.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPRE ou DOCUMENTEVENT \_ ENDDOC     | La valeur de retour n’est pas utilisée et ne doit pas être lue.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDPAGE                                | La valeur de retour n’est pas utilisée et ne doit pas être lue.                                                                                                                                       |
| DOCUMENTEVENT \_ échappement                                 | La valeur de retour n’est pas utilisée et ne doit pas être lue.                                                                                                                                       |
| DOCUMENTEVENT \_ QUERYFILTER                            | Consultez la section Notes.                                                                                                                                                                               |
| DOCUMENTEVENT \_ RESETDCPOST                            | La valeur de retour n’est pas utilisée et ne doit pas être lue.                                                                                                                                       |
| DOCUMENTEVENT \_ RESETDCPRE                             | Échec de DOCUMENTEVENT \_ -GDI ne réinitialise pas le contexte de périphérique et fournit une valeur de retour de 0 pour [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca).                                                           |
| DOCUMENTEVENT \_ STARTDOCPOST                           | \_Échec de DOCUMENTEVENT-GDI appelle [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) pour arrêter le document, puis fournit une valeur de retour d' \_ erreur SP pour [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                      |
| DOCUMENTEVENT \_ STARTDOCPRE ou DOCUMENTEVENT \_ STARTDOC | \_Échec de DOCUMENTEVENT-GDI ne démarre pas le document et fournit une valeur de retour de l' \_ erreur SP pour [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                                                       |
| DOCUMENTEVENT \_ StartPage                              | \_Échec de DOCUMENTEVENT-GDI ne démarre pas la page et fournit une valeur de retour de SP \_ Error pour [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage).                                                         |



 

## <a name="remarks"></a>Notes

Pour une valeur *iEsc* de DOCUMENTEVENT \_ QUERYFILTER, le spouleur peut interpréter une \_ valeur de réussite DOCUMENTEVENT retournée par **DOCUMENTEVENT** de deux façons, selon que le pilote a modifié certains membres de la structure de \_ filtre DOCEVENT (qui est documenté dans le kit de développement de [pilotes Windows](https://msdn.microsoft.com/windows/hardware/gg487428) ). (Le paramètre *pvOut* pointe vers cette structure.) Lorsque le spouleur alloue de la mémoire pour une structure de ce type, il initialise deux membres de cette structure, **cElementsReturned** et **cElementsNeeded**, aux valeurs connues. Une fois **DocumentEvent** retourné, le spouleur détermine si les valeurs de ces membres ont changé et utilise ces informations pour interpréter la valeur de retour **DocumentEvent** . Le tableau suivant résume cette situation.



| Valeur renvoyée                          | État de cElementsReturned et cElementsNeeded    | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| réussite de DOCUMENTEVENT \_<br/>     | Le pilote n’a apporté aucune modification à l’un ou l’autre des membres.<br/> | Le spouleur interprète cette valeur de retour comme équivalant à DOCUMENTEVENT \_ non pris en charge. Le spouleur ne parvient pas à récupérer le filtre d’événements à partir du pilote. il persiste donc dans l’appel de **DocumentEvent** pour tous les événements.<br/>                                                                                                                                                                                                                         |
| réussite de DOCUMENTEVENT \_<br/>     | Le pilote a été écrit sur un ou les deux membres.<br/>    | Le spouleur accepte cette valeur de retour sans interprétation. Si le pilote a écrit dans un seul **cElementsNeeded** et **cElementsReturned**, le spouleur considère que le membre inchangé a une valeur de zéro.<br/> Le spouleur filtre tous les événements répertoriés dans le membre **aDocEventCall** du \_ filtre DOCEVENT (qui est documenté dans le [Kit de développement de pilotes Windows](https://msdn.microsoft.com/windows/hardware/gg487428) ).<br/> |
| DOCUMENTEVENT \_ non pris en charge<br/> | Non applicable<br/>                          | Le pilote ne prend pas en charge DOCUMENTEVENT \_ QUERYFILTER.<br/> Le spouleur ne parvient pas à récupérer le filtre d’événements à partir du pilote. il persiste donc dans l’appel de **DocumentEvent** pour tous les événements.<br/>                                                                                                                                                                                                                                            |
| échec de DOCUMENTEVENT \_<br/>     | Non applicable<br/>                          | Le pilote prend en charge DOCUMENTEVENT \_ QUERYFILTER, mais a rencontré une erreur interne.<br/> Le spouleur ne parvient pas à récupérer le filtre d’événements à partir du pilote. il persiste donc dans l’appel de **DocumentEvent** pour tous les événements.<br/>                                                                                                                                                                                                                 |



 

Si le code d’échappement fourni dans le paramètre *iEsc* est DOCUMENTEVENT \_ CREATEDCPRE, les règles suivantes s’appliquent :

-   Si le travail est envoyé directement à l’imprimante sans mise en file d’attente, pvIn->pszDevice pointe sur le nom de l’imprimante. (Pour plus d’informations, consultez la documentation relative à DOCEVENT \_ Structure CREATEDCPRE dans le [Kit de développement de pilotes Windows](https://msdn.microsoft.com/windows/hardware/gg487428).)
-   Si le travail est mis en file d’attente, pvIn->pszDevice pointe sur le nom du port d’imprimante.

> [!Note]  
> Les restrictions suivantes s’appliquent lors de l’exécution d’une application 32 bits sur une version 64 bits de Windows. La seule fonction GDI que **DocumentEvent** doit appeler est [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape), et seules les séquences d’échappement privées doivent être utilisées. Les appels **DocumentEvent** à d’autres fonctions GDI peuvent produire un comportement indéfini.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DocumentEventW** (Unicode) et **DocumentEventA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[Kit de développement de pilotes Windows](https://msdn.microsoft.com/windows/hardware/gg487428)
</dt> </dl>

 

