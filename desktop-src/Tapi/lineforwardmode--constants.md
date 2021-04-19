---
description: Les \_ constantes d’indicateur de bit LINEFORWARDMODE décrivent les conditions dans lesquelles les appels à une adresse peuvent être transférés.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: Constantes LINEFORWARDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521770"
---
# <a name="lineforwardmode_-constants"></a>\_Constantes LINEFORWARDMODE

Les constantes d’indicateur de bit **LINEFORWARDMODE \_** décrivent les conditions dans lesquelles les appels à une adresse peuvent être transférés.

<dl> <dt>

<span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ occupé**
</dt> <dd> <dl> <dt>



Transférer tous les appels sur occupé, quelle que soit leur origine. Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur occupé et sans réponse ne peut pas être contrôlé séparément.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE \_ BUSYEXTERNAL**
</dt> <dd> <dl> <dt>



Transférer tous les appels externes sur occupé. Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur occupé et sur aucune réponse peut être contrôlé séparément.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE \_ BUSYINTERNAL**
</dt> <dd> <dl> <dt>



Transférer tous les appels internes sur occupé. Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur occupé et sur aucune réponse peut être contrôlé séparément.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE \_ BUSYNA**
</dt> <dd> <dl> <dt>



Transférez tous les appels en cas de non-réponse, quelle que soit leur origine. Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur occupé et sans réponse ne peut pas être contrôlé séparément.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE \_ BUSYNAEXTERNAL**
</dt> <dd> <dl> <dt>



Transférez tous les appels externes sur occupé/aucune réponse. Utilisez cette valeur lorsque le transfert d’appels sur occupé et sur aucune réponse ne peut pas être contrôlé séparément pour les appels internes.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE \_ BUSYNAINTERNAL**
</dt> <dd> <dl> <dt>



Transférez tous les appels internes sur les appels occupés/sans réponse. Utilisez cette valeur lorsque le transfert d’appels sur occupé et sur aucune réponse ne peut pas être contrôlé séparément pour les appels internes.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE \_ BUSYNASPECIFIC**
</dt> <dd> <dl> <dt>



Transférer sur occupé/non répondez à tous les appels provenant d’une adresse spécifiée (transfert sélectif de l’appel).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE \_ BUSYSPECIFIC**
</dt> <dd> <dl> <dt>



Transférer sur les appels occupés qui proviennent d’une adresse spécifiée (transfert d’appel sélectif).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE \_ NOANSW**
</dt> <dd> <dl> <dt>



Transférer tous les appels sans réponse, quelle que soit leur origine. Utilisez cette valeur lorsque le transfert d’appels pour les appels internes et externes sur aucune réponse ne peut pas être contrôlé séparément.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE \_ NOANSWEXTERNAL**
</dt> <dd> <dl> <dt>



Transférez tous les appels externes sans réponse. Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur aucune réponse peut être contrôlé séparément.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE \_ NOANSWINTERNAL**
</dt> <dd> <dl> <dt>



Transférez tous les appels internes sans réponse. Utilisez cette valeur lorsque le transfert pour des appels internes et externes sur aucune réponse peut être contrôlé séparément.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE \_ NOANSWSPECIFIC**
</dt> <dd> <dl> <dt>



Transférer en l’absence de réponse tous les appels provenant d’une adresse spécifiée (transfert sélectif de l’appel).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE \_ INdispo**
</dt> <dd> <dl> <dt>



Les appels sont transférés, mais les conditions dans lesquelles le transfert se produit ne sont pas connues, et ne sont jamais connues du fournisseur de services. (TAPI versions 1,4 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE \_**
</dt> <dd> <dl> <dt>



Transférez tous les appels de manière inconditionnelle, quelle que soit leur origine. Utilisez cette valeur lorsque le transfert non conditionnel pour des appels internes et externes ne peut pas être contrôlé séparément. Le transfert non conditionnel remplace le transfert sur des conditions de réponse occupées et/ou aucune.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE \_ UNCONDEXTERNAL**
</dt> <dd> <dl> <dt>



Transférer tous les appels externes sans condition. Utilisez cette valeur lorsque le transfert non conditionnel pour des appels internes et externes peut être contrôlé séparément.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE \_ UNCONDINTERNAL**
</dt> <dd> <dl> <dt>



Transférer tous les appels internes de manière inconditionnelle. Utilisez cette valeur lorsque le transfert non conditionnel pour des appels internes et externes peut être contrôlé séparément.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE \_ UNCONDSPECIFIC**
</dt> <dd> <dl> <dt>



Transférer de manière inconditionnelle tous les appels provenant d’une adresse spécifiée (transfert sélectif de l’appel).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ inconnu**
</dt> <dd> <dl> <dt>



Les appels sont transférés, mais les conditions dans lesquelles le transfert se produit ne sont pas connues pour l’instant. Il est possible que les conditions soient connues à un moment ultérieur. (TAPI versions 1,4 et ultérieures)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Les indicateurs binaires définis par LINEFORWARDMODE ne \_ sont pas orthogonals. Le transfert non conditionnel ignore toute condition spécifique, telle que occupé ou aucune réponse. Si le transfert non conditionnel n’est pas activé, le transfert sur occupé et sur aucune réponse peut être contrôlé séparément ou non séparément. S’ils sont contrôlés séparément, les \_ indicateurs LINEFORWARDMODE Busy et LINEFORWARDMODE \_ NOANSW peuvent être utilisés séparément. S’il n’est pas contrôlé séparément, l’indicateur LINEFORWARDMODE \_ BUSYNA doit être utilisé. De même, si le transfert d’appels internes et externes peut être contrôlé séparément, \_ les indicateurs externes LINEFORWARDMODE internes et LINEFORWARDMODE \_ peuvent être utilisés séparément ; sinon, la combinaison est utilisée.

Les fonctionnalités d’adresse indiquent les modes de transfert disponibles pour chaque adresse affectée à une ligne. Une application peut utiliser [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) pour définir des conditions de transfert au niveau du commutateur.

Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser ces \_ valeurs LINEFORWARDMODE si la version négociée ne les prend pas en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




