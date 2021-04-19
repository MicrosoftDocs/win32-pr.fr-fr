---
description: Les \_ constantes d’indicateur de bit LINETRANSLATERESULT décrivent différents résultats d’une traduction d’adresse.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: Constantes LINETRANSLATERESULT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad10c3da2b4250ded5706e4aaa10b9b61f8739b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530036"
---
# <a name="linetranslateresult_-constants"></a>\_Constantes LINETRANSLATERESULT

Les constantes d’indicateur de bit **LINETRANSLATERESULT \_** décrivent différents résultats d’une traduction d’adresse.

<dl> <dt>

<span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT \_ canonique**
</dt> <dd> <dl> <dt>



Indique que la chaîne d’entrée était au format canonique valide.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**
</dt> <dd> <dl> <dt>



Indique que l’adresse retournée contient un « $ ».


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



Indique que l’adresse retournée contient un « W ».


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



Indique que l’adresse retournée contient un «  ? ».


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Indique que l’adresse retournée contient un « @ ».


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ international**
</dt> <dd> <dl> <dt>



Indique que l’appel est traité comme un appel international (le code du pays ou de la région spécifié dans l’adresse de destination est différent du code du pays ou de la région spécifié pour le **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INTOLLLIST**
</dt> <dd> <dl> <dt>



Indique que l’appel local est composé en tant que longue distance, car le pays ou la région a un appel payant et le préfixe apparaît dans le **TollPrefixList** du **CurrentLocation**.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ local**
</dt> <dd> <dl> <dt>



Indique que l’appel est traité comme un appel local (le code du pays ou de la région et le code de zone spécifiés dans l’adresse de destination sont les mêmes que ceux spécifiés pour le **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**
</dt> <dd> <dl> <dt>



Indique que l’appel est traité comme un appel longue distance (le code du pays ou de la région spécifié dans l’adresse de destination est le même, mais le code de la zone est différent de ceux spécifiés pour le **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**
</dt> <dd> <dl> <dt>



Indique que le pays ou la région prend en charge l’appel payant, mais que le préfixe n’apparaît pas dans le **TollPrefixList**, l’appel est donc composé en tant qu’appel local. Notez que si les deux inpéages et NOTINTOLLIST sont désactivés, le pays ou la région actuel ne prend pas en charge les préfixes de péage et les éléments d’interface utilisateur liés aux préfixes de péage ne doivent pas être présentés à l’utilisateur. Si un tel bit est activé, le pays ou la région ne prend pas en charge les listes de péages, et les éléments d’interface utilisateur associés doivent être activés.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOtranslation**
</dt> <dd> <dl> <dt>



Indique que la traduction d’adresses n’est pas disponible. Cet élément est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**
</dt> <dd> <dl> <dt>



Indique que l’adresse de numérotation retournée contient un «  : ». Cet élément est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.

> [!Note]  
> Le caractère «  : » (deux-points) est ajouté à la liste des caractères qui peuvent être incorporés dans une chaîne de numérotation et passés dans les adresses de destination. Si vous tentez de la passer d’une application à un périphérique de ligne qui prend en charge une version d’API antérieure à 2,0, vous obtiendrez très probablement LINEERR \_ INVALADDRESS ou éventuellement dans le caractère ignoré. La signification de ce caractère est « suspendre jusqu’à ce qu’une invite vocale soit détectée, puis continuer la numérotation »; Il est destiné à être utilisé lors de la numérotation automatique des systèmes qui fournissent des invites vocales, telles que les processeurs de cartes d’appel longues distances.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




