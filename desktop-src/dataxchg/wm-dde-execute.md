---
title: Message WM_DDE_EXECUTE (DDE. h)
description: une application cliente échange dynamique de données (dde) publie un \_ \_ message WM execute dde dans une application de serveur dde pour envoyer une chaîne au serveur à traiter en tant que série de commandes.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- WM_DDE_EXECUTE des données de message Exchange
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095398"
---
# <a name="wm_dde_execute-message"></a>\_Message d’exécution DDE de WM \_

une application cliente échange dynamique de données (dde) publie un message **WM \_ \_ execute dde** dans une application de serveur dde pour envoyer une chaîne au serveur à traiter en tant que série de commandes. L’application serveur doit poster un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE en réponse.

Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre client qui publie le message.

</dd> <dt>

*lParam* 
</dt> <dd>

Contient un objet mémoire global qui fait référence à une chaîne de commande ANSI ou Unicode, en fonction des types de fenêtres impliquées dans la conversation.

</dd> </dl>

## <a name="remarks"></a>Notes

La chaîne de commande est une chaîne se terminant par un caractère null qui se compose d’une ou de plusieurs chaînes opcode placées entre crochets ( \[ \] ). Chaque chaîne opcode a la syntaxe suivante, où la liste de *paramètres* est facultative :

*paramètres opcode*

L' *opcode* est tout jeton unique défini par l’application. Il ne peut pas contenir des espaces, des virgules, des parenthèses, des crochets ou des guillemets.

La liste de *paramètres* peut contenir n’importe quelle valeur ou valeur définie par l’application. Plusieurs paramètres sont séparés par des virgules, et l’ensemble de la liste de paramètres est placé entre parenthèses. Les paramètres ne peuvent pas inclure de virgules ou de parenthèses à l’intérieur d’une chaîne entre guillemets. Si un crochet ou un caractère de parenthèse doit apparaître dans une chaîne entre guillemets, il n’est pas nécessaire qu’il soit doublé, comme c’était le cas dans les anciennes règles.

Les chaînes de commande valides sont les suivantes :


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



Notez que, dans les anciennes règles, les parenthèses et les crochets devaient être doublés, comme suit :


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



Les serveurs doivent être en mesure d’analyser les commandes sous l’une ou l’autre forme.

Les chaînes d’exécution Unicode ne doivent être utilisées que lorsque les handles de fenêtre du client et du serveur forcent la fonction [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) à retourner la **valeur true**.

### <a name="posting"></a>Publication

L’application cliente alloue l’objet de mémoire globale en appelant la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .

Lors du traitement du message d’accusé de réception [**\_ \_ DDE DDE**](wm-dde-ack.md) que le serveur publie en réponse à un message **WM d' \_ \_ exécution DDE** , l’application cliente doit supprimer l’objet retourné par le message d' **\_ \_ accusé** de réception DDE.

### <a name="receiving"></a>Réception

L’application serveur publie le message d’accusé de réception [**\_ DDE DDE \_**](wm-dde-ack.md) pour répondre positivement ou négativement. Le serveur doit réutiliser l’objet mémoire globale.

Sauf indication contraire d’un sous-protocole, le serveur ne doit pas envoyer le message d’accusé de réception DDE de l’échange de messages ( [**\_ \_ ACK**](wm-dde-ack.md) ) pour que toutes les actions spécifiées par la chaîne de commande d’exécution soient terminées. La seule exception à cette règle est lorsque la chaîne oblige le serveur à mettre fin à la conversation.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>Dde. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[À propos de échange dynamique de données](about-dynamic-data-exchange.md)
</dt> </dl>

 

