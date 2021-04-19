---
description: Le \_ message NEWCALL de la ligne TSPI est envoyé à la fonction de rappel LINEEVENT chaque fois qu’un nouvel appel que TAPI n’est pas arrivé sur une ligne ouverte par TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: Message LINE_NEWCALL (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535984"
---
# <a name="line_newcall-message"></a>\_Message NEWCALL de ligne

Le message **\_ NEWCALL** de la ligne TSPI est envoyé à la fonction de rappel [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) chaque fois qu’un nouvel appel que TAPI n’est pas arrivé sur une ligne ouverte par TAPI. Il doit s’agir du premier message envoyé concernant cet appel. L’interface TAPI écrit le descripteur opaque *htCall* à l’emplacement passé par le fournisseur de services en tant que *dwParam2*. Cela donne au fournisseur de services la valeur *htCall* à utiliser dans les messages suivants.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*htLine* 
</dt> <dd>

Handle de l’objet opaque TAPI sur le périphérique de ligne.

</dd> <dt>

*htCall* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwMsg* 
</dt> <dd>

La ligne de valeur \_ NEWCALL.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Handle opaque du fournisseur de services pour l’appel, de type [**HDRVCALL**](hdrvline.md). L’interface TAPI transmet cette valeur en tant que paramètre *hdCall* pour identifier l’appel dans les procédures suivantes qu’il appelle pour fonctionner sur l’appel.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Pointeur de type LPHTAPICALL pointant vers un [**HTAPICALL**](htapicall.md). L’interface TAPI écrit le descripteur TAPI opaque pour l’appel à l’emplacement indiqué. Le fournisseur de services doit enregistrer cette valeur et la passer en tant que paramètre *htCall* pour identifier l’appel dans les événements suivants qu’il signale pour l’appel.

Ce paramètre peut également obtenir une valeur **null** (consultez la section Notes suivante).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="remarks"></a>Notes

Le fournisseur de services doit envoyer le message [**\_ CALLSTATE de ligne**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) comme message suivant pour cet appel. L’événement de **ligne \_ NEWCALL** est inhabituel dans le fait qu’il renvoie également une valeur au fournisseur de services.

Cette fonction signale tous les nouveaux appels provenant du fournisseur de services (entrants, sortants, initiés au téléphone, etc.) pour lesquels l’interface TAPI et le fournisseur de services n’ont pas encore échangé les descripteurs opaques. Les handles sont échangés afin que l’interface TAPI et le fournisseur de services puissent ensuite effectuer des demandes et signaler des événements impliquant l’appel. Étant donné que ces nouveaux appels ne sont pas nécessairement entrants, les appels peuvent être initialement dans n’importe quel État, pas nécessairement dans l’état d' *offre* . Si le fournisseur de services démarre et découvre qu’un ou plusieurs appels sont déjà actifs sur la ligne, il en informe l’interface TAPI avec des messages **\_ NEWCALL de ligne** suivis de messages de [**\_ CALLSTATE de ligne**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) indiquant l’état actuel. Un nouvel appel sortant, lancé sur le téléphone par l’utilisateur, est signalé avec un message de **ligne \_ NEWCALL** , et le message **\_ CALLSTATE** de la ligne initiale indique que l’appel était en état de **tonalité** (puis continue à partir de là).

Si le fournisseur de services passe un grand nombre d’appels à l’interface TAPI dans un laps de temps très bref (au cours du même cycle d’interruption), l’interface TAPI peut être retardée dans le traitement de ces appels. Dans ce cas, l’interface TAPI signale au fournisseur de services qu’il doit attendre un peu de temps avant d’envoyer d’autres appels. Il signale cela en écrivant la valeur **null** au lieu d’un [**HTAPICALL**](htapicall.md)valide, à l’emplacement désigné par le paramètre *dwParam2* de la **ligne \_ NEWCALL**. Cela indique que la tentative de traitement du handle d’appel nouvellement offert a échoué, probablement en raison d’une impossibilité temporaire d’allouer de la mémoire. Le fournisseur de services peut répondre en supprimant l’appel ou en renvoyant le message de **ligne \_ NEWCALL** après un délai de planification (pendant lequel le fournisseur de services doit générer le processeur pour permettre à l’interface TAPI de traiter d’autres actions en attente). Dans tous les cas, aucun autre message concernant le nouvel appel ne peut être passé à l’interface TAPI tant que le handle Exchange n’a pas réussi. Lorsque l’emplacement désigné par *dwParam2* acquiert une valeur non **null** , le fournisseur de services sait que cette valeur est un handle [**HTAPICALL**](htapicall.md) valide pour l’appel.

Il n’y a aucun message directement correspondant au niveau de l’interface TAPI. Ce message est utilisé au niveau TSPI pour introduire de manière unique et sans ambiguïté un nouvel appel entrant à TAPI et récupérer l’identificateur opaque TAPI pour l’appel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CALLSTATE de ligne \_**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

