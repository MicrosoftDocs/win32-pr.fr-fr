---
title: Message EM_AUTOURLDETECT (RichEdit. h)
description: Active ou désactive la détection automatique des liens hypertexte par un contrôle RichEdit.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195703"
---
# <a name="em_autourldetect-message"></a>\_Message AUTOURLDETECT em

Active ou désactive la détection automatique des liens hypertexte par un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifiez 0 pour désactiver la détection de liaison automatique, ou l’une des valeurs suivantes pour activer différents types de détection.



| Valeur                                                                                                                                                                                       | Signification                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**AURL \_ DISABLEMIXEDLGC**</dt> </dl>          | **Windows 8**: désactiver la reconnaissance des noms de domaine qui contiennent des étiquettes avec des caractères appartenant à plusieurs des scripts suivants : Latin, grec et cyrillique. <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**AURL \_ ENABLEDRIVELETTERS**</dt> </dl> | **Windows 8**: reconnaître les noms de fichiers qui ont une spécification de lecteur de début, par exemple c : \\ temp.<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**AURL \_ ENABLEEA**</dt> </dl>                               | Cette valeur est déconseillée ; Utilisez **AURL \_ ENABLEEAURLS** à la place.<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**AURL \_ ENABLEEAURLS**</dt> </dl>                   | Reconnaître les URL qui contiennent des caractères d’Extrême-Orient. <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**AURL \_ ENABLEEMAILADDR**</dt> </dl>          | **Windows 8**: reconnaître les adresses de messagerie.<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**AURL \_ ENABLETELNO**</dt> </dl>                      | **Windows 8**: reconnaître les numéros de téléphone.<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**AURL \_ ENABLEURL**</dt> </dl>                            | **Windows 8**: reconnaît les url qui incluent le chemin d’accès.<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre détermine les schémas d’URL reconnus si **AURL \_ ENABLEURL** est actif. Si *lParam* a la valeur null, la liste de noms de schémas par défaut est utilisée (consultez la section Notes). *LParam* peut également pointer vers une chaîne se terminant par un caractère null, composée de noms de schéma se terminant par un point-virgule allant jusqu’à 50 qui remplacent la liste de noms de schéma par défaut. Par exemple, la chaîne peut être « News : http : ftp : Telnet : ». La syntaxe du nom du schéma est définie dans le document [URI (Uniform Resource Identifiers) : syntaxe générique]( https://www.ietf.org/rfc/rfc2396.txt) sur le site Web IETF (Internet Engineering Task Force). Plus précisément, un nom de schéma peut contenir jusqu’à 13 caractères (y compris le signe deux-points), doit commencer par un caractère alphabétique ASCII et peut être suivi d’un mélange de alphabetics ASCII, de chiffres et de trois caractères de ponctuation : « . », « + » et « - ». Le type de chaîne peut être **char \* *_ ou _* WCHAR \***; le contrôle Rich Edit détecte automatiquement le type.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si le message est correctement exécuté, la valeur de retour est zéro.

Si le message échoue, la valeur de retour est une valeur différente de zéro. Par exemple, le message peut échouer en raison d’une mémoire insuffisante, d’une option de détection non valide ou d’une chaîne de nom de schéma non valide.

Si *lParam* contient plus de 50 noms de schéma, le message échoue avec la valeur de retour **E \_ INVALIDARG**.

## <a name="remarks"></a>Notes

si la détection automatique d’URL est activée (autrement dit, *wParam* comprend **AURL \_ ENABLEURL**), le contrôle rich edit analyse tout texte modifié pour déterminer si le texte correspond au format d’une URL (ou plus généralement dans Windows 8 ou ultérieur un identificateur de ressource IRI International). Si *lParam* a la valeur null, le contrôle détecte les URL qui commencent par les noms de schémas suivants :

-   callto
-   fichier
-   ftp
-   gopher
-   http
-   https
-   mailto
-   news
-   HDInsight
-   NNTP
-   onenote
-   programme
-   prospero
-   tel
-   telnet
-   wais
-   webcal

Lorsque la détection automatique des liens est activée, le contrôle RichEdit supprime l’effet de **\_ lien CFE** d’un texte modifié qui n’a pas un format reconnu par le contrôle. Si votre application utilise l’effet de **\_ lien CFE** pour marquer d’autres types de texte, n’activez pas la détection automatique des liens. Le contrôle RichEdit ne vérifie pas si un lien détecté existe ; Cette responsabilité appartient au client.

Un contrôle RichEdit envoie la notification [en \_ lien](en-link.md) lorsqu’il reçoit plusieurs messages lorsque le pointeur de la souris est sur du texte qui a l’effet de **\_ lien CFE** . Pour plus d’informations, consultez [liens hypertexte RichEdit automatique](/archive/blogs/murrays/automatic-richedit-hyperlinks) et [liens hypertexte de nom convivial RichEdit](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[en \_ lien](en-link.md)
</dt> </dl>

 

