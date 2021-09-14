---
description: Le \_ message LINEDEVSTATE de ligne TAPI est envoyé lorsque l’état d’un périphérique de ligne a changé. L’application peut appeler lineGetLineDevStatus pour déterminer le nouvel état de la ligne.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: Message LINE_LINEDEVSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217697"
---
# <a name="line_linedevstate-message"></a>\_Message LINEDEVSTATE de ligne

Le message **\_ LINEDEVSTATE de ligne** TAPI est envoyé lorsque l’état d’un périphérique de ligne a changé. L’application peut appeler [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) pour déterminer le nouvel état de la ligne.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de l’appareil de ligne. Ce paramètre est **null** lorsque *DWPARAM1* est LINEDEVSTATE \_ rein.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne. Si le paramètre *dwParam1* est LINEDEVSTATE \_ Réinit, le paramètre *dwCallbackInstance* n’est pas valide et a la valeur zéro.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Élément d’état de périphérique de ligne qui a changé. Le paramètre peut être une ou plusieurs des [**\_ constantes LINEDEVSTATE**](linedevstate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

L’interprétation de ce paramètre dépend de la valeur de *dwParam1*. Si *dwParam1* est LINEDEVSTATE \_ Ringing, *dwParam2* contient le mode Ring avec lequel le commutateur demande à la ligne de sonner. Les modes Ring valides sont des nombres compris dans la plage **dwNumRingModes**, où **dwNumRingModes** est une fonctionnalité de périphérique en ligne.

Si *dwParam1* est LINEDEVSTATE \_ Réinit et que le message a été émis par l’interface TAPI suite à la traduction d’un nouveau message d’API en message de réinitialisation, *DwParam2* contient le paramètre *dwMsg* du message d’origine (par exemple, [**line \_ Create**](line-create.md) ou Line \_ LINEDEVSTATE). Si *dwParam2* est égal à zéro, cela indique que le message de réinitialisation est un message de réinitialisation « réel » qui oblige l’application à appeler [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) au plus tôt.

</dd> <dt>

*dwParam3* 
</dt> <dd>

L’interprétation de ce paramètre dépend de la valeur de *dwParam1*. Si *dwParam1* est LINEDEVSTATE \_ Ringing, *dwParam3* contient le nombre de sonneries pour cet événement Ring. Le nombre de sonneries démarre à zéro.

Si *dwParam1* est LINEDEVSTATE \_ Réinit et que le message a été émis par l’interface TAPI suite à la traduction d’un nouveau message d’API en message de réinitialisation, *DwParam3* contient le paramètre *dwParam1* du message d’origine (par exemple, LINEDEVSTATE \_ TRANSLATECHANGE ou une autre \_ valeur LINEDEVSTATE, si *dwParam2* est \_ la ligne LINEDEVSTATE ou le nouvel identificateur de périphérique, si *dwParam2* est la [**ligne \_ Create**](line-create.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

L’envoi de la **ligne \_ LINEDEVSTATE** message peut être contrôlé avec [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Une application peut indiquer des modifications d’élément d’État sur lesquelles elle souhaite être notifiée. Par défaut, tous les rapports d’État sont désactivés, à l’exception de LINEDEVSTATE \_ reinit, qui ne peut pas être désactivé. Ce message est envoyé à toutes les applications qui ont un handle vers la ligne, y compris celles qui ont appelé [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) avec le paramètre *DWPRIVILEGES* défini sur LINECALLPRIVILEGE \_ None, LINECALLPRIVILEGE \_ Owner, LINECALLPRIVILEGE \_ Monitor ou des combinaisons autorisées de ces.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**fermeture de ligne \_**](line-close.md)
</dt> <dt>

[**création de ligne \_**](line-create.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




