---
description: Implémenté par le Shell pour aider le script et Microsoft Visual Basic les développeurs utilisent certaines des fonctionnalités disponibles dans l’interpréteur de commandes. L’objet ShellUIHelper n’a pas de propriétés ou d’événements. Des méthodes sont fournies pour ajouter des éléments à l’interpréteur de commandes.
title: Objet ShellUIHelper (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973731"
---
# <a name="shelluihelper-object"></a>Objet ShellUIHelper

Implémenté par le Shell pour aider le script et Microsoft Visual Basic les développeurs utilisent certaines des fonctionnalités disponibles dans l’interpréteur de commandes. L’objet **ShellUIHelper** n’a pas de propriétés ou d’événements. Des méthodes sont fournies pour ajouter des éléments à l’interpréteur de commandes.

## <a name="members"></a>Membres

L’objet **ShellUIHelper** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **ShellUIHelper** a ces méthodes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Méthode</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></td>
<td style="text-align: left;">Ajoute un nouveau canal à la liste de canaux dans le menu <strong>favoris</strong> d’Internet Explorer et à la barre de <strong>canaux</strong> sur le bureau.<br/>
<blockquote>
[!Note]<br />
Cette méthode n’est plus prise en charge sous Windows Vista. Sous ce système d’exploitation, il retourne E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></td>
<td style="text-align: left;">Ajoute un élément à Active Desktop.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></td>
<td style="text-align: left;">Affiche l’interface utilisateur par défaut pour la création d’un élément favori. L’interface utilisateur est initialisée avec les paramètres spécifiés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></td>
<td style="text-align: left;">Indique si une URL spécifiée est abonnée à.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




