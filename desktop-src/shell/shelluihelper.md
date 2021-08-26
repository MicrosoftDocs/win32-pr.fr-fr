---
description: implémenté par le shell pour aider le script et Microsoft Visual Basic les développeurs utilisent certaines des fonctionnalités disponibles dans l’interpréteur de commandes. L’objet ShellUIHelper n’a pas de propriétés ou d’événements. Des méthodes sont fournies pour ajouter des éléments à l’interpréteur de commandes.
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
ms.openlocfilehash: f254bd218024b3d1df15a826da701b1f010ae616
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473325"
---
# <a name="shelluihelper-object"></a>Objet ShellUIHelper

implémenté par le shell pour aider le script et Microsoft Visual Basic les développeurs utilisent certaines des fonctionnalités disponibles dans l’interpréteur de commandes. L’objet **ShellUIHelper** n’a pas de propriétés ou d’événements. Des méthodes sont fournies pour ajouter des éléments à l’interpréteur de commandes.

## <a name="members"></a>Membres

L’objet **ShellUIHelper** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **ShellUIHelper** a ces méthodes.




| Méthode | Description | 
|--------|-------------|
| <a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a> | Ajoute un nouveau canal à la liste de canaux dans le menu <strong>favoris</strong> d’Internet Explorer et à la barre de <strong>canaux</strong> sur le bureau.<br /><blockquote>[!Note]<br />cette méthode n’est plus prise en charge sous Windows Vista. Sous ce système d’exploitation, il retourne E_NOTIMPL.</blockquote><br /> | 
| <a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a> | Ajoute un élément à Active Desktop.<br /> | 
| <a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a> | Affiche l’interface utilisateur par défaut pour la création d’un élément favori. L’interface utilisateur est initialisée avec les paramètres spécifiés.<br /> | 
| <a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a> | Indique si une URL spécifiée est abonnée à.<br /> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




