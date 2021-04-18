---
title: SELFLAG, constantes (oleacc. h)
description: Cette rubrique décrit les valeurs constantes utilisées pour spécifier la façon dont un objet accessible est sélectionné ou qui prend le focus.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540442"
---
# <a name="selflag-constants"></a>Constantes SELFLAG

Cette rubrique décrit les valeurs constantes utilisées pour spécifier la façon dont un objet accessible est sélectionné ou qui prend le focus. Les constantes sont définies dans oleacc. h et sont utilisées avec la méthode [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .

Les combinaisons suivantes ne sont pas autorisées :

-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION
-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION

**Remarque pour les clients :** Microsoft Active Accessibility ne prend pas en charge la sélection du texte contenu dans les contrôles Edit et Rich Edit, car le texte est exposé sous la forme d’une chaîne dans la [propriété Value](value-property.md)de l’objet.

Pour plus d’informations sur la façon d’effectuer des opérations de sélection complexes, consultez [sélection des objets enfants](selecting-child-objects.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valeur</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </dl></td>
<td style="text-align: left;">N’effectue aucune action. Microsoft Active Accessibility ne modifie pas la sélection ou le focus.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </dl></td>
<td style="text-align: left;">Définit le focus sur l’objet et en fait l’ancre de sélection. Utilisé par lui-même, cet indicateur ne modifie pas la sélection. L’effet est similaire au déplacement manuel du focus en appuyant sur une touche de direction tout en maintenant la touche CTRL enfoncée dans l’Explorateur Windows ou dans une zone de liste à sélection multiple. <br/> Avec les objets qui ont le <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS est combiné aux valeurs suivantes :<br/>
<ul>
<li>SELFLAG_TAKESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li>
<li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li>
</ul>
Si vous appelez <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible :: accSelect</strong></a> avec l’indicateur SELFLAG_TAKEFOCUS sur un objet qui a un <strong>HWND</strong>, l’indicateur prend effet uniquement si le parent de l’objet a déjà le focus.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0X2</dt> </dl></td>
<td style="text-align: left;">Sélectionne l’objet et supprime la sélection de tous les autres objets dans le conteneur. <br/> À moins qu’elle ne soit combinée avec SELFLAG_TAKEFOCUS, cet indicateur ne change pas le focus ou l’ancre de sélection. Le SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combinaison équivaut à un simple clic sur un élément dans l’Explorateur Windows.<br/> Cet indicateur ne doit pas être combiné avec les indicateurs suivants :<br/>
<ul>
<li>SELFLAG_ADDSELECTION</li>
<li>SELFLAG_REMOVESELECTION</li>
<li>SELFLAG_EXTENDSELECTION</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </dl></td>
<td style="text-align: left;">Modifie la sélection afin que tous les objets entre l’ancre de sélection et cet objet prennent l’état de sélection de l’objet d’ancrage. Si l'objet d'ancrage n'est pas sélectionné, les objets sont enlevés de la sélection. Si l’objet d’ancrage est sélectionné, la sélection est étendue pour inclure cet objet et tous les objets compris entre. Définissez l’état de sélection en combinant cet indicateur avec SELFLAG_ADDSELECTION ou SELFLAG_REMOVESELECTION. <br/> À moins qu’elle ne soit combinée avec SELFLAG_TAKEFOCUS, cet indicateur ne change pas le focus ou l’ancre de sélection. Le SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinaison revient à ajouter un élément à une sélection manuellement en maintenant la touche Maj enfoncée et en cliquant sur un objet non sélectionné dans l’Explorateur Windows.<br/> Cet indicateur n’est pas combiné avec SELFLAG_TAKESELECTION.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </dl></td>
<td style="text-align: left;">Ajoute l’objet à la sélection actuelle ; le résultat possible est une sélection non contiguë. <br/> À moins qu’elle ne soit combinée avec SELFLAG_TAKEFOCUS, cet indicateur ne change pas le focus ou l’ancre de sélection. Le SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinaison revient à ajouter un élément à une sélection manuellement en maintenant la touche CTRL enfoncée et en cliquant sur un objet non sélectionné dans l’Explorateur Windows.<br/> Cet indicateur n’est pas combiné avec SELFLAG_REMOVESELECTION ou SELFLAG_TAKESELECTION.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </dl></td>
<td style="text-align: left;">Supprime l’objet de la sélection actuelle ; le résultat possible est une sélection non contiguë. <br/> À moins qu’elle ne soit combinée avec SELFLAG_TAKEFOCUS, cet indicateur ne change pas le focus ou l’ancre de sélection. Le SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combinaison équivaut à supprimer un élément d’une sélection manuellement, en maintenant la touche CTRL enfoncée tout en cliquant sur un objet sélectionné dans l’Explorateur Windows.<br/> Cet indicateur n’est pas combiné avec SELFLAG_ADDSELECTION ou SELFLAG_TAKESELECTION.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Oleacc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[Sélection des objets enfants](selecting-child-objects.md)
</dt> </dl>

 

 





