---
description: Expose des méthodes qui activent des pages HTML hébergées dans une extension d’Assistant pour communiquer avec l’Assistant.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Objet WebWizardHost (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: c5bcf40a77c2f464d5277ac4823ed74a3f3c2bdd6a2114d2431684cc8b319f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967747"
---
# <a name="webwizardhost-object"></a>Objet WebWizardHost

Expose des méthodes qui activent des pages HTML hébergées dans une extension d’Assistant pour communiquer avec l’Assistant.

## <a name="members"></a>Membres

L’objet **WebWizardHost** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **WebWizardHost** a ces méthodes.



| Méthode                                                      | Description                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Annuler**](iwebwizardhost-cancel.md)                     | Simule un clic sur le bouton **Annuler** .<br/>                                                                                                                                    |
| [**FinalBack**](iwebwizardhost-finalback.md)               | Accède à la page côté client qui précède immédiatement la page hébergeant les pages HTML côté serveur.<br/>                                                                    |
| [**FinalNext**](iwebwizardhost-finalnext.md)               | Accède à la page de l’Assistant côté client qui suit la page qui héberge les pages HTML côté serveur, ou termine l’Assistant s’il n’y a pas d’autres pages côté client.<br/> |
| [**SetHeaderText**](iwebwizardhost-setheadertext.md)       | Définit le titre et le sous-titre qui s’affichent dans l’en-tête de l’Assistant. En général, le client affiche l’en-tête au-dessus du code HTML et sous la barre de titre.<br/>                    |
| [**SetWizardButtons**](iwebwizardhost-setwizardbuttons.md) | Met à jour les boutons **précédent**, **suivant** et **Terminer** dans le frame de l’Assistant du client.<br/>                                                                                    |



 

### <a name="properties"></a>Propriétés

L’objet **WebWizardHost** a ces propriétés.



| Propriété                                               | Type d’accès           | Description                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Caption**](iwebwizardhost-caption.md)<br/>   | Lecture/écriture<br/> | Non implémenté.<br/>                              |
| [**Propriété**](iwebwizardhost-property.md)<br/> | Lecture/écriture<br/> | Définit ou récupère la valeur actuelle d’une propriété.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |
| IID<br/>                      | CLSID \_ WebWizardHost<br/>                                                        |



 

 




